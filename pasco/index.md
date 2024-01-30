---
Title: pasco
Homepage: https://sf.net/projects/odessa
Repository: https://salsa.debian.org/pkg-security-team/pasco
Architectures: any
Version: 20040505-4
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pasco
 
  Pasco is a forensic tool that examines the content of cache files (index.dat)
  produced by Microsoft Internet Explorer.
   
  It parses the file and outputs a field separated that can be loaded in a
  spreadsheet.
   
  This package is useful in forensics investigations.
 
 **Installed size:** `34 KB`  
 **How to install:** `sudo apt install pasco`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### pasco
 
 Tool to extract information from MS IE cache files
 
 ```
 root@kali:~# pasco -h
 ERROR - The index.dat file cannot be opened!
 
 
 Usage:  pasco [options] <filename>
 	-d Undelete Activity Records
 	-t Field Delimiter (TAB by default)
 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
