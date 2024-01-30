---
Title: missidentify
Homepage: http://missidentify.sf.net
Repository: https://salsa.debian.org/pkg-security-team/missidentify
Architectures: any
Version: 1.0-11
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### missidentify
 
  Miss Identify (missidentify) is a program to find MS Windows type win32
  applications. By default, it displays the filename of any executable that
  does not have an extension, as exe, dll, com, sys, cpl, hxs, hxi, olb, rll
  or tlb. It can also display all the executables regardless the extension.
   
  Miss Identify is useful in forensics investigations.
 
 **Installed size:** `43 KB`  
 **How to install:** `sudo apt install missidentify`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### missidentify
 
 Find executable files without an executable extension
 
 ```
 root@kali:~# missidentify -h
 missidentify version 1.0 by Jesse Kornblum
 Usage: missidentify [-Vh] [-rablv] [-s|-S len] [FILES]
 
 -r  Recursive mode. All subdirectories are traversed
 -q  Silent mode. No error messages are displayed
 -a  Display all executable files regardless of extension
 -b  Bare filename. No path information displayed
 -l  Relative paths in filenames
 -v  Verbose mode. Displays the filename for every 10th file processed
 -s|-S Display strings
 -V  Display version number and exit
 -h  Display this help message
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
