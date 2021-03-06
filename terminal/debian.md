Debian commands
---------------

* Login as root: `su` (or `su -m` to preserve the environment)
* Create user: `adduser LOGIN`
	- Change password: `passwd LOGIN`
	- Create home: `mkdir /home/LOGIN; chown LOGIN:users /home/LOGIN` 
	- Login as this user: `su -m -s /bin/bash LOGIN` (`login LOGIN` doesn't work)
* Groups (primair & secundair):
	- bekijken eigen groepen: `groups`
	- toevoegen secundaire groepen: `usermod -a -G GROUP-NAME USER-NAME`
* Passwordless login: append local `~/.ssh/id_rsa.pub` to remote file `~/.ssh/authorized_keys`
* Determine Debian version: `cat /etc/debian_version`
* `man page` [systemctl](https://manpages.debian.org/stretch/systemd/systemctl.1.en.html)

Package manager
---------------

Zie ook: <http://newbiedoc.sourceforge.net/tutorials/apt-get-intro/info.html>

* Make package list up-to-date: `apt-get update`
* Search for a package: `apt-cache search PACKAGE_SUBSTRING` (or surf to <http://packages.debian.org/PACKAGE_SUBSTRING>)
* Show info about a package: `apt-cache show PACKAGE_NAME`
* Show installed packages: `dpkg --get-selections`

Certbot (Letsencrypt)
---------------------

* Timer & service staan in `/lib/systemd/system`
* Logs staan in `/var/log/letsencrypt`


