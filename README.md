# Rocq-verified Operational transformation for tree-like data structures

This fork of [JetBrains/ot-coq](https://github.com/JetBrains/ot-coq) is created to use it with [Rocq 9.0.0](https://rocq-prover.org/). 
For this purpose, the following changes have been made:

- To use `Hierarchy Builder` to implement `eqType`

- To use `Mczify` instead of `Omega`

- To specify load paths with the `From` syntax

except for other minor changes on the proofs to avoid warnings.
All of the `admit` and `Admitted` parts in `RichTextTests.v` still remain as they have been.

For compilation, [`rocq-hierarchy-builder-1.10.1`](https://github.com/math-comp/hierarchy-builder) and [`coq-mathcomp-zify-1.5.0`](https://github.com/math-comp/mczify) are required.
Then run 
```
coq_makefile -f _CoqProject -o CoqMakefile
make -f CoqMakefile
```
to compile it.

The original code (tag `original-ot-coq`) is preserved for reference.
The branch `master` contains modifications to make it work on modern environments. The original `README.md` follows below.


-------------------

# Coq-verified Operational transformation for tree-like data structures

[![JetBrains research project](https://jb.gg/badges/obsolete.svg)](https://confluence.jetbrains.com/display/ALL/JetBrains+on+GitHub)

This repository contains Coq source code accompanying the paper "Verified Operational 
Transformation for Trees" by S. Sinchuk, P. Chuprikov and K. Solomatov published in proceedings of 7th International Conference, ITP 2016 (pp. 358--373).
[Link to the paper](https://link.springer.com/chapter/10.1007/978-3-319-43144-4_22)

## Building
The original source code is compatible with Coq 8.4 and makes use of Ssreflect.
The repository also contains version of the code compatible with Coq 8.8 and 8.13.
Use `make -f Makefile`[^1] to build the project.
[^1] The `Makefile` has been removed from this repository to avoid confusion.
