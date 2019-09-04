# Data Model

A **datum** is the atomic concept in the system.
Every datum belongs to a dataset.
It gives a value for some property of some item.
It has a provenance and is represented with a codec.
We can not eliminate the possibility of encountering more than one value
for a property of an item - this could happen due to a computational error.

A **dataset** corresponds to a single research product
and consists of a set of single data items (_datum_s).
It combines information about the items it contains,
the properties (mathematical invariants) each item has,
which codecs are used to encode the actual values,
and finally, the provenances of all data contained in it.
The datasets can overlap non-trivially, e.g. the smaller graphs in 
the [Census of Cubic Vertex-Transitive Graphs](http://staff.matapp.unimib.it/~spiga/census.html)
also appear in the list of [Transitive Graphs](http://staffhome.ecm.uwa.edu.au/~00013890/remote/trans/index.html),
which also contains graphs of other degrees.

An **item** is a single mathematical object, 
represented in the system simply by a unique identifier.
Examples of these include groups, graphs, lattices, and other complex mathematical objects.
An item can belong to more than one dataset:
the Petersen graph naturally appears in both previously mentioned censuses.

**Provenance** is information on how and under which conditions each datum was produced.
Note that a datum can have more than one provenance.
This happens whenever the value of a property of an item is
computed independently in different datasets.

A **property** is a mathematical invariant of a mathematical structure.
An example of such a property is orthogonality of a matrix.
A property can be encoded in several ways
(recall the case of integers in LMFDB, where three different encodings are used).
Encodings of objects (such as the `graph6` representation for graphs)
are a special case of properties.

A **codec** is a pair of partial mappings between 
mathematical values of properties and the values represented in the database.
A codec combines the concepts of
* a _mathematical type_,
* _condition operators_, and
* a _database type_
with interface components such as a presenter (value display, possibly via a view) and condition widgets.

This data model already works well over the large set of examples we have examined so far.
To support more datasets, we will add further concepts in the future.
One of the concepts we want to add are ``Aggregated Datasets''. 
These are composed of several datasets and will introduce support for databases such as the OEIS or House of Graphs.
These curated datasets are composed of a large number of smaller contributions.
