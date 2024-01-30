---
Title: mac-robber
Homepage: https://www.sleuthkit.org/mac-robber
Repository: https://salsa.debian.org/pkg-security-team/mac-robber
Architectures: any
Version: 1.02-13
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### mac-robber
 
  mac-robber is a digital investigation tool (digital forensics) that collects
  metadata from allocated files in a mounted filesystem. This is useful during
  incident response when analyzing a live system or when analyzing a dead
  system in a lab. The data can be used by the mactime tool in The Sleuth Kit
  (TSK or SleuthKit only) to make a timeline of file activity. The mac-robber
  tool is based on the grave-robber tool from TCT (The Coroners Toolkit).
   
  mac-robber requires that the filesystem be mounted by the operating system,
  unlike the tools in The Sleuth Kit that process the filesystem themselves.
  Therefore, mac-robber will not collect data from deleted files or files that
  have been hidden by rootkits. mac-robber will also modify the Access times
  on directories that are mounted with write permissions.
   
  mac-robber is useful when dealing with a filesystem that is not supported
  by The Sleuth Kit or other filesystem analysis tools. You can run mac-robber
  on an obscure, suspect UNIX filesystem that has been mounted read-only on a
  trusted system.
 
 **Installed size:** `35 KB`  
 **How to install:** `sudo apt install mac-robber`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### mac-robber
 
 Collects data about allocated files in mounted filesystems
 
 ```
 root@kali:~# mac-robber -h
 usage: mac-robber [-V] <directories>
   -V: Print the version to stdout
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
