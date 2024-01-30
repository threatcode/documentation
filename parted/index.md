---
Title: parted
Homepage: https://www.gnu.org/software/parted
Repository: https://salsa.debian.org/parted-team/parted
Architectures: any all
Version: 3.6-3
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libparted-dev
 
  GNU Parted is a program that allows you to create, destroy, resize,
  move, and copy disk partitions. This is useful for creating space
  for new operating systems, reorganizing disk usage, and copying data
  to new hard disks.
   
  This package contains the static library and header files for
  libparted, which are really only of interest to parted developers.
 
 **Installed size:** `960 KB`  
 **How to install:** `sudo apt install libparted-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libblkid-dev
 * libc6-dev
 * libdevmapper-dev
 * libparted-fs-resize0 
 * libparted2 
 * uuid-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### libparted-fs-resize0
 
  GNU Parted is a program that allows you to create, destroy, resize,
  move, and copy disk partitions. This is useful for creating space
  for new operating systems, reorganizing disk usage, and copying data
  to new hard disks.
   
  This package contains the libparted-fs-resize shared library for
  resizing HFS+ and FAT file systems.
 
 **Installed size:** `106 KB`  
 **How to install:** `sudo apt install libparted-fs-resize0`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libparted2 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libparted-i18n
 
  GNU Parted is a program that allows you to create, destroy, resize,
  move, and copy disk partitions. This is useful for creating space
  for new operating systems, reorganizing disk usage, and copying data
  to new hard disks.
   
  This package contains localization data.
 
 **Installed size:** `2.13 MB`  
 **How to install:** `sudo apt install libparted-i18n`  
 
 {{< spoiler "Dependencies:" >}}
 * libparted2
 {{< /spoiler >}}
 
 
 - - -
 
 ### libparted2
 
  GNU Parted is a program that allows you to create, destroy, resize,
  move, and copy disk partitions. This is useful for creating space
  for new operating systems, reorganizing disk usage, and copying data
  to new hard disks.
   
  This package contains the shared library.
 
 **Installed size:** `535 KB`  
 **How to install:** `sudo apt install libparted2`  
 
 {{< spoiler "Dependencies:" >}}
 * dmidecode
 * libblkid1 
 * libc6 
 * libdevmapper1.02.1 
 * libuuid1 
 {{< /spoiler >}}
 
 
 - - -
 
 ### parted
 
  GNU Parted is a program that allows you to create, destroy, resize,
  move, and copy disk partitions. This is useful for creating space
  for new operating systems, reorganizing disk usage, and copying data
  to new hard disks.
   
  This package contains the binary and manual page. Further
  documentation is available in parted-doc.
   
  Parted currently supports DOS, Mac, Sun, BSD, GPT, MIPS, and PC98
  partitioning formats, as well as a "loop" (raw disk) type which
  allows use on RAID/LVM. It can detect and remove ASFS/AFFS/APFS,
  Btrfs, ext2/3/4, FAT16/32, HFS, JFS, linux-swap, UFS, XFS, and ZFS
  file systems. Parted also has the ability to create and modify file
  systems of some of these types, but using it to perform file system
  operations is now deprecated.
   
  The nature of this software means that any bugs could cause massive
  data loss. While there are no such bugs known at the moment, they
  could exist, so please back up all important files before running
  it, and do so at your own risk.
 
 **Installed size:** `122 KB`  
 **How to install:** `sudo apt install parted`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libparted2 
 * libreadline8 
 * libtinfo6 
 * libuuid1 
 {{< /spoiler >}}
 
 ##### parted
 
 A partition manipulation program
 
 ```
 root@kali:~# parted -h
 Usage: parted [OPTION]... [DEVICE [COMMAND [PARAMETERS]...]...]
 Apply COMMANDs with PARAMETERS to DEVICE.  If no COMMAND(s) are given, run in
 interactive mode.
 
 OPTIONs:
   -h, --help                      displays this help message
   -l, --list                      lists partition layout on all block devices
   -m, --machine                   displays machine parseable output
   -j, --json                      displays JSON output
   -s, --script                    never prompts for user intervention
   -f, --fix                       in script mode, fix instead of abort when asked
   -v, --version                   displays the version
   -a, --align=[none|cyl|min|opt]  alignment for new partitions
 
 COMMANDs:
   align-check TYPE N                       check partition N for TYPE(min|opt)
         alignment
   help [COMMAND]                           print general help, or help on
         COMMAND
   mklabel,mktable LABEL-TYPE               create a new disklabel (partition
         table)
   mkpart PART-TYPE [FS-TYPE] START END     make a partition
   name NUMBER NAME                         name partition NUMBER as NAME
   print [devices|free|list,all]            display the partition table, or
         available devices, or free space, or all found partitions
   quit                                     exit program
   rescue START END                         rescue a lost partition near START
         and END
   resizepart NUMBER END                    resize partition NUMBER
   rm NUMBER                                delete partition NUMBER
   select DEVICE                            choose the device to edit
   disk_set FLAG STATE                      change the FLAG on selected device
   disk_toggle [FLAG]                       toggle the state of FLAG on selected
         device
   set NUMBER FLAG STATE                    change the FLAG on partition NUMBER
   toggle [NUMBER [FLAG]]                   toggle the state of FLAG on partition
         NUMBER
   type NUMBER TYPE-ID or TYPE-UUID         type set TYPE-ID or TYPE-UUID of
         partition NUMBER
   unit UNIT                                set the default unit to UNIT
   version                                  display the version number and
         copyright information of GNU Parted
 
 Report bugs to bug-parted@gnu.org
 ```
 
 - - -
 
 ##### partprobe
 
 Inform the OS of partition table changes
 
 ```
 root@kali:~# partprobe -h
 Usage: partprobe [OPTION] [DEVICE]...
 Inform the operating system about partition table changes.
 
   -d, --dry-run    do not actually inform the operating system
   -s, --summary    print a summary of contents
   -h, --help       display this help and exit
   -v, --version    output version information and exit
 
 When no DEVICE is given, probe all partitions.
 
 Report bugs to <bug-parted@gnu.org>.
 ```
 
 - - -
 
 ### parted-doc
 
  GNU Parted is a program that allows you to create, destroy, resize,
  move, and copy disk partitions. This is useful for creating space
  for new operating systems, reorganizing disk usage, and copying data
  to new hard disks.
   
  This package contains user documentation for parted and API
  documentation for the library packages.
 
 **Installed size:** `252 KB`  
 **How to install:** `sudo apt install parted-doc`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
