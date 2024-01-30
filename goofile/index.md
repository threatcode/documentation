---
Title: goofile
Homepage: https://github.com/sosukeinu/goofile
Repository: https://gitlab.com/kalilinux/packages/goofile
Architectures: all
Version: 1.6+git20190819-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### goofile
 
  Use this tool to search for a specific file type in a given domain.
 
 **Installed size:** `37 KB`  
 **How to install:** `sudo apt install goofile`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-requests
 {{< /spoiler >}}
 
 ##### goofile
 
 
 ```
 root@kali:~# goofile -h
 usage: goofile [-h] [-d DOMAIN] [-f FILETYPE] [-k KEY] [-e ENGINE] [-q QUERY]
                [--logging LOGGING]
 
 options:
   -h, --help            show this help message and exit
   -d DOMAIN, --domain DOMAIN
                         the domain to search - optional (ie. kali.org
   -f FILETYPE, --filetype FILETYPE
                         the filetype to search for - required (ie. pdf)
   -k KEY, --key KEY     Google Custom Search Engine API key - optional
   -e ENGINE, --engine ENGINE
                         Google Custom Search Engine ID - optional
   -q QUERY, --query QUERY
                         Only search for files with keyword - optional
   --logging LOGGING     Set the logging verbosity to something other than
                         "INFO" - optional
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/31264.js" id="asciicast-31264" async></script>

## goofile Usage Example

Search for files from a domain (`-d kali.org`) of the PDF filetype (`-f pdf)`:

```
root@kali:~# goofile -d kali.org -f pdf

-------------------------------------
|Goofile v1.5                       |
|Coded by Thomas (G13) Richards     |
|www.g13net.com                     |
|code.google.com/p/goofile          |
-------------------------------------


Searching in kali.org for pdf
========================================

Files found:
====================

docs.kali.org/pdf/kali-book-fr.pdf
docs.kali.org/pdf/kali-book-es.pdf
docs.kali.org/pdf/kali-book-id.pdf
docs.kali.org/pdf/kali-book-de.pdf
docs.kali.org/pdf/kali-book-it.pdf
docs.kali.org/pdf/kali-book-ar.pdf
docs.kali.org/pdf/kali-book-ja.pdf
docs.kali.org/pdf/kali-book-nl.pdf
docs.kali.org/pdf/kali-book-ru.pdf
docs.kali.org/pdf/kali-book-en.pdf
docs.kali.org/pdf/kali-book-pt-br.pdf
docs.kali.org/pdf/kali-book-zh-hans.pdf
docs.kali.org/pdf/kali-book-sw.pdf
docs.kali.org/pdf/articles/kali-linux-live-usb-install-en.pdf
====================
```
