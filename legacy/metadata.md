# MathHub Metadata

Metadata and documentation occur at three levels:

1.  at the **system-level** in the `meta` pseudo-library that contains
      - a repository `help` with documentation about the
        [MathHub.info](https://mathhub.info) system itself.
      - a repository `conf` with system configuration
      - a repository `inf` with metadata about the set of libraries in
        MathHub in `MANIFEST.MF` form (see below).
2.  at the **library/user space-level** in the `meta-inf` repository in
    the respective GitLab group or namespace. This repository contains
    the `MANIFEST.MF` file with metadata and additional files with HTML5
    fragments for documentation.
3.  at the level of **[math archives](math-archives)**
    metadata is given in the metadata file `MANIFEST.MF` and additional
    HTML5 fragment files in the `META-INF` dimension.

For the content of the `MANIFEST.MF` we consider an example:

    ...    
    description:desc.html
    title:Mathematical Vernacular
    teaser:The special language to express mathematical knowledge
    responsible: kolhlhase@kwarc.info

We have elided the [math archive metadata](math-archives)
here. The other metadata are given in the form of a key:value property
list.

  - `description:` contains the (relative) path name of a HTML5 fragment
    file that contains a description of the repository.
  - `title:` and `teaser:` the title (itself, not a file name) and a
    teaser text. Both can be HTML5 fragments.
  - finally `responsible:` a comma-separated list of e-mails of the
    responsible persons.
