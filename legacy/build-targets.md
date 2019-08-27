# MathHub Build System

The [MathHub build system](build-system) has several targets,
which we document here

  - `planetary`  
    ?????
  - `latexml`  
    applies the [LaTeXML daemon](http://dlmf.nist.gov/LaTeXML/) to
    [sTeX](surface-formats) sources to produce
    [OMDoc 1.3](http://www.omdoc.org/OMDoc1.3/) output. The results go into the `latexml`
    dimension of a [math archive](math-archives).
  - `stex-omdoc`  
    converts [OMDoc 1.3](http://www.omdoc.org/OMDoc1.3/) to
    [OMDoc/MMT](omdoc-mmt) for further processing. The
    results go into the `content` dimension of a [math archive](math-archives).
  - `svg `  
    ????? pre-generates SVG visualizations of the OMDoc/MMT theory
    graphs. The results go into the `????` dimension of a [math archive](math-archives) ????
  - `mmt-omdoc`  
    converts the [MMT surface syntax](surface-formats) to
    [OMDoc/MMT](omdoc-mmt) for further processing. The
    results go into the `content` dimension of a [math archive](math-archives).
  - `mh-html`  
    pre-generates semantically annotated HTML5 presentations from
    [OMDoc/MMT](omdoc-mmt) contents to be served on the
    MathHub web portal. The results go into the `narrative` dimension of
    a [math archive](math-archives).
  - `index`  
    ?????
