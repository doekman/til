Debian commands
---------------

* Login as root: `su` (or `su -m` to preserve the environment)
* Change password: `passwd`
* Passwordless login: append local `~/.ssh/id_rsa.pub` to remote file `~/.ssh/authorized_keys`
* Determine Debian version: `cat /etc/debian_version`


Package manager
---------------

Zie ook: <http://newbiedoc.sourceforge.net/tutorials/apt-get-intro/info.html>

* Make package list up-to-date: `apt-get update`
* Search for a package: `apt-cache search PACKAGE_SUBSTRING` (or surf to <http://packages.debian.org/PACKAGE_SUBSTRING>)
* Show info about a package: `apt-cache show PACKAGE_NAME`
* Show installed packages: `dpkg --get-selections`
