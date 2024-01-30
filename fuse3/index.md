---
Title: fuse3
Homepage: https://github.com/libfuse/libfuse/wiki
Repository: 
Architectures: linux-any kfreebsd-any
Version: 3.14.0-4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-hardware 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### fuse3
 
  Filesystem in Userspace (FUSE) is a simple interface for userspace programs to
  export a virtual filesystem to the Linux kernel. It also aims to provide a
  secure method for non privileged users to create and mount their own filesystem
  implementations.
 
 **Installed size:** `100 KB`  
 **How to install:** `sudo apt install fuse3`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * libfuse3-3 
 * mount 
 * sed 
 {{< /spoiler >}}
 
 ##### fusermount
 
 Mount and unmount FUSE filesystems
 
 ```
 root@kali:~# fusermount -h
 fusermount: [options] mountpoint
 Options:
  -h		    print help
  -V		    print version
  -o opt[,opt...]    mount options
  -u		    unmount
  -q		    quiet
  -z		    lazy unmount
 ```
 
 - - -
 
 ##### fusermount3
 
 Mount and unmount FUSE filesystems
 
 ```
 root@kali:~# fusermount3 -h
 fusermount3: [options] mountpoint
 Options:
  -h		    print help
  -V		    print version
  -o opt[,opt...]    mount options
  -u		    unmount
  -q		    quiet
  -z		    lazy unmount
 ```
 
 - - -
 
 ##### mount.fuse
 
 Configuration and mount options for FUSE file systems
 
 ```
 root@kali:~# mount.fuse -h
 usage: mount.fuse type#[source] destination [-t type] [-o opt[,opts...]]
 ```
 
 - - -
 
 ##### mount.fuse3
 
 Configuration and mount options for FUSE file systems
 
 ```
 root@kali:~# mount.fuse3 -h
 usage: mount.fuse3 type#[source] destination [-t type] [-o opt[,opts...]]
 ```
 
 - - -
 
 ### libfuse3-3
 
  Filesystem in Userspace (FUSE) is a simple interface for userspace programs to
  export a virtual filesystem to the Linux kernel. It also aims to provide a
  secure method for non privileged users to create and mount their own filesystem
  implementations.
   
  This package contains the shared library.
 
 **Installed size:** `305 KB`  
 **How to install:** `sudo apt install libfuse3-3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libfuse3-dev
 
  Filesystem in Userspace (FUSE) is a simple interface for userspace programs to
  export a virtual filesystem to the Linux kernel. It also aims to provide a
  secure method for non privileged users to create and mount their own filesystem
  implementations.
   
  This package contains the development files.
 
 **Installed size:** `706 KB`  
 **How to install:** `sudo apt install libfuse3-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libfuse3-3 
 * libselinux-dev
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
