# Math Archives

**Math Archives** organize the different dimensions of mathematical
knowledge into a standardized directory tree layout to facilitate
archiving ([details and
discussion](https://kwarc.info/people/frabe/Research/HIJKR_dimensions_11.pdf)).
MathHub has adopted Math Archives as the main packaging format, manages
knowledge in this format, and stores all knowledge as versioned math
archives in the [MathHub GitLab Server](http://gl.mathhub.info).

The dimensions of a Math Archive include (other dimensions are possible,
but are not standardized in MathHub)

1.  `source`: the human-editable [surface language representations](surface-formats).
2.  `content`: the [OMDoc/MMT](omdoc-mmt) generated from the
    `source` dimension.
3.  `narration`:
4.  `presentation`:
5.  `relational`:
6.  `errors`: the errors encountered by the compilation pipelines organized into
    subdirectories by the [build targets](build-targets) that produced them.
7.  `export`: ??????
8.  `latexml`: the [OMDoc 1.3](http://www.omdoc.org/OMDoc1.3/) version
    of the `source` dimension.

All of these are given as subdirectories of the math archive, which also contains

1.  the `META_INF` directory for metadata, it contains
    1.  a file `MANIFEST.MF`, which specifies the archive name `id`, base URLs
        (`source-base` and `narration-base`, dependencies on other math archives
        (`dependencies`; these can be cyclic), maintainers (`responsible`), documentation
        strings for the [libraries page](/libraries) (`title`, `teaser`, and
        `description`), and information on generated branches (`generated-branches`).
    2.  other HTML5 files with further description (if they are
        referenced in the `MANIFEST.MF` file.)
    3.  Legacy/convenience Scala scripts like `serve.msl` and
        `build.msl`. These are a mostly deprecated mechanism and are not
        used in MathHub.
