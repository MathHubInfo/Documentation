# MathHub Surface Formats

[Flexiformal](FlexiForms) content in MathHub can be
[authored](authoring) in various **surface formats** better
suited for human manipulation.

MathHub currently supports the following five surface formats natively:

  - **HTML5** and **TeX**/**LaTeX** (as a minimally flexiformal document
    formats)
  - **[sTeX](http://github.com/KWARC/sTeX)** (semantic TeX/LaTeX) is an
    extension of **LaTeX** that allows to annotate LaTeX documents with
    semantic properties and relations.
  - **[MMT](http://uniformal.github.io)** syntax.
  - **TWELF** (Edinburgh Logical Framework in [TWELF](http://twelf.org)
    syntax)

Additionally, the native formats of the [theorem prover
libraries](/libraries) imported into MathHub are handled by special
importers on a system-by-system basis.

Flexiformal content authored in any of these surface formats can is
[converted](build-system) to [OMDoc/MMT](omdoc-mmt) format for
[interoperability](interoperability) and processing in MathHub.info.
