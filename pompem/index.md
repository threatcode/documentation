---
Title: pompem
Homepage: https://github.com/rfunix/Pompem
Repository: https://salsa.debian.org/pkg-security-team/pompem
Architectures: all
Version: 0.2.0-6
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pompem
 
  Find exploit with a system of advanced search, designed to automate the search
  for Exploits and Vulnerability in the most important databases facilitating
  the work of pentesters, ethical hackers and forensics expert. Performs searches
  in databases: PacketStorm security, CXSecurity, ZeroDay, Vulners, National
  Vulnerability Database, WPScan Vulnerability Database. This tool is essential
  in the security of networks and systems.
   
  The search results can be exported to HTML or text format.
 
 **Installed size:** `51 KB`  
 **How to install:** `sudo apt install pompem`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-requests
 {{< /spoiler >}}
 
 ##### pompem
 
 Exploit and Vulnerability Finder
 
 ```
 root@kali:~# pompem -h
 
 Options:
   -h, --help                      show this help message and exit
   -s, --search <keyword,keyword,keyword>  text for search
   --txt                           Write txt File
   --html                          Write html File
   --update                        upgrade to latest version
   -g, --get                       Download exploit files
               
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
