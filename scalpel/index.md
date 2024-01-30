---
Title: scalpel
Homepage: http://www.digitalforensicssolutions.com/Scalpel
Repository: https://salsa.debian.org/pkg-security-team/scalpel
Architectures: any
Version: 1.60-10
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/scalpel-logo.svg
PackagesInfo: |
 ### scalpel
 
  scalpel is a fast file carver that reads a database of header and footer
  definitions and extracts matching files from a set of image files or raw
  device files.
   
  scalpel is filesystem-independent and will carve files from FAT16, FAT32,
  exFAT, NTFS, Ext2, Ext3, Ext4, JFS, XFS, ReiserFS, raw partitions, etc.
   
  scalpel is a complete rewrite of the Foremost 0.69 file carver and is
  useful for both digital forensics investigations and file recovery.
 
 **Installed size:** `88 KB`  
 **How to install:** `sudo apt install scalpel`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### scalpel
 
 Recover files using a header/footer database
 
 ```
 root@kali:~# scalpel -h
 Scalpel version 1.60
 Written by Golden G. Richard III, based on Foremost 0.69.
 Carves files from a disk image based on file headers and footers.
 
 Usage: scalpel [-b] [-c <config file>] [-d] [-h|V] [-i <file>]
                  [-m blocksize] [-n] [-o <outputdir>] [-O num] [-q clustersize]
                  [-r] [-s num] [-t <blockmap file>] [-u] [-v]
                  <imgfile> [<imgfile>] ...
 
 -b  Carve files even if defined footers aren't discovered within
     maximum carve size for file type [foremost 0.69 compat mode].
 -c  Choose configuration file.
 -d  Generate header/footer database; will bypass certain optimizations
     and discover all footers, so performance suffers.  Doesn't affect
     the set of files carved.  **EXPERIMENTAL**
 -h  Print this help message and exit.
 -i  Read names of disk images from specified file.
 -m  Generate/update carve coverage blockmap file.  The first 32bit
     unsigned int in the file identifies the block size. Thereafter
     each 32bit unsigned int entry in the blockmap file corresponds
     to one block in the image file.  Each entry counts how many
     carved files contain this block. Requires more memory and
     disk.  **EXPERIMENTAL**
 -n  Don't add extensions to extracted files.
 -o  Set output directory for carved files.
 -O  Don't organize carved files by type. Default is to organize carved files
     into subdirectories.
 -p  Perform image file preview; audit log indicates which files
     would have been carved, but no files are actually carved.
 -q  Carve only when header is cluster-aligned.
 -r  Find only first of overlapping headers/footers [foremost 0.69 compat mode].
 -s  Skip n bytes in each disk image before carving.
 -t  Set directory for coverage blockmap.  **EXPERIMENTAL**
 -u  Use carve coverage blockmap when carving.  Carve only sections
     of the image whose entries in the blockmap are 0.  These areas
     are treated as contiguous regions.  **EXPERIMENTAL**
 -V  Print copyright information and exit.
 -v  Verbose mode.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
