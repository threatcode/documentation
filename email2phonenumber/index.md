---
Title: email2phonenumber
Homepage: https://github.com/martinvigo/email2phonenumber
Repository: https://gitlab.com/kalilinux/packages/email2phonenumber
Architectures: all
Version: 0~git20220216-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### email2phonenumber
 
  This package contains an OSINT tool that allows you to obtain a target's phone
  number just by having their email address.
   
  This tool helps automate discovering someone's phone number by abusing
  password reset design weaknesses and publicly available data. It supports 3
  main functions:
   
     * "scrape" - scrapes websites for phone number digits by initiating
       password reset using the target's email address.
     * "generate" - creates a list of valid phone numbers based on the country's
       Phone Numbering Plan publicly available information.
     * "bruteforce" - iterates over a list of phone numbers and initiates
       password reset on different websites to obtain associated masked emails
       and correlate it to the victim's one.
 
 **Installed size:** `72 KB`  
 **How to install:** `sudo apt install email2phonenumber`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-bs4
 * python3-certifi
 * python3-chardet
 * python3-idna
 * python3-requests
 * python3-soupsieve
 * python3-urllib3
 {{< /spoiler >}}
 
 ##### email2phonenumber
 
 
 ```
 root@kali:~# email2phonenumber -h
 usage: email2phonenumber.py [-h] {scrape,generate,bruteforce} ...
 
 An OSINT tool to find phone numbers associated to email addresses
 
 positional arguments:
   {scrape,generate,bruteforce}
                         commands
     scrape              scrape online services for phone number digits
     generate            generate all valid phone numbers based on NANPA's
                         public records
     bruteforce          bruteforce using online services to find the phone
                         number
 
 options:
   -h, --help            show this help message and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
