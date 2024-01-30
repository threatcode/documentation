---
archived: "true"
Title: abootimg
Homepage: http://gitorious.org/ac100/abootimg
Repository: 
Architectures: any
Version: 0.6-1
Metapackages: kali-linux-arm kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### abootimg
 
  Android devices use a special partition format to boot any
  operating system on the devices. These boot-images contain
  a kernel image, a ramdisk, optionally a 2nd stage boot loader
  and the commandline passed to the kernel when booting.
  The original mkbootimg from Android can only create these images
  where abootimg can also extract and modify them.
  Handling android boot images is necessary when bringing other
  operating systems to android devices.
 
 **Installed size:** `44 KB`  
 **How to install:** `sudo apt install abootimg`  
 
 {{< spoiler "Dependencies:" >}}
 * libblkid1 
 * libc6 
 {{< /spoiler >}}
 
 ##### abootimg
 
 Manipulate Android Boot Images.
 
 ```
 root@kali:~# abootimg --help
 error - bad arguments
 
  abootimg - manipulate Android Boot Images.
  (c) 2010-2011 Gilles Grandou <gilles@grandou.net>
  0.6
 
  abootimg [-h]
 
       print usage
 
  abootimg -i <bootimg>
 
       print boot image information
 
  abootimg -x <bootimg> [<bootimg.cfg> [<kernel> [<ramdisk> [<secondstage>]]]]
 
       extract objects from boot image:
       - config file (default name bootimg.cfg)
       - kernel image (default name zImage)
       - ramdisk image (default name initrd.img)
       - second stage image (default name stage2.img)
 
  abootimg -u <bootimg> [-c "param=value"] [-f <bootimg.cfg>] [-k <kernel>] [-r <ramdisk>] [-s <secondstage>]
 
       update a current boot image with objects given in command line
       - header informations given in arguments (several can be provided)
       - header informations given in config file
       - kernel image
       - ramdisk image
       - second stage image
 
       bootimg has to be valid Android Boot Image, or the update will abort.
 
  abootimg --create <bootimg> [-c "param=value"] [-f <bootimg.cfg>] -k <kernel> -r <ramdisk> [-s <secondstage>]
 
       create a new image from scratch.
       if the boot image file is a block device, sanity check will be performed to avoid overwriting a existing
       filesystem.
 
       argurments are the same than for -u.
       kernel and ramdisk are mandatory.
 
 ```
 
 - - -
 
 ##### abootimg-pack-initrd
 
 
 ```
 root@kali:~# abootimg-pack-initrd -h
 ramdisk does not exist.
 ```
 
 - - -
 
 ##### abootimg-unpack-initrd
 
 
 ```
 root@kali:~# abootimg-unpack-initrd -h
 -h does not exist.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
