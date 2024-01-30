---
Title: testdisk
Homepage: 
Repository: 
Architectures: any
Version: 7.1-5+nmu1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### testdisk
 
  TestDisk checks the partition and boot sectors of your disks.
  It is very useful in forensics, recovering lost partitions.
  It works with :
   * DOS/Windows FAT12, FAT16 and FAT32
   * NTFS ( Windows NT/2K/XP )
   * Linux Ext2 and Ext3
   * BeFS ( BeOS )
   * BSD disklabel ( FreeBSD/OpenBSD/NetBSD )
   * CramFS (Compressed File System)
   * HFS and HFS+, Hierarchical File System
   * JFS, IBM's Journaled File System
   * Linux Raid
   * Linux Swap (versions 1 and 2)
   * LVM and LVM2, Linux Logical Volume Manager
   * Netware NSS
   * ReiserFS 3.5 and 3.6
   * Sun Solaris i386 disklabel
   * UFS and UFS2 (Sun/BSD/...)
   * XFS, SGI's Journaled File System
   
  PhotoRec is file data recovery software designed to recover
  lost pictures from digital camera memory or even Hard Disks.
  It has been extended to search also for non audio/video headers.
  It searches for following files and is able to undelete them:
   * Sun/NeXT audio data (.au)
   * RIFF audio/video (.avi/.wav)
   * BMP bitmap (.bmp)
   * bzip2 compressed data (.bz2)
   * Source code written in C (.c)
   * Canon Raw picture (.crw)
   * Canon catalog (.ctg)
   * FAT subdirectory
   * Microsoft Office Document (.doc)
   * Nikon dsc (.dsc)
   * HTML page (.html)
   * JPEG picture (.jpg)
   * MOV video (.mov)
   * MP3 audio (MPEG ADTS, layer III, v1) (.mp3)
   * Moving Picture Experts Group video (.mpg)
   * Minolta Raw picture (.mrw)
   * Olympus Raw Format picture (.orf)
   * Portable Document Format (.pdf)
   * Perl script (.pl)
   * Portable Network Graphics (.png)
   * Raw Fujifilm picture (.raf)
   * Contax picture (.raw)
   * Rollei picture (.rdc)
   * Rich Text Format (.rtf)
   * Shell script (.sh)
   * Tar archive (.tar )
   * Tag Image File Format (.tiff)
   * Microsoft ASF (.wma)
   * Sigma/Foveon X3 raw picture (.x3f)
   * zip archive (.zip)
 
 **Installed size:** `1.37 MB`  
 **How to install:** `sudo apt install testdisk`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libext2fs2 
 * libjpeg62-turbo 
 * libncursesw6 
 * libntfs-3g89
 * libtinfo6 
 * libuuid1 
 * ntfs-3g
 * zlib1g 
 {{< /spoiler >}}
 
 ##### fidentify
 
 Determine file type using PhotoRec database
 
 ```
 root@kali:~# fidentify -h
 
 Usage: fidentify [--check] [+file_format] [directory|file]
        fidentify --version
 
 fidentify determines the file type, the 'extension', by using the same database as PhotoRec.
 By default, all known file formats are searched unless one is specifically enabled.
 ```
 
 - - -
 
 ##### photorec
 
 Recover lost files from harddisk, digital camera and cdrom
 
 ```
 root@kali:~# photorec -h
 PhotoRec 7.1, Data Recovery Utility, July 2019
 Christophe GRENIER <grenier@cgsecurity.org>
 https://www.cgsecurity.org
 
 Usage: photorec [/log] [/debug] [/d recup_dir] [file.dd|file.e01|device]
        photorec /version
 
 /log          : create a photorec.log file
 /debug        : add debug information
 
 PhotoRec searches for various file formats (JPEG, Office...). It stores files
 in the recup_dir directory.
 ```
 
 - - -
 
 ##### testdisk
 
 Scan and repair disk partitions
 
 ```
 root@kali:~# testdisk -h
 TestDisk 7.1, Data Recovery Utility, July 2019
 Christophe GRENIER <grenier@cgsecurity.org>
 https://www.cgsecurity.org
 
 Usage: testdisk [/log] [/debug] [file.dd|file.e01|device]
        testdisk /list  [/log]   [file.dd|file.e01|device]
        testdisk /version
 
 /log          : create a testdisk.log file
 /debug        : add debug information
 /list         : display current partitions
 
 TestDisk checks and recovers lost partitions
 It works with :
 - BeFS (BeOS)                           - BSD disklabel (Free/Open/Net BSD)
 - CramFS, Compressed File System        - DOS/Windows FAT12, FAT16 and FAT32
 - XBox FATX                             - Windows exFAT
 - HFS, HFS+, Hierarchical File System   - JFS, IBM's Journaled File System
 - Linux btrfs                           - Linux ext2, ext3 and ext4
 - Linux GFS2                            - Linux LUKS
 - Linux Raid                            - Linux Swap
 - LVM, LVM2, Logical Volume Manager     - Netware NSS
 - Windows NTFS                          - ReiserFS 3.5, 3.6 and 4
 - Sun Solaris i386 disklabel            - UFS and UFS2 (Sun/BSD/...)
 - XFS, SGI's Journaled File System      - Wii WBFS
 - Sun ZFS
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
