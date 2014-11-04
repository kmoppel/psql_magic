psql_magic
==========

Conventions based "auto-complete" for "psql" (PostgreSQL command line client) for faster data-skimming.

Tested with Postgres 9.3 and 9.4

Usage
==========


```
postgres=# \*

psql_magic usage 1: "\* table_pattern [o|od|oa|oc|oca|ocd|om|oma|omd] [lX]"

	table_pattern - "*" can be used for wildcards. full table names (with schema) will be searched
	[o|od|oa|oc|oca|ocd|om|oma|omd] - optional order by clause
		where:
		[o]-> order by PK. sort direction determined by .psqlrc variable psql_magic_default_order_by_direction
		[c|m] -> [created|modified]. column patterns defined by psql_magic_created_column_patterns variable 
		[a|d] -> [asc|desc]. column patterns defined by psql_magic_created_column_patterns variable 
	[lX] - optional "limit X" clause. if not specified default "limit" defined by psql_magic_default_row_limit wil be used

psql_magic usage 2: "\* table_pattern w[here] column_pattern column_value"

	table_pattern - "*" can be used for wildcards. full table names (with schema) will be searched
	column_pattern - "*" can be used for wildcards
	column_value - quotes will be added automatically

```
