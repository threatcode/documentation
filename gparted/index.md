---
Title: gparted
Homepage: https://gparted.org
Repository: https://salsa.debian.org/debian/gparted
Architectures: any all
Version: 1.5.0-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/gparted-logo.svg
PackagesInfo: |
 ### gparted
 
  GParted uses libparted to detect and manipulate devices and partition
  tables while several (optional) filesystem tools provide support for
  filesystems not included in libparted.
 
 **Installed size:** `2.12 MB`  
 **How to install:** `sudo apt install gparted`  
 
 {{< spoiler "Dependencies:" >}}
 * gparted-common 
 * libatkmm-1.6-1v5 
 * libc6 
 * libcairomm-1.0-1v5 
 * libgcc-s1 
 * libglib2.0-0 
 * libglibmm-2.4-1v5 
 * libgtk-3-0 
 * libgtkmm-3.0-1v5 
 * libpangomm-1.4-1v5 
 * libparted-fs-resize0 
 * libparted2 
 * libsigc++-2.0-0v5 
 * libstdc++6 
 * libuuid1 
 * pkexec
 {{< /spoiler >}}
 
 ##### gparted
 
 GNOME Partition Editor for manipulating disk partitions.
 
 ```
 root@kali:~# man gparted
 GPARTED(8)                      GParted Manual                      GPARTED(8)
 
 NAME
        gparted - GNOME Partition Editor for manipulating disk partitions.
 
 SYNOPSIS
        gparted [device]...
 
 DESCRIPTION
        The gparted application is the GNOME partition editor for creating, re-
        organizing, and deleting disk partitions.
 
        A  disk  device  can  be  subdivided  into one or more partitions.  The
        gparted application enables you to change the partition organization on
        a disk device while preserving the contents of the partition.
 
        With gparted you can accomplish the following tasks:
        - Create a partition table on a disk device.
        - Enable and disable partition flags such as boot and hidden.
        - Perform actions with partitions such as create, delete, resize, move,
        check, label, copy, and paste.
 
        More documentation can be found in the application help manual, and on-
        line at:
        https://gparted.org
 
 EXAMPLES
        You can run gparted from a command line and specify one  or  more  disk
        devices.
 
        For  example,  to  start gparted with the devices /dev/sda and /dev/sdc
        you would use the following command:
 
        gparted /dev/sda /dev/sdc
 
 NOTES
        Editing partitions has the potential to cause LOSS of DATA.
 
        The gparted application is designed to enable you  to  edit  partitions
        while  reducing  the  risk  of data loss.  The application is carefully
        tested and is used by the GParted project team.  However, loss of  data
        might occur due to software bugs, hardware problems, or power failure.
 
        You  can  help  to  reduce the risk of data loss by not mounting or un-
        mounting partitions outside of the gparted application while gparted is
        running.
 
        You are advised to BACKUP your DATA before using the  gparted  applica-
        tion.
 
 REPORTING BUGS
        Report bugs at:
        https://gparted.org/bugs.php
 
 AUTHOR
        Manual page written by Curtis Gedak <gedakc@users.sf.net>
 
 SEE ALSO
        parted(8), fdisk(8), mkfs(8), ntfsprogs(8)
 
 gparted                         Jan 16th, 2011                      GPARTED(8)
 ```
 
 - - -
 
 ### gparted-common
 
  GParted uses libparted to detect and manipulate devices and partition
  tables while several (optional) filesystem tools provide support for
  filesystems not included in libparted.
   
  This package contains architecture-independent data, such as documentation and
  help, icons, and application metadata.
 
 **Installed size:** `6.53 MB`  
 **How to install:** `sudo apt install gparted-common`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
