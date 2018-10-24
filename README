runsed is a wrapper for the command "sed -f sed.script FILE". runsed runs
the script-file called "sed.script" (which must exist in the current directory)
on each FILE listed on the command line.  runsed changes the files in place,
that is, it replaces the existing FILE with a stream-edited copy of itself.

A copy of each original FILE is created called ".FILE.runsed" in the directory
that FILE resides.

Two special files are also created in the current directory to allow you
to review all the changes made as well as undo the changes if the results
weren't what you expected.  The files ".runsed.diff.runsed" and
".runsed.undo.runsed" are executable.

When you are eventually satisfied simply remove all files called ".*.runsed"
with the command:
    rm .*.runsed

If you changed files in subdirectories, this is a better way to get rid
of all the crufty leftovers:
    find . -name '.*.runsed' -type f -print0 | xargs -0 /bin/rm -f

Ultimately it's up to you to clean up the crufty leftover files.
