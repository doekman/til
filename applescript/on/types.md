On Types
========

On Text
-------

Text is an ordered series of Unicode characters, also known as string. Some basic operations:

	set t to "Hello World"
	get length of t
	get text 7 thru 11 of t -- substring, returns "World"
	set t to t & " to you!" -- concat
	set t to "He said \"Use the '\\' character.\"" --escape quotes and backslashes
	set special_characters to space & tab & return & linefeed & quote --text constants


On Lists
--------



On Records
----------



Shell interaction
-----------------

To use a variable containing a path, you need to use the quoted form, in case the path contains special characters:

	set posix_path to "/Applications/Safari Technology Preview.app"
	set disk_usage to do shell script "du -d 0 -h " & quoted form of posix_path

However, `quoted form of` wraps the text in single quotes. While this is a very safe choice, it prevents you from using `~/`-syntax (and environment variables). When you need this, you can use this trick:

	set posix_path to "~/Dropbox (Personal)/"
	set quoted_posix_path to quoted form of posix_path
	set escaped_posix_path to do shell script "printf \"%q\" " & quoted_posix_path
	do shell script "cd " & escaped_posix_path & "; ls -l"
