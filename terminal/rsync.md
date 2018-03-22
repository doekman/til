rsync
=====

The `rsync` command-line utility is very well equiped, but you have to use it a lot, before you become fluent.
That's why I include some examples here.

Copy all files of a certain type (remove `--dry-run` to actually perform the command). And yes, the patterns are case sensitive:

    rsync -av --include '*/' --include '*.(JPG|jpg)' --exclude '*' --prune-empty-dirs --dry-run ~/source/folder ~/destination/folder

[More examples](https://www.garron.me/en/go2linux/rsync-backup-linux-using-rsync-to-backup-files-or-folder-under-linux.html "How to copy files and sync files between Linux or Mac computers with rsync")
