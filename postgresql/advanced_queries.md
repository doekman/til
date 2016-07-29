Advanced Queries
================

UPSERT
------

You can `INSERT` or `UPDATE` (when the record already exists) in one statement:

    INSERT INTO table_name (name, age, email) VALUES 
        ('Doeke Zanstra', 43, 'doekman@icloud.com'), 
        ('Tester until Example', 60, 'test@example.com'), 
    ON CONFLICT (email) DO UPDATE SET 
    	name = EXCLUDED.name,
        age = EXCLUDED.age
    ;

Composite type
--------------
A composite ("complex") type can help structure things:

    DROP TYPE if exists adres;
    CREATE TYPE adres AS (
      straat varchar(50),
      huisnr int,
      huisnr_toev varchar(50),
      postcode char(6),
      plaats varchar(50)
    );
    DROP TABLE if exists personen;
    CREATE TABLE personen (
    	id serial,
    	naam varchar(50),
    	"adres" adres,
    	email varchar(255),
    	PRIMARY KEY(id)
    );

    INSERT INTO personen("naam", "adres", "email") 
        VALUES('Doeke', ROW('Superstraat',51,NULL,'4321ZY','Gownum'), 'bla@papperle.pap')
    ;
    INSERT INTO personen("naam", "adres", "email") 
        VALUES('Tester', ROW('Pand',35,'b','1234AB','Xorqum'), 'tester@example.com')
    ;

    SELECT  naam, (adres).straat, (adres).huisnr, (adres).huisnr_toev
        FROM personen
    ;

