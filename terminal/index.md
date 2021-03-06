index
=====

Sometimes urgently needed, but almost never remembered command-line utilities on Mac:

- **codesign** -- Create and manipulate code signatures
- **pbcopy** -- provide copying to the pasteboard (the Clipboard)
- **pbpaste** -- provide pasting from the pasteboard (the Clipboard)
- **sips** -- scriptable image processing system

For software developmnt, one might use one or more of these obscure tools:

- **hexdump** -- ASCII, decimal, hexadecimal, octal dump. Use "-C" for that classical PC-Tools like hexview
- **otool** -- object file displaying tool (check dynamic libraries of binaries)
- **install_name_tool** -- change dynamic shared library install names
- **codesign** -- Create and manipulate code signatures


Bugs in terminal commands
-------------------------

* __mkdir__: the `-v` option (verbose) doesn't work in combination with the `-p` (Create intermediate directories). rdar://30893732
* __find__: it seams that with options `-type d -depth 1`, find will still walk the complete directory tree, which makes it pretty slow at times. A solution is to use `ls -F` in combination with `grep` (to filter the wanted lines) and `sed` (to remove the trailing `/`).


Handy resources
---------------

* [Furbo's The Terminal](http://furbo.org/2014/09/03/the-terminal/)
* [Mac Terminal Tips](https://mjtsai.com/blog/2016/09/26/mac-terminal-tips/)
* [Scripting Bash](https://scriptingosx.com/bash/)  - Scripting OS X
* [Bash-It](https://github.com/Bash-it/bash-it) - Bash-it is a collection of community Bash commands and scripts for Bash 3.2+. (And a shameless ripoff of oh-my-zsh 😃)
  - [Yonce](https://yoncetheme.com) - A Queen Bey inspired theme for Bash-It

