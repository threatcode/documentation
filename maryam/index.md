---
Title: maryam
Homepage: https://github.com/saeeddhqan/Maryam
Repository: https://gitlab.com/kalilinux/packages/maryam
Architectures: all
Version: 2.5.0-0kali2
Metapackages: kali-linux-everything kali-tools-identify 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### maryam
 
  This package contains the OWASP Maryam, a modular/optional open source
  framework based on OSINT and data gathering. Maryam is written in Python
  programming language and it’s designed to provide a powerful environment to
  harvest data from open sources and search engines and collect data quickly and
  thoroughly.
 
 **Installed size:** `1.08 MB`  
 **How to install:** `sudo apt install maryam`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-bs4
 * python3-cloudscraper
 * python3-flask
 * python3-lxml
 * python3-matplotlib
 * python3-nltk
 * python3-pandas
 * python3-plotly
 * python3-requests
 * python3-vadersentiment
 {{< /spoiler >}}
 
 ##### maryam
 
 
 ```
 root@kali:~# maryam -h
 usage: maryam [-h] [-e execute] [-s start] [-v]
 maryam -h
 
 optional arguments:
 	  -h, --help   show this help message and exit
 	  -e execute   execute a command and exit
 	  -s start     run a command without exit
 	  -v           show version and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
