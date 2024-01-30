---
Title: hosthunter
Homepage: https://github.com/SpiderLabs/HostHunter
Repository: https://gitlab.com/kalilinux/packages/hosthunter
Architectures: all
Version: 1.6-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hosthunter
 
  This package contains a tool to efficiently discover and extract hostnames
  providing a large set of target IP addresses. HostHunter utilises simple OSINT
  techniques to map IP addresses with virtual hostnames. It generates a CSV or
  TXT file containing the results of the reconnaissance.
   
  Latest version of HostHunter also takes screenshots of the targets, it is
  currently a beta functionality.
 
 **Installed size:** `33 KB`  
 **How to install:** `sudo apt install hosthunter`  
 
 {{< spoiler "Dependencies:" >}}
 * chromium-driver
 * python3
 * python3-fake-useragent 
 * python3-openssl
 * python3-requests
 * python3-selenium
 * python3-urllib3
 {{< /spoiler >}}
 
 ##### hosthunter
 
 
 ```
 root@kali:~# hosthunter -h
 usage: hosthunter [-h] [-f FORMAT] [-o OUTPUT] [-sc] [-t TARGET] [-V]
                   [targets]
 
 [?] HostHunter v1.6 - Help Page
 
 positional arguments:
   targets               Sets the path of the target IPs file.
 
 options:
   -h, --help            show this help message and exit
   -f FORMAT, --format FORMAT
                         Choose between CSV and TXT output file formats.
   -o OUTPUT, --output OUTPUT
                         Sets the path of the output file.
   -sc, --screen-capture
                         Capture a screenshot of any associated Web
                         Applications.
   -t TARGET, --target TARGET
                         Scan a Single IP.
   -V, --version         Displays the current version.
 
 Author: Andreas Georgiou (@superhedgy)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
