---
Title: autopsy
Homepage: https://www.sleuthkit.org/autopsy/
Repository: https://salsa.debian.org/debian/autopsy
Architectures: all
Version: 2.24-5
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/autopsy-logo.svg
PackagesInfo: |
 ### autopsy
 
  The Autopsy Forensic Browser is a graphical interface to the command line
  digital forensic analysis tools in The Sleuth Kit. Together, The Sleuth Kit
  and Autopsy provide many of the same features as commercial digital forensics
  tools for the analysis of Windows and UNIX file systems (NTFS, FAT, FFS,
  EXT2FS, and EXT3FS).
 
 **Installed size:** `1.00 MB`  
 **How to install:** `sudo apt install autopsy`  
 
 {{< spoiler "Dependencies:" >}}
 * binutils
 * perl
 * sleuthkit 
 {{< /spoiler >}}
 
 ##### autopsy
 
 Autopsy Forensic Browser
 
 ```
 root@kali:~# autopsy -h
 Invalid flag: -h
 
 
 usage: /usr/bin/autopsy [-c] [-C] [-d evid_locker] [-i device filesystem mnt] [-p port] [remoteaddr]
   -c: force a cookie in the URL
   -C: force NO cookie in the URL
   -d dir: specify the evidence locker directory
   -i device filesystem mnt: Specify info for live analysis
   -p port: specify the server port (default: 9999)
   remoteaddr: specify the host with the browser (default: localhost)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
