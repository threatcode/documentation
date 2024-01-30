---
Title: xmount
Homepage: https://www.pinguin.lu/
Repository: https://salsa.debian.org/pkg-security-team/xmount
Architectures: linux-any
Version: 0.7.6-3
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### xmount
 
  xmount can be used to boot forensic disk images with QEMU, KVM,
  VirtualBox, VMware, or the like, since it supports virtual write
  access with redirection to a cache file.
   
  xmount converts between multiple input and output disk image types
  on the fly, using FUSE (Filesystem in Userspace) to create a virtual
  file system representing the input image. The virtual representation
  can be in raw DD, DMG, VirtualBox VDI format, Microsoft VHD format, or
  VMware VMDK format; input images can be raw DD, EWF (Expert Witness
  Compression Format), or AFF (Advanced Forensic Format) files.
 
 **Installed size:** `271 KB`  
 **How to install:** `sudo apt install xmount`  
 
 {{< spoiler "Dependencies:" >}}
 * libafflib0v5 
 * libc6 
 * libewf2 
 * libfuse2 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### xmount
 
 Tool to crossmount between multiple input and output harddisk image files
 
 ```
 root@kali:~# xmount -h
 
 xmount v0.7.6 Copyright (c) 2008-2018 by Gillen Daniel <gillen.dan@pinguin.lu>
 
 Usage:
   xmount [fopts] <xopts> <mntp>
 
 Options:
   fopts:
     -d : Enable FUSE's and xmount's debug mode.
     -h : Display this help message.
     -s : Run single threaded.
     -o no_allow_other : Disable automatic addition of FUSE's allow_other option.
     -o <fopts> : Specify fuse mount options. Will also disable automatic addition of FUSE's allow_other option!
 
   xopts:
     --cache <cfile> : Enable virtual write support.
       <cfile> specifies the cache file to use.
     --in <itype> <ifile> : Input image format and source file(s). May be specified multiple times.
       <itype> can be "raw", "dd", "aewf", "ewf", "aff", "aaff".
       <ifile> specifies the source file. If your image is split into multiple files, you have to specify them all!
     --inopts <iopts> : Specify input library specific options.
       <iopts> specifies a comma separated list of key=value options. See below for details.
     --info : Print out infos about used compiler and libraries.
     --morph <mtype> : Morphing function to apply to input image(s). If not specified, defaults to "combine".
       <mtype> can be "unallocated", "combine", "raid0".
     --morphopts <mopts> : Specify morphing library specific options.
       <mopts> specifies a comma separated list of key=value options. See below for details.
     --offset <off> : Move the output image data start <off> bytes into the input image(s).
     --out <otype> : Output image format. If not specified, defaults to "raw".
       <otype> can be "raw", "dmg", "vdi", "vhd", "vmdk", "vmdks".
     --owcache <file> : Same as --cache <file> but overwrites existing cache file.
     --sizelimit <size> : The data end of input image(s) is set to no more than <size> bytes after the data start.
     --version : Same as --info.
 
   mntp:
     Mount point where output image should be located.
 
 Infos:
   * One --in option and a mount point are mandatory!
   * If you specify --in multiple times, data from all images is morphed into one output image using the specified morphing function.
   * For VMDK emulation, you have to uncomment "user_allow_other" in /etc/fuse.conf or run xmount as root.
 
 Input / Morphing library specific options:
   Input / Morphing libraries might support an own set of options to configure / tune their behaviour.
   Libraries supporting this feature (if any) and their options are listed below.
 
   - libxmount_input_aewf.so
     aewfmaxmem   : Maximum amount of RAM cache, in MiB, for image offset tables. Default: 10 MiB
     aewfmaxfiles : Maximum number of concurrently opened image segment files. Default: 10
     aewfstats    : Output statistics at regular intervals to this directory (must exist).
                    The files created in this directory will be named stats_<pid>.
     aewfrefresh  : The update interval, in seconds, for the statistics (aewfstats must be set). Default: 10s.
     aewflog      : Path for writing log file (must exist).
                    The files created in this directory will be named log_<pid>.
     aewfthreads  : Max. number of threads for parallelized decompression. Default: 4
                    A value of 1 switches back to old, single-threaded legacy functions.
 
   - libxmount_input_aaff.so
     aaffmaxmem   : Maximum amount of RAM cache, in MiB, for image seek offsets. Default: 10 MiB
     aafflog      : Log file name.
     Specify full path for aafflog. The given file name is extended by _<pid>.
 
   - libxmount_morphing_unallocated.so
     unallocated_fs : Specify the filesystem to extract unallocated blocks from. Supported filesystems are: 'hfs', 'fat'. Default: autodetect.
 
   - libxmount_morphing_raid.so
     raid_chunksize : Specify the chunk size to use in bytes. Defaults to 524288 (512k).
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
