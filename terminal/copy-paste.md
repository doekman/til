Copy paste
==========

You can get the location of a program to the clipboard with the command `which psql | pbcopy`. You can use values from the clipboard with the command ``cp `pbpaste` .``. 

Typing `cp ` and then <key>cmd+c</key> won't work, because a newline character has also been copied, and the command will be executed prematurely. 

Of course you could use the command ``cp `which psql` .`` in this case 😉.

* There doesn't seem to be a "append to pasteboard" option with `pbcopy`; you can do it like `(pbpaste; which psql) | pbcopy`
* Linux often uses the [xclip](http://tedhagos.com/linux/clipboard-copy-paste-terminal.html) command
* <http://osxdaily.com/2007/03/05/manipulating-the-clipboard-from-the-command-line/>
* Use `screencapture -c` to copy the screen to the copy/paste buffer
