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

The command `brew install python` installs Python version 2.7.x, and `brew install python3` installes the Python 3.5.x.


pip
---

With Python comes pip, the package manager for Python stuff. Type `pip3 install psycopg2` to install the Postgres driver 
for [SqlAlchemy][], Python's db-driver/ORM. Type `pip install psycopg2` to install this for Python 2.


venv
----
[VirtualEnv][venv] will enable you to specify *per project* what Python version and packages to use... 


gem
---
Gem is a packager manager for Ruby, which is needed to install [lolcat][]: `sudo gem install lolcat`.
Try it with `ls -la | lolcat` or [this](https://gist.github.com/dakull/6615458#osx-users-can-have-fun-too).



[brew]: http://brew.sh
[doingItRight]: http://docs.python-guide.org/en/latest/starting/install/osx/#doing-it-right
[brewFaq]: 
	https://github.com/Homebrew/brew/blob/master/share/doc/homebrew/FAQ.md 
	"Brew's Frequently Asked Questions"
[venv]: https://virtualenv.pypa.io/en/latest/installation/
[SqlAlchemy]:
	https://en.wikipedia.org/wiki/SQLAlchemy
[lolcat]:
    https://github.com/busyloop/lolcat
wh
	
Links:
	
* <http://docs.python-guide.org/en/latest/>

