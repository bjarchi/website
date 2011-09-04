---
layout: page
title: Figfs
---

The Filesystem Interface to Git (known by the acronym "figfs",
pronounced like "figs") allows developers to work with a project in a
Git repository just like a local filesystem. This means that all the
branchs, tags, and revisions are available for browsing without having
to check anything out. This is great for browsing project histories
because you can have your editor pointed at two different versions at
once and can use all your normal tools like diff to compare things.

In addition, figfs has the ability to create a "workspace" in which
the contents of the repository at a particular revision can be freely
edited.

### Releases

v0.1.0: First official release, *very* beta-level code:
[source](figfs-0.1.0.tar.bz2)
[linux-amd64](figfs-0.1.0-linux-amd64.tar.bz2)

### Getting the source

The project is a work in progress. The current source can be obtained
from version control with the following command or you can [browse the
source online](http://github.com/reillyeon/figfs):

    git clone git://github.com/reillyeon/figfs.git

The following packages are required to build and run figfs:

* [ounit](http://www.xs4all.nl/~mmzeeman/ocaml/) (tested with 1.0.2)
* [camlzip](http://cristal.inria.fr/~xleroy/software.html#camlzip) (tested with 1.03)
* [ocaml-sqlite3](http://www.ocaml.info/home/ocaml_sources.html#toc13) (tested with 1.2.0)

Code is licensed under the GPLv2. The project was my Senior Design
Project at the University of Pennsylvania’s School of Engineering and
Applied Science with Jonathan M. Smith as advisor.
