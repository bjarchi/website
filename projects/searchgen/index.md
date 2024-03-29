---
layout: page
title: SearchGen
---

SearchGen is a script for generating a trie in C. I wrote it as an
experiment to see how a bytecode based matcher (like those used by
many regular expression engines) and the same logic written in native
assembly would compare.

The obvious difference is that for the bytecode system, there is a
small amount of code used to interpret it, while my system has a
larger code footprint and thus may cause cache pressure in the
instruction cache. Also, an interpreter may get better branch
prediction behaviour because of the tight loop, where mine probably
sufferes from many mispredictions. If someone has access to a copy of
the Intel vTune performance analysis tools, I’d be interested in the
results.

### Usage

Download the [source](searchgen-0.1.tar.gz) and unpack the
tarball. The file `build.py` is the main program. The files `main.c`
and `main-len.c` are example programs. The `Makefile` is a good
example of how to build using the script. The `words` file is used as
a test case.

When given a dictionary the script generates a header file which
defines a single `match` function. There are two modes. When given the
`--length` option the match function expects the length of the input
string to be given as an argument. Otherwise it expects the string to
be null terminated. Depending on the dictionary, one may be more
efficient than the other.

The match function returns the index into the supplied dictionary file
of the word that was found, or -1 if there was no match.
