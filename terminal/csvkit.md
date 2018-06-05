CSVKit
======

Install [csvkit][], including Postgres driver for SqlAlchemy:

	pip3 install csvkit
	pip3 install psycopg2-binary #(if it failes with "can't find libpq-fe.h", install this first: brew install pgcli)
	
Convert to JSON:

	csvjson data.csv > data.json

Import into PostgreSQL:

	csvsql --db postgresql:///database --insert data.csv

Extract data from PostgreSQL:

	sql2csv --db postgresql:///database --query "select * from data" > extract.csv

And [much more](http://csvkit.readthedocs.io/en/0.9.1/)...

For diffing csv files, use [daff](http://paulfitz.github.io/daff/) (install: `pip3 install daff`)

[csvkit]:
	http://csvkit.readthedocs.io/en/latest/
	"Awesome!"
