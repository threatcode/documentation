---
Title: sqlitebrowser
Homepage: https://sqlitebrowser.org/
Repository: https://salsa.debian.org/sqlitebrowser-team/sqlitebrowser
Architectures: any
Version: 3.12.2-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-database kali-tools-forensics kali-tools-respond kali-tools-web 
Icon: images/sqlitebrowser-logo.svg
PackagesInfo: |
 ### sqlitebrowser
 
  SQLite Database Browser is a visual tool used to create, design and edit
  database files compatible with SQLite. Its interface is based on QT,
  and is meant to be used for users and developers that want to create
  databases, edit and search data using a familiar spreadsheet-like
  interface, without the need to learn complicated SQL commands.
  Controls and wizards are available for users to:
   - Create and compact database files
   - Create, define, modify and delete tables
   - Create, define and delete indexes
   - Browse, edit, add and delete records
   - Search records
   - Import and export records as text
   - Import and export tables from/to CSV files
   - Import and export databases from/to SQL dump files
   - Issue SQL queries and inspect the results
   - Examine a log of all SQL commands issued by the application
   
  SQLite Database Browser is not a visual shell for the sqlite command line
  tool. It does not require familiarity with SQL commands.
 
 **Installed size:** `5.78 MB`  
 **How to install:** `sudo apt install sqlitebrowser`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libqscintilla2-qt5-15 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5printsupport5 
 * libqt5widgets5 
 * libqt5xml5 
 * libsqlite3-0 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### sqlitebrowser
 
 Light GUI editor for SQLite databases
 
 ```
 root@kali:~# man sqlitebrowser
 SQLITEBROWSER(1)            General Commands Manual           SQLITEBROWSER(1)
 
 NAME
        sqlitebrowser - light GUI editor for SQLite databases
 
 SYNOPSIS
        sqlitebrowser [file]
 
 DESCRIPTION
        SQLite  Database  Browser  is  a visual tool used to create, design and
        edit database files compatible with SQLite. It is meant to be used  for
        users  and  developers  that  want to create databases, edit and search
        data using a familiar spreadsheet-like interface, without the  need  to
        learn complicated SQL commands.
 
 SEE ALSO
        SQLitebrowser's home page: http://sqlitebrowser.sourceforge.net/.
 
 AUTHOR
        sqlitebrowser was developed originally by Mauricio Piacentini from Tab-
        uleiro  Producoes. Icons were contributed by Raquel Ravanini, also from
        Tabuleiro. Jens Miltner contributed the  code  to  support  SQLite  3.x
        databases for the 1.2 release.
        In the spirit of the original SQLite source files, the authors disclaim
        copyright  to  this  source code. It may be used as the basis for other
        programs, public domain, open source or  commercial.  Do  whatever  you
        want with it.
 
        This  manual page was written by Francois Fevotte <francois.fevotte@en-
        sta.org>, for the Debian project (but may be used by others).
        Permission is granted to copy, distribute and/or modify  this  document
        under  the  terms  of  the GNU General Public License, Version 2 or any
        later version published by the Free Software Foundation.
        On Debian systems, the complete text of the GNU General Public  License
        can be found in /usr/share/common-licenses/GPL.
 
                                 August  4, 2007               SQLITEBROWSER(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
