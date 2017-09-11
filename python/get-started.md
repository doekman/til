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

Activate a previously installed version of a formula (because Debian doesn't have 3.6 installed yet):

    brew info python3
    brew switch python3 3.5.2_3
    brew pin python3

If you've never installed the previous Python version, but want to:

		git clone git@github.com:Homebrew/homebrew-core.git      #Clone locally, because GitHub thinks the repo is 
		cd homebrew-core/Formula/                                #  to complex to search
		git log python3.rb                                       #Find the hash of the version you want
		git rev-parse 1e62c645b2                                 #Get the full hash
		git checkout 1e62c645b2fc2d82042d9f7c364c6a246f2e11ed .  #And go back to the version
		brew uninstall python3                                   #Uninstall python3 (files stay on your computer)
		brew install ./python3.rb                                #and install the old version
		pip3 install --upgrade pip setuptools wheel
		#don't forget to upgrade your virtual environments
		git reset --hard                                         #and optionally reset the git-repo to the current head


pip
---

With Python comes pip, the package manager for Python stuff. Type `pip3 install psycopg2` to install the Postgres driver for [SqlAlchemy][], Python's db-driver/ORM. Type `pip install psycopg2` to install this for Python 2. Or better: use *venv* and `pip` will automatically use the right Python version.


venv
----
A Virtual Environment is a tool to keep the dependencies required by different projects in separate places, by creating virtual Python environments for them. 

* Create: `python3 -m venv path/to/venv`
* Activate: `source path/to/venv/bin/activate`
* Deactivate: `deactivate`


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

