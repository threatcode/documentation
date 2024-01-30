---
Title: ext4magic
Homepage: http://ext4magic.sf.net/ext4magic_en.html
Repository: https://salsa.debian.org/pkg-security-team/ext4magic
Architectures: any
Version: 0.3.2-14
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ext4magic
 
  ext4magic is a file carver (or file carving). It can be used when recovering
  from disasters or in digital forensics activities.
   
  The deletion of files in ext3/4 filesystems can not be easily reversed. Zero
  out of the block references in the inodes makes that impossible. Experiences
  with other programs have proved that is possible restore sufficient information
  for a recover of many data files, directly from the filesystem journal.
   
  ext4magic can extract the information from the journal and restore files in an
  entire directory tree, if the information in the journal are sufficient.
   
  This tool can recover the most file types, with original filename, owner and
  group, file mode bits and also the old atime/mtime stamps.
 
 **Installed size:** `233 KB`  
 **How to install:** `sudo apt install ext4magic`  
 
 {{< spoiler "Dependencies:" >}}
 * libblkid1 
 * libbz2-1.0
 * libc6 
 * libext2fs2 
 * libmagic1 
 * libuuid1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### ext4magic
 
 Recover deleted files on ext3/4 filesystems
 
 ```
 root@kali:~# ext4magic -h
 ext4magic : Error: Missing device name and options.
 
 ext4magic -M [-j <journal_file>] [-d <target_dir>] <filesystem> 
 ext4magic -m [-j <journal_file>] [-d <target_dir>] <filesystem> 
 ext4magic [-S|-J|-H|-V|-T] [-x] [-j <journal_file>] [-B n|-I n|-f <file_name>|-i <input_list>] [-t n|[[-a n][-b n]]] [-d <target_dir>] [-R|-r|-L|-l] [-Q] <filesystem> 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
