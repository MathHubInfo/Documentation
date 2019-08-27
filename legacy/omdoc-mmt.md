# OMDoc/MMT in MathHub

The uniform representation format for
[[flexiformal|FlexiForms]] content in
[MathHub](https://mathhub.info)is the **OMDoc**/**MMT** format.

[OMDoc](http://omdoc.org/) (**O**pen **M**athematical **Doc**uments) is
a content-oriented representation format for
[[flexiformal|FlexiForms]] mathematical knowledge and
documents. The content is represented at three levels:

1.  **object level** (mathematical formulae and phrases)
2.  **statement level** (axioms, definitions, theorems, proofs, ...)
3.  **context level** (theories declare symbol and terminology for
    mathematical domains and languages; theory morphisms relate theories
    in meaning-preserving ways)

The [MMT](http://uniformal.github.io) (**M**odular **M**athematical
**T**heories) is a rational reconstruction of the formal core of OMDoc
that clarifies the semantic status of many OMDoc constructs and extends
it to a web-scalable foundation-independent meta-framework for formal
mathematical knowledge.

We are currently working towards unifying OMDoc and MMT by generalizing
MMT language primitives to the flexiformal case, and complementing MMT
by a presentation/narrative layer. The target (tentatively called
OMDoc2) of this unification is the intended representation format of
MathHub. Until it is ready for deployment, we use the evolving OMDoc and
MMT formats in their respective intended scopes.

At the processing level, the integration is already further along, so we
use an extension of the [MMT API](http://uniformal.github.io) as a
uniform processing platform in MathHub.
