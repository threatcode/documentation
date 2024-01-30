---
Title: mdbtools
Homepage: https://github.com/mdbtools/mdbtools
Repository: https://salsa.debian.org/debian/mdbtools
Architectures: any all
Version: 1.0.0+dfsg-1.1
Metapackages: kali-linux-everything kali-linux-large kali-tools-database kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libmdb3
 
  Core library for accessing JET / MS Access database (MDB) files
  programmatically.
   
  Allows one to use MDB files with PHP for example.
 
 **Installed size:** `152 KB`  
 **How to install:** `sudo apt install libmdb3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libglib2.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libmdbsql3
 
  Libraries built on libmdb to provide a SQL engine for reading
  JET / MS Access database (MDB) files.
   
  See mdb-sql util in mdbtools package.
 
 **Installed size:** `71 KB`  
 **How to install:** `sudo apt install libmdbsql3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libglib2.0-0 
 * libmdb3 
 {{< /spoiler >}}
 
 
 - - -
 
 ### mdbtools
 
  These are various tools for manipulating JET / MS Access database (MDB) files:
   * utils     - provides command line utilities to list tables, export schema,
                 and data, show file versions, and other useful stuff.
   * mdb-sql   - a command line SQL tool that allows one to type SQL queries and
                 get results.
 
 **Installed size:** `257 KB`  
 **How to install:** `sudo apt install mdbtools`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libglib2.0-0 
 * libmdb3 
 * libmdbsql3 
 * libreadline8 
 {{< /spoiler >}}
 
 ##### mdb-array
 
 Export data in an MDB database table to a C array.
 
 ```
 root@kali:~# mdb-array -h
 mdb-array is deprecated and will disappear in a future version of mdbtools.
 Please drop us a line if you have any use of it.
 See https://github.com/mdbtools/mdbtools/issues/197
 
 Usage: mdb-array <file> <table>
 ```
 
 - - -
 
 ##### mdb-count
 
 Get listing of tables in an MDB database
 
 ```
 root@kali:~# mdb-count -h
 Usage:
   mdb-count [OPTION?] <file> <table> - print the number of records in an Access database
 
 Help Options:
   -h, --help       Show help options
 
 Application Options:
   --version        Show mdbtools version and exit
 
 ```
 
 - - -
 
 ##### mdb-export
 
 Export data in an MDB database table to CSV format.
 
 ```
 root@kali:~# mdb-export -h
 Usage:
   mdb-export [OPTION?] <file> <table> - export data from MDB file
 
 Help Options:
   -h, --help                        Show help options
 
 Application Options:
   -H, --no-header                   Suppress header row.
   -d, --delimiter=char              Specify an alternative column delimiter. Default is comma.
   -R, --row-delimiter=char          Specify a row delimiter
   -Q, --no-quote                    Don't wrap text-like fields in quotes.
   -q, --quote=char                  Use <char> to wrap text-like fields. Default is double quote.
   -X, --escape=format               Use <char> to escape quoted characters within a field. Default is doubling.
   -e, --escape-invisible            Use C-style escaping for return (\r), tab (\t), line-feed (\n), and back-slash (\\) characters. Default is to leave as they are.
   -I, --insert=backend              INSERT statements (instead of CSV)
   -N, --namespace=namespace         Prefix identifiers with namespace
   -S, --batch-size=int              Size of insert batches on supported platforms.
   -D, --date-format=format          Set the date format (see strftime(3) for details)
   -T, --datetime-format=format      Set the date/time format (see strftime(3) for details)
   -0, --null=char                   Use <char> to represent a NULL value
   -b, --bin=strip|raw|octal|hex     Binary export mode
   -B, --boolean-words               Use TRUE/FALSE in Boolean fields (default is 0/1)
   --version                         Show mdbtools version and exit
 
 ```
 
 - - -
 
 ##### mdb-header
 
 Write header file from an MDB database
 
 ```
 root@kali:~# man mdb-header
 mdb-header(1)        Executable programs or shell commands       mdb-header(1)
 
 NAME
        mdb-header - Write header file from an MDB database
 
 SYNOPSIS
        mdb-header [database]
 
 DESCRIPTION
        mdb-header is a utility program distributed with MDB Tools.
 
        It  will  dump  the names and types of the tables and columns in an MDB
        database in a C header format.
 
        It will create three files - types.h and dumptypes.[ch]
 
 ENVIRONMENT
        MDB_JET3_CHARSET
               Defines the charset of the input JET3 (access 97) file.  Default
               is CP1252. See iconv(1).
 
        MDBICONV
               Defines the output charset. Default is UTF-8. mdbtools must have
               been compiled with iconv.
 
        MDBOPTS
               Colon-separated list of options:
 
               o  debug_like
 
               o  debug_write
 
               o  debug_usage
 
               o  debug_ole
 
               o  debug_row
 
               o  debug_props
 
               o  debug_all is a shortcut for all debug_* options
 
               o  no_memo (deprecated; has no effect)
 
               o  use_index (experimental; requires libmswstr)
 
 EXIT STATUS
        mdb-header exits with error code 1 if there was anunsupported type.
 
 FUTURE DIRECTIONS
        mdb-header is deprecated. Soon, it will no longer be distributed.
 
        It  is the feeling of developers that it is not used, as C code genera-
        tion is now usually replaced by more generic approaches, including lib-
        mdb calls and odbc.
 
        However,  should  you  find  this  tool  useful,  drop  us  a  line  at
        https://github.com/mdbtools/mdbtools/issues/197   and   we'll  consider
        maintaining it.
 
 SEE ALSO
        mdb-array(1) mdb-count(1)  mdb-export(1)  mdb-hexdump(1)  mdb-import(1)
        mdb-json(1)  mdb-parsecsv(1)  mdb-prop(1)  mdb-queries(1) mdb-schema(1)
        mdb-sql(1) mdb-tables(1) mdb-ver(1)
 
 AUTHORS
        The mdb-header utility was written by Brian Bruns.
 
 BUGS
        Only a few types are currently supported.
 
 MDBTools 1.0.0                   03 April 2023                   mdb-header(1)
 ```
 
 - - -
 
 ##### mdb-hexdump
 
 Hexdump utility from MDB Tools
 
 ```
 root@kali:~# man mdb-hexdump
 mdb-hexdump(1)       Executable programs or shell commands      mdb-hexdump(1)
 
 NAME
        mdb-hexdump - Hexdump utility from MDB Tools
 
 SYNOPSIS
        mdb-hexdump file [pagenumber]
 
 DESCRIPTION
        mdb-hexdump is a utility program distributed with MDB Tools.
 
        mdb-hexdump makes a hex dump of a binary file (such as an mdb file).
 
 ENVIRONMENT
        MDB_JET3_CHARSET
               Defines  the charset of the input JET3 (access 97) file. Default
               is CP1252. See iconv(1).
 
        MDBICONV
               Defines the output charset. Default is UTF-8. mdbtools must have
               been compiled with iconv.
 
        MDBOPTS
               Colon-separated list of options:
 
               o  debug_like
 
               o  debug_write
 
               o  debug_usage
 
               o  debug_ole
 
               o  debug_row
 
               o  debug_props
 
               o  debug_all is a shortcut for all debug_* options
 
               o  no_memo (deprecated; has no effect)
 
               o  use_index (experimental; requires libmswstr)
 
 SEE ALSO
        mdb-array(1)  mdb-count(1)  mdb-export(1)  mdb-header(1)  mdb-import(1)
        mdb-json(1)  mdb-parsecsv(1)  mdb-prop(1)  mdb-queries(1) mdb-schema(1)
        mdb-sql(1) mdb-tables(1) mdb-ver(1)
 
 AUTHORS
        The mdb-hexdump utility was written by Brian Bruns.
 
 MDBTools 1.0.0                   03 April 2023                  mdb-hexdump(1)
 ```
 
 - - -
 
 ##### mdb-json
 
 Export data in an MDB database table to JSON.
 
 ```
 root@kali:~# mdb-json -h
 Usage:
   mdb-json [OPTION?] <file> <table> - export data from Access file to JSON
 
 Help Options:
   -h, --help                       Show help options
 
 Application Options:
   -D, --date-format=format         Set the date format (see strftime(3) for details)
   -T, --datetime-format=format     Set the date/time format (see strftime(3) for details)
   -U, --no-unprintable             Change unprintable characters to spaces (otherwise escaped as \u00XX)
   --version                        Show mdbtools version and exit
 
 ```
 
 - - -
 
 ##### mdb-parsecsv
 
 Convert CSV table dump into C file.
 
 ```
 root@kali:~# man mdb-parsecsv
 mdb-parsecsv(1)      Executable programs or shell commands     mdb-parsecsv(1)
 
 NAME
        mdb-parsecsv - Convert CSV table dump into C file.
 
 SYNOPSIS
        mdb-parsecsv file
 
 DESCRIPTION
        mdb-parsecsv is a utility program distributed with MDB Tools.
 
        mdb-parsecsv  takes  a CSV file representing a database table, and con-
        verts it into a C array.
 
 NOTES
        If the first argument does not exist as a file, mdb-parsecsv will  look
        for the same filename with '.txt' appended.
 
        The file extension is stripped, and the output written to the base name
        plus a '.c' extension.
 
 ENVIRONMENT
        MDB_JET3_CHARSET
               Defines  the charset of the input JET3 (access 97) file. Default
               is CP1252. See iconv(1).
 
        MDBICONV
               Defines the output charset to use for the SQL file.  Default  is
               UTF-8. mdbtools must have been compiled with iconv.
 
        MDBOPTS
               Colon-separated list of options:
 
               o  debug_like
 
               o  debug_write
 
               o  debug_usage
 
               o  debug_ole
 
               o  debug_row
 
               o  debug_props
 
               o  debug_all is a shortcut for all debug_* options
 
               o  no_memo (deprecated; has no effect)
 
               o  use_index (experimental; requires libmswstr)
 
 FUTURE DIRECTIONS
        mdb-parsecsv is deprecated. Soon, it will no longer be distributed.
 
        It  is the feeling of developers that it is not used, as C code genera-
        tion is now usually replaced by more generic approaches, including lib-
        mdb calls and odbc.
 
        However,  should  you  find  this  tool  useful,  drop  us  a  line  at
        https://github.com/mdbtools/mdbtools/issues/197   and   we'll  consider
        maintaining it.
 
 SEE ALSO
        mdb-array(1) mdb-count(1)  mdb-export(1)  mdb-header(1)  mdb-hexdump(1)
        mdb-import(1) mdb-json(1) mdb-prop(1) mdb-queries(1) mdb-schema(1) mdb-
        sql(1) mdb-tables(1) mdb-ver(1)
 
 AUTHORS
        The mdb-parsecsv utility was written by Brian Bruns.
 
 MDBTools 1.0.0                   03 April 2023                 mdb-parsecsv(1)
 ```
 
 - - -
 
 ##### mdb-prop
 
 Get properties list from MDB database
 
 ```
 root@kali:~# mdb-prop -h
 Usage:
   mdb-prop [OPTION?] <file> <object name> [<prop col>] - display properties of an object in an Access database
 
 Help Options:
   -h, --help       Show help options
 
 Application Options:
   --version        Show mdbtools version and exit
 
 ```
 
 - - -
 
 ##### mdb-queries
 
 Get listing of tables in an MDB database
 
 ```
 root@kali:~# mdb-queries -h
 Usage:
   mdb-queries [OPTION?] <file> <query name> - list or export queries from an Access database
 
 Help Options:
   -h, --help                Show help options
 
 Application Options:
   -L, --list                List queries in the database (default if no query name is passed)
   -1, --newline             Use newline as the delimiter (used in conjunction with listing)
   -d, --delimiter=delim     Specify delimiter to use
   --version                 Show mdbtools version and exit
 
 ```
 
 - - -
 
 ##### mdb-schema
 
 Generate schema creation DDL
 
 ```
 root@kali:~# mdb-schema -h
 Usage:
   mdb-schema [OPTION?] <file> [<backend>] - Dump schema
 
 Help Options:
   -h, --help                    Show help options
 
 Application Options:
   -T, --table=table             Only create schema for named table
   -N, --namespace=namespace     Prefix identifiers with namespace
   --drop-table                  Include DROP TABLE statements
   --no-drop-table               Don't include DROP TABLE statements
   --not-null                    Include NOT NULL constraints
   --no-not-null                 Don't include NOT NULL constraints
   --default-values              Include default values
   --no-default-values           Don't include default values
   --not-empty                   Include not empty constraints
   --no-not_empty                Don't include not empty constraints
   --comments                    Include COMMENT ON statements
   --no-comments                 Don't include COMMENT statements.
   --indexes                     Include indexes
   --no-indexes                  Don't include indexes
   --relations                   Include foreign key constraints
   --no-relations                Don't include foreign key constraints
   --version                     Show mdbtools version and exit
 
 ```
 
 - - -
 
 ##### mdb-sql
 
 SQL interface to MDB Tools
 
 ```
 root@kali:~# mdb-sql -h
 Usage:
   mdb-sql [OPTION?] <file> - Run SQL
 
 Help Options:
   -h, --help                Show help options
 
 Application Options:
   -d, --delim=char          Use this delimiter.
   -P, --no-pretty-print     Don't pretty print
   -H, --no-header           Don't print header
   -F, --no-footer           Don't print footer
   -i, --input=file          Read SQL from specified file
   -o, --output=file         Write result to specified file
   --version                 Show mdbtools version and exit
 
 ```
 
 - - -
 
 ##### mdb-tables
 
 Get listing of tables in an MDB database
 
 ```
 root@kali:~# mdb-tables -h
 Usage:
   mdb-tables [OPTION?] <file> - show MDB files tables/entries
 
 Help Options:
   -h, --help               Show help options
 
 Application Options:
   -S, --system             Include system tables
   -1, --single-column      One table name per line
   -d, --delimiter=char     Table name delimiter
   -t, --type=type          Type of entry
   -T, --showtype           Show type
   --version                Show mdbtools version and exit
 
 ```
 
 - - -
 
 ##### mdb-ver
 
 Return the format of a given MDB database.
 
 ```
 root@kali:~# mdb-ver -h
 Usage:
   mdb-ver [OPTION?] <file> - display MDB file version
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -M, --version     Show mdbtools version and exit
 
 ```
 
 - - -
 
 ### mdbtools-dev
 
  Utilities for reading MS Access database (MDB) files
   
  These are development files for mdbtools, needed to build applications
  with it.
 
 **Installed size:** `283 KB`  
 **How to install:** `sudo apt install mdbtools-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libglib2.0-dev
 * libmdb3 
 * libmdbsql3 
 * odbc-mdbtools 
 {{< /spoiler >}}
 
 
 - - -
 
 ### mdbtools-doc
 
  This is a transitional package. It can safely be removed.
   
  See package libmdb3 documentation.
 
 **Installed size:** `20 KB`  
 **How to install:** `sudo apt install mdbtools-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libmdb3
 {{< /spoiler >}}
 
 
 - - -
 
 ### odbc-mdbtools
 
  This is the software driver to access JET / MS Access database (MDB) files
  through ODBC.
  This also contains the installation interface for unixodbc.
 
 **Installed size:** `99 KB`  
 **How to install:** `sudo apt install odbc-mdbtools`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libglib2.0-0 
 * libmdb3 
 * libmdbsql3 
 * libodbcinst2 
 * odbcinst
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
