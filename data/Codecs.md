# Codec Master List

See [codec consolidation](https://github.com/MathHubInfo/mdh_django/issues/7).

## Basic Codecs

#### StandardBool

#### StandardInt

### Auxiliaries (Import Codecs)

- **Bool:** true-false, 0-1.
- **Integer:** integers as strings, integers as lists of `base64` digits.

## Codec Operators

- **matrix**: list of lists operator (by row, column, flattened)
- **vector**: list
- **set**: as list or ordered list

## Unsorted

- polynomial: as sparse array (one variable, flattened list of pairs)

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
