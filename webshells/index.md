---
Title: webshells
Homepage: https://www.kali.org
Repository: https://gitlab.com/kalilinux/packages/webshells
Architectures: all
Version: 1.1+kali8
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-web 
Icon: images/webshells-logo.svg
PackagesInfo: |
 ### webshells
 
  A collection of webshells for ASP, ASPX, CFM,
  JSP, Perl, and PHP servers.
 
 **Installed size:** `71 KB`  
 **How to install:** `sudo apt install webshells`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 {{< /spoiler >}}
 
 ##### webshells
 
 
 ```
 root@kali:~# webshells -h
 
 > webshells ~ Collection of webshells
 
 /usr/share/webshells
 |-- asp
 |-- aspx
 |-- cfm
 |-- jsp
 |-- laudanum -> /usr/share/laudanum
 |-- perl
 |-- php
 `-- seclists -> /usr/share/seclists/Web-Shells
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Webshells Usage Examples

```
root@kali:~# tree /usr/share/webshells/
/usr/share/webshells/
├── asp
│   ├── cmd-asp-5.1.asp
│   └── cmdasp.asp
├── aspx
│   └── cmdasp.aspx
├── cfm
│   └── cfexec.cfm
├── jsp
│   ├── cmdjsp.jsp
│   └── jsp-reverse.jsp
├── perl
│   ├── perlcmd.cgi
│   └── perl-reverse-shell.pl
└── php
    ├── findsock.c
    ├── php-backdoor.php
    ├── php-findsock-shell.php
    ├── php-reverse-shell.php
    ├── qsd-php-backdoor.php
    └── simple-backdoor.php

6 directories, 14 files
root@kali:~#
```
