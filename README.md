# tree

an implementation of the unix tree command

## goals

some goals for the program

- provide a basic set of features
  - hide files and directories begining with a '.' (dot) by default, use an option to show these entries
  - do not follow directory symlinks by default, use an option to follow directory symlinks, unless a cycle is detected
  - list all available entries by default, use an option to restrict entries to the current disk device
- include an option to limit the descention depth
- include an option to filter entries and only show directories
  - expand on this to limit output to certain kinds of files (symlinks,pipes,fifos,etc)
- include an option to not show link names for symlinks (git-annex inspired)
- include an option to not descend into some known vcs directories


A more general goal/guideline is to have options in common with [**OpenBSD**](https://www.openbsd.org)'s version of [**ls(1)**](https://man.openbsd.org/ls.1) should use the same option flag. e.g. since **-L** is used to follow directory symlinks in [**ls(1)**](https://man.openbsd.org/ls.1) it will have the corresponding behaviour in **tree(1)**.

## non-goals

some things that will **likely** not be implemented.

- unicode block characters used for diagram segments or pointers
- output to html,json,xml,etc
- color or stylized output
