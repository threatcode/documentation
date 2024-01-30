---
archived: "true"
Title: initramfs-tools
Homepage: 
Repository: https://salsa.debian.org/kernel-team/initramfs-tools
Architectures: all
Version: 0.142
Metapackages: kali-linux-arm kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### initramfs-tools
 
  This package builds a bootable initramfs for Linux kernel packages.  The
  initramfs is loaded along with the kernel and is responsible for
  mounting the root filesystem and starting the main init system.
 
 **Installed size:** `113 KB`  
 **How to install:** `sudo apt install initramfs-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * initramfs-tools-core 
 * linux-base
 {{< /spoiler >}}
 
 ##### update-initramfs
 
 Generate an initramfs image
 
 ```
 root@kali:~# update-initramfs -h
 
 Usage: update-initramfs {-c|-d|-u} [-k version] [-v] [-b directory]
 
 Options:
  -k version	Specify kernel version or 'all'
  -c		Create a new initramfs
  -u		Update an existing initramfs
  -d		Remove an existing initramfs
  -b directory	Set alternate boot directory
  -v		Be verbose
 
 See update-initramfs(8) for further details.
 
 ```
 
 - - -
 
 ### initramfs-tools-core
 
  This package contains the mkinitramfs program that can be used to
  create a bootable initramfs for a Linux kernel.  The initramfs should
  be loaded along with the kernel and is then responsible for mounting
  the root filesystem and starting the main init system.
 
 **Installed size:** `215 KB`  
 **How to install:** `sudo apt install initramfs-tools-core`  
 
 {{< spoiler "Dependencies:" >}}
 * coreutils 
 * cpio 
 * klibc-utils 
 * kmod
 * logsave | e2fsprogs 
 * udev
 {{< /spoiler >}}
 
 ##### lsinitramfs
 
 List content of an initramfs image
 
 ```
 root@kali:~# lsinitramfs -h
 
 Usage: lsinitramfs [-l] initramfs-file...
 
 Options:
   -l   Display long and more verbose listing of initramfs content
 
 See lsinitramfs(8) for further details.
 
 ```
 
 - - -
 
 ##### mkinitramfs
 
 Low-level tool for generating an initramfs image
 
 ```
 root@kali:~# mkinitramfs -h
 
 Usage: mkinitramfs [option]... -o outfile [version]
 
 Options:
   -c compress	Override COMPRESS setting in initramfs.conf.
   -d confdir	Specify an alternative configuration directory.
   -l level	Override COMPRESSLEVEL setting in initramfs.conf.
   -k		Keep temporary directory used to make the image.
   -o outfile	Write to outfile.
   -r root	Override ROOT setting in initramfs.conf.
 
 See mkinitramfs(8) for further details.
 
 ```
 
 - - -
 
 ##### unmkinitramfs
 
 Extract content from an initramfs image
 
 ```
 root@kali:~# unmkinitramfs -h
 
 Usage: unmkinitramfs [-v] initramfs-file directory
 
 Options:
   -v   Display verbose messages about extraction
 
 See unmkinitramfs(8) for further details.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
