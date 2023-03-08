% TODO
% John Gabriele and Ninad Khargonkar

Couple of TODO items copied from John's website and added a some QoL items of 
my own!

1. [x] *Title:* Change the default for doc title. If no `% title DOC_TITLE` block
   found, then instead of quitting, simply use the filename as a sane default. 
2. [x] *Copyright:* Auto create the copyright information based on some command 
   line args string. Add a sane default with fun name!
3. [x] *Document Footer:* 
   1. [x] Remove the option to view pandoc markdown source 
   2. [x] Update link to rippledoc repo to point to custom repo with my changes
   3. [x] Edit string for copyright to remove the word copyright!
   4. [x] Add last modified: date, time and timezone.
4. [x] *Links:* write pandoc filter to auto-convert internal markdown links
   to html. This will ensure inter-linking of files is preserved even when
   converted to html. See [this](https://stackoverflow.com/q/40993488/9579260)
   stack overflow thread for ideas about how to implement this.
   1. [ ] Embed the filter inside `rippledoc.py` and use that instead of requiring
      users to supply the file. Of course, if they supply a file, also use that!
5. [ ] *Style:* Edit the default css file according to your needs!
6. [ ] *Output:* Option for writing html files to a custom `_site` dir.
7. [ ] *Help Docs:* Create a list of docs and host them on your github webpage.
   Refer the help message of this website to the edited docs.
8. [ ] *Cleanup:* Add feature to clean up all generated files
   1. [ ] `--clean`: remove all generated .html, toc.conf, and styles.css files
   2. [ ] `--modified`: shows which md files have been modified and need processinng
9. [ ] Title in browser window & bookmark should include project name
10. [ ] Check to make sure there's at least one doc file present other than index.md.