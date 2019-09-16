# What can MathHub Data do for you?

MathHub Data is a unified infrastructure to support FAIR mathematical research data.  
Specifically, it aims to support the usual kind of data -- data that conform to the relational data model, 
in contrast to, for example, formalised mathematics or research papers.  
MathHub Data builds on and is a part of the MathHub portal for narrative and symbolic mathematical data.

The infrastructure provided by MathHub Data includes storage and a searchable interface for datasets.  The team is setting up a dataset [submission process](submission-editorial.md) that will involve peer review, and thus improve the reliability of published data.

## Joe's story

Joe has a simple [matrix dataset](https://joe.discretezoo.xyz/) and wants to submit it to MathHub Data.
This is going to be a little more work than just putting it on his website,
but he is convinced that the benefits will easily outweigh the extra work.
He first contacts one of the [MathHub Data editors](submission-editorial.md#people-involved-and-their-roles) 
and sends them a description of his dataset (in paragraph or a few paragraphs, as needed).
It could look a little bit like the following.

> My matrix dataset contains three _2_ by _2_ integer matrices.
> I have computed their traces, eigenvalues, and orthogonality.
> It is important to several people who write about the MathHub Data project,
> as they need a simple dataset to explain things on.

The dataset is accepted and the editor guides Joe through the submission process.
Joe first describes the structure of his dataset with the help of 
[MathHub Data knowledge engineers](submission-editorial.md#people-involved-and-their-roles) 
The end result is a 
[schema theory for the matrix dataset](https://gl.mathhub.info/ODK/mbgen/blob/master/source/matrix_schema.mmt).
The main content of this description is a list of mathematical properties or invariants used in the dataset:
matrix, trace, orthogonal, eigenvalues.

An important part of the schema theory is specifying how the mathematical values can be 
stored at the database level.
Mappings between the mathematical and database level are called codecs.
MathHub Data contains a library of codecs. 
If a desired codec does not yet exist, the MathHub Data team organises the implementation. 
Domain experts are needed for this, so the dataset authors will typically be asked 
to either help with the domain specific knowledge or alternatively help find other experts.

The other important aspect of the schema theory is that it connects the properties
to the Math in the Middle Ontology.
The formalisation serves as documentation and sets things up for interoperability between datasets and systems. 

Finally, Joe prepares a JSON file with the data and a file describing the provenance of data 
(an explanation of how things were produced).
