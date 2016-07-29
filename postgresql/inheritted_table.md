Inheritted Tables
=================

Get table name
--------------
You can get the name of the underlaying table without joining to `pg_class`:

    select *, tableoid::regclass::text AS table_name
    from base_table
    ;
