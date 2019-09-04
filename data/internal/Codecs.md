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
