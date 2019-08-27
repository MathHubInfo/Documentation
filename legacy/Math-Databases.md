### Contents

The main contents of the catalogue are available as an overview table at [mathdb.mathhub.info](https://mathdb.mathhub.info/).

Collections and databases that are not yet entered in the overview table are listed in the section [TODO](#TODO).

### Call to action

If you have a collection or database that is not contained in a catalogue, let me know!

I will also be very grateful for any other comments you might have.

To do so, please open an [issue](https://github.com/MathHubInfo/Documentation/issues) with a label `math db`.
For other ways of contacting me, see [my FAU page](https://kwarc.info/people/kbercic/)

### <a name="TODO">TODO</a>

Possibly more could be found on [EUDAT](https://b2share.eudat.eu/).

#### MathOverflow

* Timothy Gowers asked [What could be some potentially useful mathematical databases](https://mathoverflow.net/questions/68442/what-could-be-some-potentially-useful-mathematical-databases)

* Gordon Royle asked [What are some early examples of creation of lists / catalogues of (particularly) combinatorial objects?](https://mathoverflow.net/questions/47044/what-are-some-early-examples-of-creation-of-lists-catalogues-of-particularly)

Look for keywords such as
[atlas](https://mathoverflow.net/search?q=atlas),
[census](https://mathoverflow.net/search?q=census),
[collection](https://mathoverflow.net/search?q=collection),
[database](https://mathoverflow.net/search?q=database),

* [Database of simplicial polytopes/spheres](https://mathoverflow.net/questions/218316/database-of-simplicial-polytopes-spheres?rq=1)

Unsorted resources:
* [Manifold atlas](http://www.map.mpim-bonn.mpg.de/Main_Page) (possibly contains a collection of manifolds?)
* [Number theory calculator sites/tables](http://www.numbertheory.org/ntw/N1.html)
* [Design Theory](http://www.maths.qmul.ac.uk/~lsoicher/designtheory.org/)
* [SuiteSparse](https://sparse.tamu.edu/)
* [Distributome](http://www.distributome.org/)
* [The Multiply Perfect Numbers Page](http://wwwhomes.uni-bielefeld.de/achim/mpn.html)

#### Miscelaneous

* [Software Heritage](https://www.softwareheritage.org/)
* [Oberwolfach References on Mathematical Software](https://orms.mfo.de/)
* [The Open Graph Archive: A Community-Driven Effort](https://arxiv.org/abs/1109.1465) (discontinued)
* [Inverse Symbolic Calculator](http://wayback.cecm.sfu.ca/projects/ISC/ISCmain.html), [Inverse Symbolic Calculator Plus](https://isc.carma.newcastle.edu.au/)
* [Cantor's Attic](http://cantorsattic.info/Cantor%27s_Attic) - a comprehensive resource of information about all notions of mathematical infinity
* [Complexity ZOO](https://complexityzoo.uwaterloo.ca)
* [A compendium of NP optimization problems](http://www.nada.kth.se/~viggo/problemlist/compendium.html)
* [Graph Classes](http://www.graphclasses.org)

### Other kinds of mathematical data

* [The TPTP Problem Library for Automated Theorem Proving](http://tptp.org/)
* SMTPlib

## <a name="Index">Index</a>

### [Database Requirements](#Requirements)

### [Updated Requirements](#Requirements2)

#### [FAIR Principles](#FAIR)

### [Contents](#SurveyContents)

### [Collection features, classification](#Features)

# <a name="Requirements">Database Requirements</a>

[Go up](#Index) to index.

In alphabetical order.

1. **Citable**  
The records in the database need to be citable.
1. **Coverage information**  
The database interfaces should make explicit the assumptions made by the system and collections as well as providing information on the completeness of the search results. For example for graphs:  _"the search results are complete for your search parameters up to order 511"_.
1. **Collaborative**  
The database should be collaborative. It needs to be easy for people to contribute and it must be possible for any data to find out who contributed it and when. In particular,
    1. adding a new collection should ideally be a declarative task as opposed to a programming one -- it should suffice to describe the structure of the collection,
    1. changes such as adding new kinds of objects, new collections, new properties, or updates to existing values need to be tracked by the database.
1. **Decentralised**  
The database should not rely on the existence of a central authority.  An entry in a local copy of the database should be easily distributable to other copies without any third-party intervention.
1. **Interoperable**  
Other systems (like databases and computer algebra systems) should be able to interact with the database. This involves having well defined APIs.
1. **Non-redundant**  
The objects should be stored up to isomorphism.
1. **Provenance**
In addition to the information on who and when produced the data, the database needs to provide information on how the data were obtained (algorithms used, software libraries, pipelines, etc.).
1. **Self-explaining**  
The database interfaces should make accessing definitions of concepts and further information easily available.
1. **Searchable**  
The database should have at least a basic search (filter) functionality for objects
1. **User-friendly**  
The database should provide suitable interfaces.  This means
    1. simple, intuitive and easily accessible interfaces for casual users (it should avoid exposing the casual user to low level interfaces, such as Python, SageMath, SQL, ...),
    1. making usage easy or easier for power users.

# <a name="Requirements2">Updated Requirements</a>

[Go up](#Index) to index.

This is a draft.

## <a name="FAIR">FAIR</a>

The descriptions of the principles are short excerpts from [GO FAIR](https://www.go-fair.org/fair-principles/).

### <a name="F">Findable</a>

#### <a name="F1">F1</a>: (Meta)data are assigned globally unique and persistent identifiers

[F1 at GO FAIR](https://www.go-fair.org/fair-principles/f1-meta-data-assigned-globally-unique-persistent-identifiers/)

Globally unique and persistent identifiers remove ambiguity in the meaning of your published data by assigning a unique identifier to every element of metadata and every concept/measurement in your dataset.
- **Dataset:** The dataset has a globally unique and persistent identifier.
- **Datum:** The data are assigned globally unique and persistent identifiers.
- **Metadata**: The metadata have a globally unique and persistent identifier.

#### <a name="F2">F2</a>: Data are described with rich metadata

[F2 at GO FAIR](https://www.go-fair.org/fair-principles/f2-data-described-rich-metadata/)

Rich metadata allow a computer to automatically accomplish routine and tedious sorting and prioritising tasks that currently demand a lot of attention from researchers.  Rich metadata implies that you should not presume that you know who will want to use your data, or for what purpose.
- **Metadata**: The metadata richly describes the data.

#### <a name="F3">F3</a>: Metadata clearly and explicitly include the identifier of the data they describe

[F3 at GO FAIR](https://www.go-fair.org/fair-principles/f3-metadata-clearly-explicitly-include-identifier-data-describe/)

The metadata and the dataset they describe are usually separate files. The association between a metadata file and the dataset should be made explicit by mentioning a dataset’s globally unique and persistent identifier in the metadata.
- **Metadata**: Metadata clearly and explicitly include the identifier of the data they describe.

#### <a name="F4">F4</a>: (Meta)data are registered or indexed in a searchable resource

[F4 at GO FAIR](https://www.go-fair.org/fair-principles/f4-metadata-registered-indexed-searchable-resource/)

The metadata and the dataset they describe are usually separate files. The association between a metadata file and the dataset should be made explicit by mentioning a dataset’s globally unique and persistent identifier in the metadata.
- **Dataset:** The dataset is registered or indexed in a searchable resource.
- **Datum:** The data are registered or indexed in a searchable resource.
- **Metadata**: The metadata are registered or indexed in a searchable resource.

### <a name="A">Accessible</a>

#### <a name="A1">A1</a>: (Meta)data are retrievable by their identifier using a standardised communication protocol

[A1 at GO FAIR](https://www.go-fair.org/fair-principles/metadata-retrievable-identifier-standardised-communication-protocol/)

FAIR data retrieval should be mediated without specialised tools or communication methods. So, clearly define who can access the actual data, and specify how.  Most users of the internet retrieve data by ‘clicking on a link’. This is a high-level interface to a low-level protocol called tcp, that the computer executes to load data in the user’s web browser.
- **Dataset:** The dataset is retrievable by its identifier using a standardised communication protocol.
- **Datum:** The data are retrievable by their identifiers using a standardised communication protocol.
- **Metadata**: The metadata are retrievable by their identifier using a standardised communication protocol.

#### <a name="A11">A1.1</a>: The protocol is open, free and universally implementable

[A1.1 at GO FAIR](https://www.go-fair.org/fair-principles/a1-1-protocol-open-free-universally-implementable/)

To maximise data reuse, the protocol should be free (no-cost) and open (-sourced) and thus globally implementable to facilitate data retrieval. Anyone with a computer and an internet connection can access at least the metadata.
- **Dataset:** The protocol to retrieve the dataset is open, free and universally implementable.
- **Datum:** The protocol to retrieve the data is open, free and universally implementable.
- **Metadata**: The protocol to retrieve the metadata is open, free and universally implementable.

#### <a name="A12">A1.2</a>: The protocol allows for an authentication and authorisation where necessary

[A1.2 at GO FAIR](https://www.go-fair.org/fair-principles/a1-2-protocol-allows-authentication-authorisation-required/)

This is a key, but often misunderstood, element of FAIR. The ‘A’ in FAIR does not necessarily mean ‘open’ or ‘free’. Rather, it implies that one should provide the exact conditions under which the data are accessible. Hence, even heavily protected and private data can be FAIR. Ideally, accessibility is specified in such a way that a machine can automatically understand the requirements, and then either automatically execute the requirements or alert the user to the requirements.
- **Dataset:** The protocol to retrieve the dataset allows for an authentication and authorisation where necessary.
- **Datum:** The protocol to retrieve the data allows for an authentication and authorisation where necessary.
- **Metadata**: The protocol to retrieve the metadata allows for an authentication and authorisation where necessary.

#### <a name="A2">A2</a>: Metadata should be accessible even when the data is no longer available


[A2 at GO FAIR](https://www.go-fair.org/fair-principles/a2-metadata-accessible-even-data-no-longer-available/)

Metadata are valuable in and of themselves, when planning research, especially replication studies. Even if the original data are missing, tracking down people, institutions or publications associated with the original research can be extremely useful.
- **Metadata**: Metadata should be accessible even when the data is no longer available.

### <a name="I">Interoperable</a>

#### <a name="I1">I1</a>: (Meta)data use a formal, accessible, shared, and broadly applicable language for knowledge representation

[I1 at GO FAIR](https://www.go-fair.org/fair-principles/i1-metadata-use-formal-accessible-shared-broadly-applicable-language-knowledge-representation/)

Humans should be able to exchange and interpret each other’s data (so preferably do not use dead languages). But this also applies to computers, meaning that data that should be readable for machines without the need for specialised or ad hoc algorithms, translators, or mappings.
- **Dataset:** The dataset uses a formal, accessible, shared, and broadly applicable language for knowledge representation.
- **Datum:** The data use a formal, accessible, shared, and broadly applicable language for knowledge representation.
- **Metadata**: The metadata use a formal, accessible, shared, and broadly applicable language for knowledge representation.

#### <a name="I2">I2</a>: (Meta)data use vocabularies that follow the FAIR principles

[I2 at GO FAIR](https://www.go-fair.org/fair-principles/f2-data-described-rich-metadata/)

The controlled vocabulary used to describe datasets needs to be documented and resolvable using globally unique and persistent identifiers. This documentation needs to be easily findable and accessible by anyone who uses the dataset.
- **Dataset:** The dataset uses vocabularies that follow the FAIR principles.
- **Datum:** The data use vocabularies that follow the FAIR principles.
- **Metadata**: The metadata use vocabularies that follow the FAIR principles.

#### <a name="I3">I3</a>: (Meta)data include qualified references to other (meta)data

[I3 at GO FAIR](https://www.go-fair.org/fair-principles/i3-metadata-include-qualified-references-metadata/)

A qualified reference is a cross-reference that explains its intent. For example, X is regulator of Y is a much more qualified reference than X is associated with Y, or X see also Y. The goal therefore is to create as many meaningful links as possible between (meta)data resources to enrich the contextual knowledge about the data, balanced against the time/energy involved in making a good data model. To be more concrete, you should specify if one dataset builds on another data set, if additional datasets are needed to complete the data, or if complementary information is stored in a different dataset.
- **Dataset:** The dataset includes qualified references to other (meta)data.
- **Datum:** The data include qualified references to other (meta)data.
- **Metadata**: The metadata include qualified references to other (meta)data.

### <a name="R">Reusable</a>

#### <a name="R1">R1</a>: (Meta)data are richly described with a plurality of accurate and relevant attributes

[R1 at GO FAIR](https://www.go-fair.org/fair-principles/r1-metadata-richly-described-plurality-accurate-relevant-attributes/)

It will be much easier to find and reuse data if there are many labels are attached to the data. Principle R1 is related to F2, but R1 focuses on the ability of a user (machine or human) to decide if the data is actually USEFUL in a particular context.
- **Dataset:** The dataset is richly described with a plurality of accurate and relevant attributes.
- **Datum:** The data are richly described with a plurality of accurate and relevant attributes.
- **Metadata**: The metadata are richly described with a plurality of accurate and relevant attributes.

#### <a name="R11">R1.1</a>: (Meta)data are released with a clear and accessible data usage license

[R1.1 at GO FAIR](https://www.go-fair.org/fair-principles/r1-1-metadata-released-clear-accessible-data-usage-license/)

Under **I**, we covered elements of technical interoperability. R1.1 is about legal interoperability. What usage rights do you attach to your data? This should be described clearly. Ambiguity could severely limit the reuse of your data by organisations that struggle to comply with licensing restrictions. Clarity of licensing status will become more important with automated searches involving more licensing considerations. The conditions under which the data can be used should be clear to machines and humans.
- **Dataset:** The dataset is released with a clear and accessible data usage license.
- **Metadata**: The metadata is released with a clear and accessible data usage license.

**Notes.** This is under the assumption that the data inherit the dataset license.

#### <a name="R12">R1.2</a>: (Meta)data are associated with detailed provenance

[R1.2 at GO FAIR](https://www.go-fair.org/fair-principles/r1-2-metadata-associated-detailed-provenance/)

For others to reuse your data, they should know where the data came from (i.e., clear story of origin/history, see R1), who to cite and/or how you wish to be acknowledged. Include a description of the workflow that led to your data: Who generated or collected it? How has it been processed? Has it been published before? Does it contain data from someone else that you may have transformed or completed? Ideally, this workflow is described in a machine-readable format.
- **Dataset:** The dataset is associated with detailed provenance.
- **Datum:** The data are associated with detailed provenance.
- **Metadata**: The metadata are associated with detailed provenance.

**Notes.** In most cases the value at R1.1 for data will just get copied over from the value for the dataset.

#### <a name="R13">R1.3</a>: (Meta)data meet domain-relevant community standards

[R1.3 at GO FAIR](https://www.go-fair.org/fair-principles/r1-3-metadata-meet-domain-relevant-community-standards/)

It is easier to reuse data sets if they are similar: same type of data, data organised in a standardised way, well-established and sustainable file formats, documentation (metadata) following a common template and using common vocabulary. If community standards or best practices for data archiving and sharing exist, they should be followed.
- **Dataset:** The dataset meets meet domain-relevant community standards.
- **Datum:** The data meet domain-relevant community standards.
- **Metadata**: The metadata meet domain-relevant community standards.

## Other Requirements

1. 

# <a name="SurveyContents">Contents</a>

[Go up](#Index) to index.

## <a name="Other">Other Resources</a>

#### 1. Some <a name="Jipsen">Lists</a> of finite Structures

Generated by a script on-the-fly.

http://www1.chapman.edu/~jipsen/finitestructures.html

_[Peter Jipsen](http://www1.chapman.edu/~jipsen)_

## Lists

#### 1. Crowdsourcing project for the database of numbers of isomorphism types of finite groups

https://github.com/alex-konovalov/gnu/wiki/Mathematical-databases

collected by _[Alex Konovalov](https://github.com/alex-konovalov)_


#### 2. DiscreteZOO

https://github.com/DiscreteZOO/DiscreteZOO-overview/issues


#### 3. The Encyclopedia of Graphs

http://atlas.gregas.eu/sources


#### 4. House of Graphs

https://hog.grinvin.org/MetaDirectory.action


### Meta papers


#### 1. Fingerprint Databases for Theorems

https://sites.math.washington.edu/~billey/papers/fingerprints.pdf

_Sara Billey and Bridget Tenner_


#### 2. Semantic-aware Fingerprints of Symbolic Research Data

https://link.springer.com/content/pdf/10.1007%2F978-3-319-42432-3_51.pdf

_Hans-Gert Gräbe_


### Data in Software Packages


#### 1. Optional and standard databases for Magma
http://magma.maths.usyd.edu.au/magma/download/db/

#### 2. Overview of data libraries in GAP
http://www.gap-system.org/Datalib/datalib.html
- https://simpcomp-team.github.io/simpcomp/ comes with an extensive library of known triangulations of manifolds

#### 3. SageMath databases
http://doc.sagemath.org/html/en/reference/databases/index.html



# <a name="Features">Collection features, classification</a>

[Go up](#Index) to index.

Some additional features to consider for databases:  query API, license, ...

Sometimes it makes more sense to just generate objects on the fly.  Are there systems that partly store, partly generate on the fly? (Small Groups in GAP?)

## Fingerprints and related

Most collections contain mathematical objects (encoded in some way), each object typically has some extra data.  What is the nature of these data and how do the collection's authors refer to it (i.e. data, invariants, properties, some kind of fingerprints)?  In particular, if the collection uses fingerprints, what is their nature?

For fingerprinting resources, see the [papers](#Papers).

## Querying

What kind of querying does the collection support?  Do the queries only use the object data or do they look at the structure of encoded objects directly in some way?