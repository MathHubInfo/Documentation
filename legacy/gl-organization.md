# MathHub GitLab Organization

The MathHub repositories are managed via an instance of
[GitLab](http://gitlab.org) whose accounts and access groups are
synchronized with the [MathHub.info](http://mathhub.info) portal. A
description of MathHub worflows can be found
[[here|lmh-workflows]].

### Content Layout of [GL.MathHub.info](http://gl.mathhub.info)

The flexiforms on [GL.MathHub.info](http://gl.mathhub.info) are hosted
on topical and personal repositories, which in turn are organized in
groups. Note that some of the links below may be inaccessible without
special permissions.

1.  **Project groups** host repositories for projects e.g.
      - [KwarcMH](http://gl.mathhub.info/groups/KwarcMH) for the
        flexiforms for [KWARC](http://kwarc.info) projects
      - [BaseMH](http://gl.mathhub.info/groups/BaseMH) for
        flexiformalizing the basics of various fields; a particular one
        is
      - [smglom](http://gl.mathhub.info/groups/smglom) for the Semantic
        Multilingual Glossary for Mathematics
2.  **Personal groups** host personal repositories, they come
    automatically with a MathHub author account.

### Layout of a MathHub Repository

A MathHub repository contains the following files at top level:

  - `build.msl`, and `serve.msl` for building and serving the repository
    contents via MMT.
  - `META-INF/MANIFEST.MF`: metadata for MMT, in particular, the line
    that starts with `dependencies:` states the repositories this one
    depends upon.
  - the `lib` subdirectory contains general files that sTeX needs, most
    prominently `lib/pre.tex`, `lib/post.tex` (pre/postambles for sTeX
    modules) and `lib/WApersons.tex` (a database of FOAFF metadata for
    specifying DC Metadata in sTeX)
  - A sTeX/repository-specific `.gitignore` file that informs GIT and
    `lmh` which files are generated and should not be versioned.

### Layout of a Local MathHub Working Copy

Given sufficient permissions, users can check out a local working copy
with MathHub repositories for [[local editing|lmh-workflows]].
The local working copy is in a directory `.../localmh` to which we will
refer to it with the meta-variable `<LMHDIR>` in the following. It
contains the files and subdirectories

  - `bin` for the `lmh` tool
  - `ext` for the external tools:
    [LaTeXML](http://dlmf.nist.gov/LaTeXML/), a powerful LaTeX to XML
    converter and [sTeX](https://github.com/KWARC/sTeX), a semantic
    extension of LaTeX, and [MMT](http://uniformal.github.io), the
    knowledge management library for MathHub
  - `docs` for the source-level documentation of the `lmh` tool.
  - `sty` for packages used in the flexiforms not found in the
    repositories
  - `styles` for the notation definitions MMT uses for generating XHTML
    from OMDoc
  - `logs` for crash reports that will help developers improve `lmh`.
  - `MathHub` for the MathHub repositories.

The `MathHub` contains subdirectories `<group>/<repos>` that are
structured as described above.
