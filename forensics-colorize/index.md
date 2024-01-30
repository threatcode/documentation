---
Title: forensics-colorize
Homepage: https://github.com/jessek/colorize
Repository: https://salsa.debian.org/pkg-security-team/forensics-colorize
Architectures: any
Version: 1.1-7
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### forensics-colorize
 
  forensics-colorize is a set of tools to visually compare large files, as
  filesystem images, creating graphics of them. It is intuitive because the
  produced graphics provide a quick and perfect sense about the percentage
  of changes between two files.
   
  Comparing large textual files using a simple diff can produce a very big
  result in lines, causing confusion. On the other hand, diff is improper
  to compare binary files.
   
  This package provides two command line programs: filecompare and colorize.
  The filecompare command is used to create a special and auxiliary input
  file for colorize. The colorize command will generate an intuitive graphic
  that will make easier to perceive the level of changes between the files.
 
 **Installed size:** `2.05 MB`  
 **How to install:** `sudo apt install forensics-colorize`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### colorize
 
 Show differences between files using color graphics
 
 ```
 root@kali:~# colorize -h
 colorize by Jesse Kornblum version 1.1
 $ colorize [-h|-V] [-w <num>] [-ovd] FILES
 
 -d  - Change direction data flows, defaults to down or right
 -o  - Change image orientation, defaults to vertical
 -v  - Verbose mode
 -w  - Set output image width, defaults to 100
 -V  - Display version number and exit
 -h  - Display this help message and exit
 ```
 
 - - -
 
 ##### filecompare
 
 Show differences between files using color graphics
 
 ```
 root@kali:~# filecompare -h
 filecompare version 1.1 by Jesse Kornblum
 Usage: filecompare [-b size[bkmgpe]] [-Vh] FILE1 FILE2
 
 -b  Set block size with optional suffix b,k,m,g,p, or e
     Note that the program will output at least one complete block
     Make sure you have enough disk space!
 -t  Use transitional colors instead of default red or green
 -V  Display version number and exit
 -h  Display this help message
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
