Common commands
===============

For installing stuff, you can use package managers (brew, pip, gem: see python getting started), and you also can use [Cask][cask] to install programs.

[cask]: https://caskroom.github.io

date
----

To get the date in [ISO 8601][iso8601] (~ish) format, execute:

	date "+%Y-%m-%d %H:%M:%S"
	
This can be abbreviated to:
	
	date "+%F %T"
	
To include timezone information:

	date "+%F %T %Z" # with symbol, like CEST
	date "+%F %T %z" # +0200 notation

And to print UTC time, in 100% correct ISO 8601 format:
	
	date -u "+%FT%TZ"

OS X El Capitan (10.11) doesn't implement `%N` for nanoseconds (or `%3N` for milliseconds) in `STRFTIME`. Check [these alternatives][nanoSecondsOnOsX].

[iso8601]: https://en.wikipedia.org/wiki/ISO_8601

[nanoSecondsOnOsX]: http://serverfault.com/a/423642


space cowboy
------------

A shell script to display SEE YOU SPACE COWBOY whenever you logout of your terminal!

I learned that a peace of work is often better than 
[generic](http://patorjk.com/software/taag/#p=display&f=Graceful&t=See%20You%20Space%20Cowboy) 
[stuff](https://github.com/busyloop/lolcat) and must be appreaciated. 

* <https://gist.github.com/danielrehn/d2e6f2129e5f853c3166>
