Solved
------

When learning a new language, sometimes it difficult to wrap your head around new concepts. This page lists all issues I faced, that I actually solved, but only after I learned I had made a wrong assumption. My errors may be a bit embarrasing at times, but I think admitting them will make me a better programmer. Besides, I'm probably not the only one learning about my own faulty assumptions.

* Both `month` and `weekday` properties of the `date class` are actually enumerations. I tried comparing them to a string in order to map them to a numerical representation: October=October actually evaluated to false... After realizing these are constants, I tried casting them to a integer. Much better!

