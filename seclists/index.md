---
Title: seclists
Homepage: https://github.com/danielmiessler/SecLists
Repository: https://gitlab.com/kalilinux/packages/seclists
Architectures: all
Version: 2023.4-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### seclists
 
  SecLists is a collection of multiple types of lists used during security
  assessments. List types include usernames, passwords, URLs, sensitive data grep
  strings, fuzzing payloads, and many more.
   
  The goal is to enable a security tester to pull this repo onto a new testing
  box and have access to every type of list that may be needed.
 
 **Installed size:** `1.73 GB`  
 **How to install:** `sudo apt install seclists`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 {{< /spoiler >}}
 
 ##### seclists
 
 
 ```
 root@kali:~# seclists -h
 
 > seclists ~ Collection of multiple types of security lists
 
 /usr/share/seclists
 |-- Discovery
 |-- Fuzzing
 |-- IOCs
 |-- Miscellaneous
 |-- Passwords
 |-- Pattern-Matching
 |-- Payloads
 |-- Usernames
 `-- Web-Shells
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## SecLists Usage Examples

```
root@kali:~# ls -lh /usr/share/seclists/
total 40K
drwxr-xr-x  6 root root 4.0K Mar 23 09:56 Discovery
drwxr-xr-x  3 root root 4.0K Mar 23 09:56 Fuzzing
drwxr-xr-x  2 root root 4.0K Mar 23 09:56 IOCs
drwxr-xr-x  2 root root 4.0K Mar 23 09:56 Miscellaneous
drwxr-xr-x 11 root root 4.0K Mar 23 09:56 Passwords
drwxr-xr-x  2 root root 4.0K Mar 23 09:56 Pattern-Matching
drwxr-xr-x  7 root root 4.0K Mar 23 09:56 Payloads
-rwxr-xr-x  1 root root 3.5K Mar  7 16:02 README.md
drwxr-xr-x  4 root root 4.0K Mar 23 09:56 Usernames
drwxr-xr-x  7 root root 4.0K Mar 23 09:56 Web-Shells
root@kali:~#
root@kali:~# tree -d /usr/share/seclists/
/usr/share/seclists/
├── Discovery
│   ├── DNS
│   ├── Infrastructure
│   ├── SNMP
│   └── Web-Content
│       ├── CMS
│       ├── SVNDigger
│       │   ├── cat
│       │   │   ├── Conf
│       │   │   ├── Database
│       │   │   ├── Language
│       │   │   └── Project
│       │   └── context
│       ├── URLs
│       └── Web-Services
├── Fuzzing
│   └── Polyglots
├── IOCs
├── Miscellaneous
├── Passwords
│   ├── Common-Credentials
│   ├── Cracked-Hashes
│   ├── Default-Credentials
│   ├── Honeypot-Captures
│   ├── Leaked-Databases
│   ├── Malware
│   ├── Permutations
│   ├── Software
│   └── WiFi-WPA
├── Pattern-Matching
├── Payloads
│   ├── Anti-Virus
│   ├── File-Names
│   ├── Images
│   ├── PHPInfo
│   └── Zip-Bombs
├── Usernames
│   ├── Honeypot-Captures
│   └── Names
└── Web-Shells
    ├── FuzzDB
    ├── JSP
    ├── laudanum-0.8
    │   ├── asp
    │   ├── aspx
    │   ├── cfm
    │   ├── jsp
    │   │   └── warfiles
    │   │       ├── META-INF
    │   │       └── WEB-INF
    │   └── php
    ├── PHP
    └── WordPress

53 directories
root@kali:~#
```
