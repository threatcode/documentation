---
Title: scrounge-ntfs
Homepage: http://thewalter.net/stef/software/scrounge/
Repository: https://salsa.debian.org/pkg-security-team/scrounge-ntfs
Architectures: any
Version: 0.9-10
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-recover kali-tools-respond 
Icon: images/scrounge-ntfs-logo.svg
PackagesInfo: |
 ### scrounge-ntfs
 
  Scrounge NTFS is a data recovery program for NTFS filesystems. It reads each
  block of the hard disk and try to rebuild the original filesystem tree into
  a directory.
   
  This package is useful in forensics investigations.
 
 **Installed size:** `50 KB`  
 **How to install:** `sudo apt install scrounge-ntfs`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### scrounge-ntfs
 
 Helps retrieve data from corrupted NTFS partitions
 
 ```
 root@kali:~# scrounge-ntfs --help
 scrounge-ntfs: invalid option -- '-'
 usage: scrounge-ntfs -l disk                                              
   List all drive partition information.                              
                                                                      
 usage: scrounge-ntfs -s disk                                              
   Search drive for NTFS partitions.                                  
                                                                      
 usage: scrounge-ntfs [-m mftoffset] [-c clustersize] [-o outdir] disk start end  
   Scrounge data from a partition                                     
   -m         Offset to mft (in sectors)                              
   -c         Cluster size (in sectors, default of 8)                 
   -o         Directory to put scrounged files in                     
   disk       The raw disk partitios (ie: /dev/hda)                   
   start      First sector of partition                               
   end        Last sector of partition                                
                                                                      
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
