---
Title: dscan
Homepage: https://github.com/0x4E0x650x6F/dscan
Repository: https://gitlab.com/kalilinux/packages/dscan
Architectures: all
Version: 0.1.5-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dscan
 
  This package provides a wrapper around nmap, and distribute scans across
  several hosts.
  It aggregates / splits address ranges, uses a configuration file where scan
  configuration can be adjusted, supports resume.
 
 **Installed size:** `95 KB`  
 **How to install:** `sudo apt install dscan`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-libnmap
 {{< /spoiler >}}
 
 ##### dscan
 
 
 ```
 root@kali:~# dscan -h
 [*] Distributed scan
 usage: Distributed scanner [-h] --name NAME {srv,agent,config} ...
 
 positional arguments:
   {srv,agent,config}
 
 options:
   -h, --help          show this help message and exit
   --name NAME
 ```
 
 - - -
 
 ### dscan-doc
 
  This package provides a wrapper around nmap, and distribute scans across
  several hosts.
  It aggregates / splits address ranges, uses a configuration file where scan
  configuration can be adjusted, supports resume.
   
  This is the documentation package.
 
 **Installed size:** `483 KB`  
 **How to install:** `sudo apt install dscan-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-sphinxdoc 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
