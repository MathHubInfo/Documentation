# Local MathHub

`lmh` is an [MMT  tool for managing a set of MathHub repositories and their
dependencies](https://uniformal.github.io/doc/applications/lmh.html). It
adds an abstraction layer for local editing workflows over GIT commands
based on the particular layout of MathHub repositories.

`lmh` commands look like this:

    mmt lmh action [options]

Valid actions are:

``` 
    root      prints the root directory of the Local Math Hub repository 
    install   fetches a MathHub repository and its dependencies
    xhtml     generate XHTML
    init      initialize repository with MathHub repository structure
    commit    commits all changed files
    push      send changes to mathhub
    clean     clean repositories of generated files
    depcrawl  crawls current repository for dependencies
    sms       generates sms files, alias for lmh gen --sms
    omdoc     generates omdoc files, alias for lmh gen --omdoc
    pdf       generates pdf files, alias for lmh gen --pdf
```

Most actions are sensitive to the local directory and restrict them to that. The option
`-h` gives help, in particular, `mmt lmh -h` generates a current version of the
documentation in the table above.
