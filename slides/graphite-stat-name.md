## Stats - Names

A name is a string with some periods in it, like:

> some.text.with.periods.in.it

Each period will represent a directory on the filesystem, each with a subdirectory, ending in the location of the whisper database archive for the stat. Stated differently, carbon will create a tree of directories, containing subdirectories, until a stat name has no more periods.
