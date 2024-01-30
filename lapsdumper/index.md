---
Title: lapsdumper
Homepage: https://github.com/n00py/LAPSDumper
Repository: https://gitlab.com/kalilinux/packages/lapsdumper
Architectures: all
Version: 0+git20221207-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### lapsdumper
 
  A tool that dumps every LAPS password the account
  has the ability to read with a domain.
 
 **Installed size:** `16 KB`  
 **How to install:** `sudo apt install lapsdumper`  
 
 {{< spoiler "Dependencies:" >}}
 * python3-ldap3
 {{< /spoiler >}}
 
 ##### lapsdumper
 
 
 ```
 root@kali:~# lapsdumper -h
 LAPS Dumper - Running at 12-01-2023 09:46:41
 usage: lapsdumper [-h] -u USERNAME -p PASSWORD [-l LDAPSERVER] -d DOMAIN
                   [-c COMPUTER] [-o OUTPUT]
 
 Dump LAPS Passwords
 
 options:
   -h, --help            show this help message and exit
   -u USERNAME, --username USERNAME
                         username for LDAP
   -p PASSWORD, --password PASSWORD
                         password for LDAP (or LM:NT hash)
   -l LDAPSERVER, --ldapserver LDAPSERVER
                         LDAP server (or domain)
   -d DOMAIN, --domain DOMAIN
                         Domain
   -c COMPUTER, --computer COMPUTER
                         Target computer
   -o OUTPUT, --output OUTPUT
                         Output file to CSV
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
