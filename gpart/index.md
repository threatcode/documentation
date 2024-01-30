---
Title: gpart
Homepage: https://github.com/baruch/gpart
Repository: https://salsa.debian.org/pkg-security-team/gpart
Architectures: any
Version: 1:0.3-10
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gpart
 
  Gpart is a tool which tries to guess the primary partition table of a PC-type
  disk in case the primary partition table in sector 0 is damaged, incorrect or
  deleted.
   
  It is also good at finding and listing the types, locations, and sizes of
  inadvertently-deleted partitions, both primary and logical. It gives you the
  information you need to manually re-create them (using fdisk, cfdisk, sfdisk,
  etc.).
   
  The guessed table can also be written to a file or (if you firmly believe the
  guessed table is entirely correct) directly to a disk device.
   
  Currently supported (guessable) filesystem or partition types:
   
   * BeOS filesystem type.
   * BtrFS filesystem type.
   * FreeBSD/NetBSD/386BSD disklabel sub-partitioning scheme used on Intel
     platforms.
   * Linux second extended filesystem (Ext2).
   * MS-DOS FAT12, FAT16 and FAT32 "filesystems".
   * IBM OS/2 High Performance filesystem.
   * Linux LVM and LVM2 physical volumes.
   * Linux swap partitions (versions 0 and 1).
   * The Minix operating system filesystem type.
   * MS Windows NT/2000 filesystem.
   * QNX 4.x filesystem.
   * The Reiser filesystem (version 3.5.X, X > 11).
   * Sun Solaris on Intel platforms uses a sub-partitioning scheme on PC hard
     disks similar to the BSD disklabels.
   * Silicon Graphics journaled filesystem for Linux.
   
  Gpart is useful in recovery actions and forensics investigations.
 
 **Installed size:** `76 KB`  
 **How to install:** `sudo apt install gpart`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### gpart
 
 Guess PC-type hard disk partitions
 
 ```
 root@kali:~# gpart --help
 gpart: invalid option -- '-'
 Usage: gpart [options] device
 Options: [-b <backup MBR>][-C c,h,s][-c][-d][-E][-e][-f][-g][-h][-i]
          [-K <last sector>][-k <# of sectors>][-L][-l <log file>]
          [-n <increment>][-q][-s <sector-size>]
          [-V][-v][-W <device>][-w <module-name,weight>]
 gpart v0.2.3-dev (c) 1999-2001 Michail Brzitwa <michail@brzitwa.de>.
 Guess PC-type hard disk partitions.
 
 Options:
  -b  Save a backup of the original MBR to specified file.
  -C  Set c/h/s to be used in the scan.
  -c  Check/compare mode.
  -d  Do not start the guessing loop.
  -E  Do not try to identify extended partition tables.
  -e  Do not skip disk read errors.
  -f  Full scan.
  -g  Do not try to get the disk geometry.
  -h  Show this help.
  -i  Run interactively (ask for confirmation).
  -K  Scan only up to given sector.
  -k  Skip sectors before scan.
  -L  List available modules and their weights, then exit.
  -l  Logfile name.
  -n  Scan increment: number or 's' sector, 'h' head, 'c' cylinder.
  -q  Run quiet (however log file is written if specified).
  -s  Sector size to use (disable sector size probing).
  -V  Show version.
  -v  Verbose mode. Can be given more than once.
  -W  Write guessed primary partition table to given device or file.
  -w  Weight factor of module.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
