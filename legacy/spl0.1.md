# SMGloM Public License

SPL Version 0.1: 2014-02-01 Copyright (c) 2014 Michael Kohlhase

Everyone is permitted to copy and distribute verbatim copies of this
license document, but modification is not allowed.

## 1. Preamble

The SMGloM Public License (SPL) is the license under which the content
of the SMGloM (Semantic Multilingual Glossary for Mathematics) content
is distributed. To use this license, the files of your distribution
should have an explicit copyright notice giving the name of the
copyright holder and the year, together with a reference to this
license. A typical example would be
```
%% Copyright 2013 M. Y. Name
%% http://mathhub/user/4711
%% Contributors: S. O. Other http://mathhub/user/0815
%% Source: http://mathhub.info/smglom/smglom/source/dgraph.en
%% Maintainer: http://mathhub.info/group/mgroup
%% State: released
% This glossary entry can redistributed and/or modified under the terms of the
% SMGloM Public License available at smglom/spl0.1 or a later version of
% the SMGloM Public License`

## 2. DEFINITIONS

A SMGloM glossary entry consists of

  - a glossary module declaration which declares a unique module name
    and contains
      - a finite number of import declarations to other modules,
      - a finite number of symbol declarations (with module-unique
        symbol names), and
      - a finite number of notation definitions.
  - a finite number of language bindings for that module indexed by
    language identifiers. Each of these contains
      - a finite number of definitions for symbols declared in the
        corresponding module.
      - a finite number of verbalization definitions for these symbols

Both module declarations and language bindings are jointly referred to
as glossary (entry) components. The module name of a language binding is
the pair of the name of the corresponding module and the ISO 639-1
language identifier.

## 3. WARRANTY

There is no warranty for the SMGloM glossary entries, to the extent
permitted by applicable law. In no event unless required by applicable
law or agreed to in writing will The Copyright Holder, or any of the
individual authors named in the glossary entry be liable to you for
damages, including any general, special, incidental or consequential
damages arising out of any use of glossary entry or out of inability to
use the glossary entry.

## 4. DISTRIBUTION

Redistribution of unchanged glossary components in source or compiled
form is allowed either individually or in the form of a sub-collection
of the SMGloM collection. The development of derived versions and their
distribution are allowed under the following restrictions:

  - **D1**. The derived work acknowledges the fact that it is derived
    from the original work and maintains a prominent reference in the
    work to the original source including its module name and URI.
  - **D2**. If the derived work is a glossary component, then the file
    name and module names must be changed so that it cannot be confused
    with the original source.
  - **D3**. The derived work is distributed/licensed under terms that
    allow the compilation of derived works, but keep paragraphs 1. and
    2. intact. The simplest way to do this is to distribute the derived
    work under the SMGloM license, but this is not a requirement.

## 5. MAINTENANCE

Every glossary entry published in SMGLoM has a current maintainer group,
and a state that are specified in the copyright notice or the metadata
of the module. The state of a module can be one of

  - *experimental*: under development, incomplete, and thus liable to
    change;
  - *complete*: under development, but considered complete
  - *stable*: approved by the maintainer group as ready for use with the
    assurance that there will not be semantic changes
  - *deprecated*: an obsolete module kept only for archival purposes.
    The members of the maintainer group can change the the wording of
    the definitions and the markup without without having to change the
    file/module name provided that the meaning of the symbol is not
    changed in any way.

## 5. TRANSLATION

Existing glossary entries can be extended by a language binding for a
module, as long as it is a translation of the existing language
bindings. In particular, a language binding must supply definitions for
all symbols of a module to be labeled complete.
