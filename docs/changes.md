% Changes
% John Gabriele, Ninad Khargonkar

# v2023-03-08

  * Auto pick the doc's title from filename if no `% title` line on top of doc.
  * Option to pass copyright info as a command line instead of always
    requiring a file.
  * Option to use a custom lua filter script which maps the markdown doc
    links to their equivalent html.
  * Custom document footer with doc update time.
  * Update the project documentation, host it on github pages and point to the
    repo's doc instead of rippledoc's home when printing help message.

# v2018-08-15

  * Instead of using heuristics, added `--readme_is_index` option.
  * Updated docs. Removed index.md, using ../README.md instead.
  * Made prev/next links spread out across nav header and footer.
  * Minor styling updates.

# v2018-08-11

  * If there's no index.md, but there's a ../README.md, use that
    README as an index.md.
  * Updated Rippledoc's docs to reflect that change, plus a few
    more minor improvements.


# v2018-07-20

  * Put in better side nav area. Removed all the sub-ToC files, which
    also allowed removing clutter from the header/footer nav bars.


# v2018-07-12

  * Rippledoc rewritten in Python. Started new changelog.
  * moved from GitHub to GitLab
  * removed old side nav pane
  * changed version numbering to date-style
  * now automatically adds newly-added files to existing toc.conf
