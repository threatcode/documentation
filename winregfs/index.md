---
Title: winregfs
Homepage: https://github.com/jbruchon/winregfs
Repository: https://salsa.debian.org/pkg-security-team/winregfs
Architectures: any
Version: 0.7-4
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### winregfs
 
  Winregfs is a FUSE-based filesystem driver that enables accessing of Windows
  registry hive files as ordinary filesystems. Registry hive file editing can
  be performed with ordinary shell scripts and command-line tools once mounted.
   
  fsck.winregfs scans a Windows registry hive file for problems that indicate
  the hive has been damaged by hardware or software issues, reading recursively
  the  key  and  value  data structures in the registry hive.
   
  This package provides mount.winregfs and fsck.winregfs commands.
  Winregfs is useful for pentesters, ethical hackers and forensics experts.
 
 **Installed size:** `102 KB`  
 **How to install:** `sudo apt install winregfs`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfuse2 
 {{< /spoiler >}}
 
 ##### fsck.winregfs
 
 Check a Windows registry file
 
 ```
 root@kali:~# fsck.winregfs -h
 Windows Registry Hive File Checker 0.7 (2017-03-10)
 
 Usage: fsck.winregfs [options] hivename
 
 ```
 
 - - -
 
 ##### mount.winregfs
 
 Windows registry FUSE filesystem
 
 ```
 root@kali:~# mount.winregfs -h
 Windows Registry Filesystem 0.7 (2017-03-10)
 
 Usage: mount.winregfs [-o ro] [fuse_options] hivename mountpoint
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
