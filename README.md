% Rippledoc Extended
% Ninad Khargonkar
% 2023

# Info
Modifying [rippledoc](http://www.unexpected-vortices.com/sw/rippledoc/index.html)
for personal use. Rippledoc is a useful utility to render a folder full of 
markdown files to html counterparts. I sourced the code for rippledoc from its 
GitLab [repository](https://gitlab.com/uvtc/rippledoc).

- Preserves Links
- Default css theme is nice!
- Produces table of contents (toc) which is useful for documentation and wiki-like notes.
- Free to modify and change according to our own needs.

Complete documentation for my tool (including changes) can be found on
[project's website](https://kninad.github.io/rippledoc-ext/)
and the source code in its github [repo](https://github.com/kninad/rippledoc-ext/).

# Original Readme

**A particularly easy-to-use doc processing tool.**

Rippledoc is a command-line program that uses
[Pandoc](http://pandoc.org/) to generate easily-navigable HTML from a
bunch of Markdown-formatted text files (it ripples down into
subdirectories looking for .md files).

This tool was modified from the original
[rippledoc](http://www.unexpected-vortices.com/sw/rippledoc/index.html) for
for personal use. Rippledoc is a useful utility to render a folder full of 
markdown files to html counterparts. My source file merely extends the original
with some features that I found to be useful.


That is, it turns:

~~~
doc/
    index.md
    changes.md
    getting-started.md
    examples/
        ex-1.md
        ex-2.md
~~~

into:

~~~
doc/
    index.md
    index.html
    changes.md
    changes.html
    styles.css  # <-- additionally created by Rippledoc
    toc.conf    # <-- additionally created by Rippledoc
    getting-started.md
    getting-started.html
    examples/
        ex-1.md
        ex-1.html
        ex-2.md
        ex-2.html
        toc.conf  # <-- additionally created by Rippledoc
~~~

(You can, optionally, omit the ./index.md file and instead use a
../README.md if you prefer.)

Rippledoc requires nearly zero configuration; you just run it in a
directory containing Markdown-formatted text files (see [more
info](more-info.html) for the few rules you've got to follow) and it
does the rest.

Find the full Rippledoc docs rendered in lovely html at
<http://www.unexpected-vortices.com/sw/rippledoc/index.html>. The
source is located at <https://gitlab.com/uvtc/rippledoc>.

Under the hood, Rippledoc uses [Pandoc](http://pandoc.org/) to do the
markdown ➞ html conversion.


Purpose
=======

The main goals for Rippledoc are:

  * make it as easy as possible to create, write, and manage
    nice-looking, ordered, easily-navigable docs
  * make it as easy as possible for others to contribute to your
    docs
  * not tie you to any one particular doc processing tool (including
    this one)


OS Compatibility
================

The author has not given even a passing thought to running this
program on any OS other than GNU/Linux.



Quick Usage
===========

~~~bash
cd path/to/my-project
touch README.md
cd doc
touch _copyright getting-started.md  # tutorial.md, changes.md, ...
# Edit those files, then run Rippledoc, telling it to use ../README.md.
rippledoc.py --readme_is_index
~~~

and point your browser to <file:///path/to/my-project/doc/index.html>
to see the results.

> Of course, [this site you're reading
> now](http://www.unexpected-vortices.com/sw/rippledoc/index.html) was
> generated using Rippledoc.

To upload your docs to a server, you might use rsync:

~~~bash
rsync -urv --delete /path/to/your-proj/doc you@remote:public_html/your-proj
~~~

That will put the local `doc` directory into the remote `your-proj`
directory.



License
=======

Copyright 2014–2018 John Gabriele

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or (at
your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
