---
Title: rifiuti
Homepage: https://sf.net/projects/odessa
Repository: https://salsa.debian.org/pkg-security-team/rifiuti
Architectures: any
Version: 20040505-4
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rifiuti
 
  Rifiuti is a tool to examine the INFO2 files. The INFO2 file gives meta
  information about the files found in the MS Windows recycle bin.
   
  This package is useful in forensics investigations.
 
 **Installed size:** `30 KB`  
 **How to install:** `sudo apt install rifiuti`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### rifiuti
 
 Tool to extract information from MS recycle bins info2 files.
 
 ```
 root@kali:~# rifiuti -h
 INFO2 File: -h
 
 ERROR - The INFO2 file cannot be opened!
 
 
 Usage:  rifiuti [options] <filename>
 	-d Field Delimiter (TAB by default)
 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
