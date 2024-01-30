---
Title: samdump2
Homepage: http://ophcrack.sourceforge.net/
Repository: https://salsa.debian.org/pkg-security-team/samdump2
Architectures: any
Version: 3.0.0-7
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-passwords kali-tools-respond 
Icon: images/samdump2-logo.svg
PackagesInfo: |
 ### samdump2
 
  This tool is designed to dump Windows 2k/NT/XP password hashes from a SAM
  file, using the syskey bootkey from the system hive.
   
  This package also provides the functionality of bkhive, which recovers the
  syskey bootkey from a Windows NT/2K/XP system hive.
   
  Syskey is a Windows feature that adds an additional encryption layer to the
  password hashes stored in the SAM database.
 
 **Installed size:** `45 KB`  
 **How to install:** `sudo apt install samdump2`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libssl3 
 {{< /spoiler >}}
 
 ##### samdump2
 
 Retrieves syskey and extract hashes from Windows 2k/NT/XP/Vista SAM.
 
 ```
 root@kali:~# samdump2 -h
 samdump2 3.0.0 by Objectif Securite (http://www.objectif-securite.ch)
 original author: ncuomo@studenti.unina.it
 
 Usage: samdump2 [OPTION]... SYSTEM_FILE SAM_FILE
 Retrieves syskey and extract hashes from Windows 2k/NT/XP/Vista SAM
 
   -d		enable debugging
   -h		display this information
   -o file	write output to file
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
