---
Title: sqlsus
Homepage: https://sqlsus.sourceforge.net/
Repository: https://gitlab.com/kalilinux/packages/sqlsus
Architectures: all
Version: 0.7.2-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-database kali-tools-web 
Icon: images/sqlsus-logo.svg
PackagesInfo: |
 ### sqlsus
 
  sqlsus is an open source MySQL injection and takeover tool,
  written in perl.
  Via a command line interface, you can retrieve the
  database(s) structure, inject your own SQL queries (even
  complex ones), download files from the web server, crawl
  the website for writable directories, upload and control a
  backdoor, clone the database(s), and much more...
  Whenever relevant, sqlsus will mimic a MySQL console output.
 
 **Installed size:** `156 KB`  
 **How to install:** `sudo apt install sqlsus`  
 
 {{< spoiler "Dependencies:" >}}
 * libdbd-sqlite3-perl
 * libhtml-linkextractor-perl
 * liblwp-protocol-socks-perl
 * libterm-readline-gnu-perl
 * libwww-perl
 * perl
 * sqlite3
 {{< /spoiler >}}
 
 ##### sqlsus
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## sqlsus Usage Example

Generate a configuration file for the scan (`-g sqlsus.cfg`):

```
root@kali:~# sqlsus -g sqlsus.cfg

              sqlsus version 0.7.2

  Copyright (c) 2008-2011 Jérémy Ruffet (sativouf)

[+] Configuration successfully saved to sqlsus.cfg
root@kali:~# nano sqlsus.cfg
```

```
root@kali:~# sqlsus sqlsus.cfg

              sqlsus version 0.7.2

  Copyright (c) 2008-2011 Jérémy Ruffet (sativouf)

[+] Session "192.168.1.25" created
sqlsus> start
```
