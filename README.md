# rippledoc-ext
Modifying [rippledoc](http://www.unexpected-vortices.com/sw/rippledoc/index.html) for personal use. 
Rippledoc is a useful utility to render a folder full of markdown files to html counterparts. I sourced
the code for rippledoc from its GitLab [repository](https://gitlab.com/uvtc/rippledoc).

- Preserves Links
- Default css theme is nice!
- Produces table of contents (toc) which is useful for documentation and wiki-like notes.
- Free to modify and change according to our own needs.

# TO DO

1. [x] *Title:* Change the default for doc title. If no `% title DOC_TITLE` block
   found, then instead of quitting, simply use the filename as a sane default. 
2. [x] *Copyright:* Auto create the copyright information based on some command 
   line args string. Add a sane default with fun name!
3. [x] *Document Footer:* 
   1. [x] Remove the option to view pandoc markdown source 
   2. [x] Update link to rippledoc repo to point to custom repo with my changes
   3. [x] Edit string for copyright to remove the word copyright!
   4. [x] Add last modified: date, time and timezone.
4. [ ] *Links:* write pandoc filter to auto-convert internal markdown links
   to html. This will ensure inter-linking of files is preserved even when
   converted to html. See [this](https://stackoverflow.com/q/40993488/9579260)
   stack overflow thread for ideas about how to implement this. (**Major**)
5. [ ] *Style:* Edit the default css file according to your needs!
6. [ ] *Output:* Option for writing html files to a custom `_site` dir.
7. [ ] *Help Docs:* Create a list of docs and host them on your github webpage.
   Refer the help message of this website to the edited docs.
   
    

# Original README

**A particularly easy-to-use doc processing tool.**

Rippledoc is a command-line program that uses
[Pandoc](http://pandoc.org/) to generate easily-navigable HTML from a
bunch of Markdown-formatted text files (it ripples down into
subdirectories looking for .md files).

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
rippledoc.py --readme-is-index
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
