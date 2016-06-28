rsync
=====

The `rsync` command-line utility is very well equiped, but you have to use it a lot, before you become fluent.
That's why I include some examples here.

Copy all files of a certain type (remove `--dry-run` to actually perform the command):

    rsync -av --include '*/' --include '*.JPG' --exclude '*' --prune-empty-dirs --dry-run ~/source/folder ~/destination/folder
