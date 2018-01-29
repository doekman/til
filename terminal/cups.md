CUPS
====

Printen op macOS.

links
-----

* <https://lapserv.maths.cam.ac.uk/docs/osxprint108.html>
* <https://www.cups.org/doc/man-cupsd.conf.html>
* <https://www.cups.org/doc/man-cups-files.conf.html>
* <https://www.papercut.com/kb/Main/HowToEnableDebugCUPS> - How to Enable Debug in CUPS
* <https://www.papercut.com/kb/Main/HowToEnableDebugInThePrintProvider> - How to Enable Debug in the Print Provider
* <https://developer.apple.com/library/content/technotes/tn2124/_index.html#//apple_ref/doc/uid/DTS10003391-CH1-SECPRINTING> - Mac OS X Debugging Magic: Printing (CUPS)

locaties en commando's
----------------------

	/etc/cups/
	/private/var/log/cups/

	sudo launchctl stop org.cups.cupsd
	sudo launchctl start org.cups.cupsd