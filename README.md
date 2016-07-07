sedRename
=========

A shell script for renaming files using a sed script to derive the new names
from the old ones.
Provides a simulation-mode (-s option) showing what would be done.

Works by first splitting the names (including extension) from the given paths,
giving each name to sed applying the given script and using the result as the
new name for the file system object.

Detected errors:
* New name would be empty
* New name collides with new name of another FS object
* New name collides with another FS object's current name

Requires:
* Python 3

Usage:
* sedRename (-s) script path (path)..
