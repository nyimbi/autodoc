# PostgreSQL Autodoc

This is a utility which will run through PostgreSQL system tables and returns HTML, DOT, and 2 styles of XML which describes the database.

The HTML is human readable (via webbrowser). The first style of XML is actually the fileformat of Dia, a UML diagram tool. The second type of XML is similar to the HTML but in the Docbook 4 format. It enables yous to mix in other docbook documentation via the XREFs, generating PDFs, HTML, RTF, or other formatted documents. Between these tools and JavaDoc with the appropriate XREFs, documentation about a project can be generated quickly and be easily updatable yet have a very professional look with some DSSSL work.


[Options](#OPTIONS)  
[Author](#AUTHOR)  

## Usage

**postgresql_autodoc** [options]

<a name="DESCRIPTION"></a>

#


<a name="OPTIONS"></a>

## OPTIONS

**−d <dbname>**

Specify database name to connect to (default: current user)


**−f <file>**

Specify output file prefix (default: current user)

**−h <host>**

Specify database server host (default: localhost)

**−p <port>**

Specify database server port (default: 5432)

**−u <username>**

Specify database username (default: current user)

**−−password=<pw>**

Specify database password (default: blank)

If no password is specified, one is prompted for.


**−w**



Use ~/.pgpass for authentication (overrides all other password options)



**−l <path>**

Path to the templates (default: @@TEMPLATE-DIR@@)

**−t <output>**

Type of output wanted (default: All in template library)



**−s <schema>**



Specify a specific schema to match. Technically this is a regular expression but anything other than a specific name may have unusual results.

**−m <regexp>**

Show only tables/objects with names matching the specified regular expression.

**−−table=<args>**

Tables to export. Multiple tables may be provided using a comma-separated list, i.e. table,table2,table3.

**−−statistics**

In 7.4 and later, with the contrib module pgstattuple installed we can gather statistics on the tables in the database (average size, free space, disk space used, dead tuple counts, etc.) This is disk intensive on large databases as all pages must be visited.

<a name="AUTHOR"></a>

## AUTHOR

Rod Taylor <autodoc@rbt.ca>

* * *
