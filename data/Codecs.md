# Codec Master List

See [codec consolidation](https://github.com/MathHubInfo/mdh_django/issues/7).

The three main sources are:
- [data.mathhub.info code](https://github.com/MathHubInfo/mdh_django),
- [MDDL](https://gl.mathhub.info/ODK/mbgen/blob/master/source/MDDL.mmt),
- [LMFDB schema theories](https://github.com/OpenDreamKit/OpenDreamKit/tree/master/WP6/schematheories).

## Basic Codecs

### Codecs in Use

Codecs from MDDL and LMFDB schema theories should be gradually added to this category.

#### StandardBool

`BoolIdent: codec bool db_bool` in MDDL.

#### StandardInt

`IntIdent: codec int db_int` in MDDL.

### Auxiliaries (Import Codecs)

- **Bool:** true-false, 0-1.
- **Integer:** integers as strings, integers as lists of `base64` digits.

## Codec Operators

- **matrix**: list of lists operator (by row, column, flattened)
- **vector**: list
- **set**: as list or ordered list

## Unsorted

## MDDL

```
StringIdent : codec string db_string ❙
UUIDIdent   : codec uuid   db_uuid ❙
IntAsString : codec int    db_string ❙

/T encodes booleans as "Yes" or "No" ❙
BoolAsYesNo : codec bool   db_string ❙

ListAsArray   : {A,a} codec A a ⟶ codec (list A) (db_array a)❘# ListAsArray 3 ❙
VectorAsArray : {A,a,n} codec A a ⟶ codec (vector A n) (db_array a)❘# VectorAsArray 3 4 ❙
OptionAsNullable : {A,a} codec A a ⟶ codec (option A) a❘# OptionAsNullable 3 ❙
ProductAsArray: {A,B,e} codec A e ⟶ codec B e ⟶ codec (A * B) e ❙
MatrixAsArray : {A,a,m,n} codec A a ⟶ codec (matrix A m n) (db_array (db_array a)) ❘
              = [A,a,m,n,C] VectorAsArray n (VectorAsArray m C)❘# MatrixAsArray 5 ❙ 
FiniteTypeAsItself : {A,a} codec A a ⟶ codec (finiteType A) a ❙
FinSetAsArray : {A,a} codec A a ⟶ codec (finset A) (db_array a) ❙
 
PolynomialAsSparseArray : {r, e} codec (r.univ) e ⟶ codec (Poly r) (db_array (db_array e))❘# %%prefix 2 1 ❙
PolynomialAsDenseArray : {r, e} codec (r.univ) e ⟶ codec (Poly r) (db_array e)❘# %%prefix 2 1 ❙
```

## Elementary/Wanted

* rational numbers
* complex numbers
* real numbers
* algebraic numbers
* permutations (of integers/arbitrary sets)
* graphs
* graph extensions such as maniplexes

## Hard

* permutation groups
* finitely presented groups
* named groups
* incompleteness (minimal set, an example that exists but might not be minimal)
* relator (word composed of Coxeter string group generators rho_i (well known in community))

## Implementing a Codec

A new codec should be registered with the system in 3 places:

- the documentation
- the backend code
- the frontend code

### Documentation Codecs

(To be documented)

### Codecs in the backend

In the backend, a codec consists of a Django Model. 
Concretly, this class should subclass [Codec](https://github.com/MathHubInfo/mdh_django/blob/master/mdh_data/models/codec.py#L51). 

A typical codec looks e.g. like this:

```python

from django.db import models

from ..codec import Codec

from rest_framework import serializers


class StandardInt(Codec):
    """ Standard Integer Codec """

    value = models.IntegerField()
  
    operators = ('=', '<', '<=', '>', '>=', '!=')
    @classmethod
    def is_valid_operand(cls, literal):
        """ Checks that the argument is a valid operand """
        return isinstance(literal, int) and not isinstance(literal, bool)
```

The codec consists of several parts:

- a name, which corresponds to the name of the class. Here `StandardInt`. 
- a database type, which corresponds to a django ModelField. Here `models.IntegerField`
- a set of supported query operators. These are by default translated to SQL operators. 
- a predicate which checks if a value is a valid parameter for an operator

The code is located in an appropriate file in the [codecs folder](https://github.com/MathHubInfo/mdh_django/tree/master/mdh_data/models/codecs). 

To make sure that the codec is loaded by Django, it should be imported in [codecs/__init__.py](https://github.com/MathHubInfo/mdh_django/blob/master/mdh_data/models/codecs/__init__.py). 

After creating a new codec, appropriate Django migrations should be created and applied. 
This can be done using `python manage.py makemigrations` and `python manage.py migrate`. 
The migrations should be commited. 

### Codecs in the frontend

Each new codec also needs an appropriate implementation in the frontend. 
This is an appropriate subclass of the [Codec class](https://github.com/MathHubInfo/mdh_django/blob/master/frontend/src/codecs/codec.tsx#L68). 

A typical frontend codec implementation lives in an appropriate file in the [codecs/impl](https://github.com/MathHubInfo/mdh_django/tree/master/frontend/src/codecs/impl) directory. 
It consists of four parts:

- the name of a codec, which has to correspond to the backend codec name, 
- filter editor + viewer components, that allow the user to enter queries
- presenters, which show values of this codec to the user

The are implemented as appropriate properties of the appropriate class. 

After implementing a new class, it needs to be registered in the [CodecManager](https://github.com/MathHubInfo/mdh_django/blob/master/frontend/src/codecs/index.ts#L19) class by instatinating it. 

### Codec Operators

Codec Operators behave similarly to Codecs.
They should also be documented, and registered in appropriate places in the frontend and backend. 
It should be noted that each concrete (i.e. applied) codec operator needs to be instantiated seperatly in the frontend and backend. 
Furthermore, each concrete codec needs a unique name that is identical across backend and frontend. 

For the frontend, this is handled as a `Codec` class with appropriate arguments. 
An example can be found in [impl/MatrixAsList.tsx](https://github.com/MathHubInfo/mdh_django/blob/master/frontend/src/codecs/impl/MatrixAsList.tsx). 

For the backend, an appropriate decorator exists. 
An example for a backend codec operator can be found in [codecs/matrixaslist.py](https://github.com/MathHubInfo/mdh_django/blob/master/mdh_data/models/codecs/matrixaslist.py). 
