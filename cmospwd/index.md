---
Title: cmospwd
Homepage: https://www.cgsecurity.org/wiki/CmosPwd
Repository: https://gitlab.com/kalilinux/packages/cmospwd
Architectures: amd64 i386
Version: 5.0+dfsg-3kali5
Metapackages: kali-linux-everything kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cmospwd
 
  CmosPwd is a cross-platform tool to decrypt password stored in CMOS used
  to access a computer's BIOS setup.
   
  This application should work out of the box on most modern systems, but
  some more esoteric BIOSes may not be supported or may require additional
  steps.
 
 **Installed size:** `65 KB`  
 **How to install:** `sudo apt install cmospwd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### cmospwd
 
 A cmos/bios password recovery tool
 
 ```
 root@kali:~# cmospwd -h
 CmosPwd - BIOS Cracker 5.0, October 2007, Copyright 1996-2007
 GRENIER Christophe, grenier@cgsecurity.org
 http://www.cgsecurity.org/
 
 Usage: cmospwd [/k[de|fr]] [/d]
        cmospwd [/k[de|fr]] [/d] /[wlr] cmos_backup_file           write/load/restore
        cmospwd /k                                          kill cmos
        cmospwd [/k[de|fr]] /m[01]*	execute selected module
 
  /kfr french AZERTY keyboard, /kde german QWERTZ keyboard
  /d to dump cmos
  /m0010011 to execute module 3,6 and 7
 
 NB: For Award BIOS, passwords are differents than original, but work.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
