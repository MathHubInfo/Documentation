# What can MathHub do for you?

MathHub Data is a unified infrastructure to support FAIR mathematical research data.  Specifically, it aims to support the usual kind of data -- data that conform to the relational data model, in contrast to, for example, formalised mathematics or research papers.  MathHub Data builds on and is a part of the MathHub portal for narrative and symbolic mathematical data.

The infrastructure provided by MathHub Data includes storage and a searchable interface for datasets.  The team is setting up a dataset submission process that will involve peer review, and thus improve the reliability of published data.

The authors need to 
- write a description of the dataset structure from which a schema theory is generated. The main part of this description is a list of mathematical invariants/properties, in your case: rank, f-vector, automorphism group, ...
- produce a file (or files) that contains the data,
- describe the provenance of data (an explanation of how things were produced),
- finally, the potentially time consuming thing is to formalise the math involved together with the knowledge engineers from the MathHub Data team.

The formalisation serves as documentation and sets things up for interoperability between datasets and systems. We can do as little or as much of it as the author wants, but if you promise to do it, it lets you bring in the interoperability buzzword.

MathHub Data contains a library of codecs. If a desired codec does not exist, the MathHub Data team organises the implementation. Domain experts are needed for this, so the dataset authors will typically be asked to either help with the domain specific knowledge or alternatively help find other experts.
