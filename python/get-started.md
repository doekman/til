Getting started with Python on OS X
===================================

brew 
----

First you need to install [brew][], which is a package manager of macOS. This we need to manage non-Python packages. You also might need to tweak things [manually][doingItRight]. Don't forget to run `xcode-select --install` (if not, it will compile all installed packages, which totally makes sense) 

With the commands `brew update` you update brew itself. `brew outdated` lists all outdated package, 
and `brew upgrade` update these packages. With `brew upgrade $PackageName`, you upgrade this 
specific package.

More info on [brew's FAQ][brewFaq]

python
------

The command `brew python` installs Python version 2.7.x, and `brew python3` installes the Python 3.5.x.

pip
---

With Python comes pip, the package manager for Python stuff. Type `pip3 install csvkit` to install [csvkit][] using Python 3.


[brew]: http://brew.sh
[doingItRight]: http://docs.python-guide.org/en/latest/starting/install/osx/#doing-it-right
[brewFaq]: 
	https://github.com/Homebrew/brew/blob/master/share/doc/homebrew/FAQ.md 
	"Brew's Frequently Asked Questions"
[csvkit]:
	http://csvkit.readthedocs.io/en/0.9.1/
	"Awesome!"
	
Links:
	
* <http://docs.python-guide.org/en/latest/>

