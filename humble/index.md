---
Title: humble
Homepage: https://github.com/rfc-st/humble
Repository: https://gitlab.com/kalilinux/packages/humble
Architectures: all
Version: 1.30-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### humble
 
  This package contains an  humble, and fast, security-oriented HTTP headers
  analyzer.
 
 **Installed size:** `195 KB`  
 **How to install:** `sudo apt install humble`  
 
 {{< spoiler "Dependencies:" >}}
 * publicsuffix
 * python3
 * python3-colorama
 * python3-fpdf
 * python3-requests
 * python3-tldextract
 {{< /spoiler >}}
 
 ##### humble
 
 
 ```
 root@kali:~# humble -h
 usage: humble.py [-h] [-a] [-b] [-f [TERM]] [-g] [-l {es}]
                  [-o {html,json,pdf,txt}] [-r] [-u URL] [-v]
 
 humble (HTTP Headers Analyzer) - https://github.com/rfc-st/humble
 
 options:
   -h, --help              show this help message and exit
   -a                      show statistics of the performed analysis (will be
                           global if '-u URL' is omitted)
   -b                      show a brief analysis (if omitted, a detailed one
                           will be shown)
   -f [TERM]               show fingerprint statistics (will be the Top 20 if
                           "TERM", e.g. "Google", is omitted)
   -g                      show guidelines for securing popular web
                           servers/services
   -l {es}                 show the analysis in the indicated language (if
                           omitted, English will be used)
   -o {html,json,pdf,txt}  save analysis to 'URL_headers_yyyymmdd.ext' file
                           (.json files will contain a brief analysis).
   -r                      show full HTTP response headers and a detailed
                           analysis
   -u URL                  schema and URL to analyze. E.g. https://google.com
   -v, --version           show the version of this tool and check for updates
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
