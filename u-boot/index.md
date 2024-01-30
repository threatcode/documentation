---
archived: "true"
Title: u-boot
Homepage: https://www.denx.de/wiki/U-Boot/
Repository: https://salsa.debian.org/debian/u-boot
Architectures: linux-any all
Version: 2022.04+dfsg-2
Metapackages: kali-linux-arm kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### u-boot
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install u-boot`  
 
 
 - - -
 
 ### u-boot-qemu
 
  Das U-Boot is a cross-platform bootloader for embedded systems,
  used as the default boot loader by several board vendors.  It is
  intended to be easy to port and to debug, and runs on many
  supported architectures, including PPC, ARM, MIPS, x86, m68k,
  NIOS, and Microblaze.
   
  This package includes boot loaders for qemu/kvm.
   
  Included platforms:
  qemu-ppce500
  qemu-riscv64
  qemu-riscv64_smode
  qemu-x86
  qemu-x86_64
  qemu_arm
  qemu_arm64
 
 **Installed size:** `11.38 MB`  
 **How to install:** `sudo apt install u-boot-qemu`  
 
 
 - - -
 
 ### u-boot-tools
 
  This package includes programs for generating and listing U-Boot
  images in various formats:
   - mkimage
   - dumpimage
   - mksunxiboot
   - mkenvimage
 
 **Installed size:** `758 KB`  
 **How to install:** `sudo apt install u-boot-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgnutls30 
 * libssl3 
 * libtinfo6 
 * libuuid1 
 {{< /spoiler >}}
 
 ##### dumpimage
 
 
 ```
 root@kali:~# dumpimage --help
 dumpimage: invalid option -- '-'
 Usage: dumpimage [-T type] -l image
           -l ==> list image header information
           -T ==> parse image file as 'type'
        dumpimage [-T type] [-p position] [-o outfile] image
           -T ==> declare image type as 'type'
           -p ==> 'position' (starting at 0) of the component to extract from image
           -o ==> extract component to file 'outfile'
        dumpimage -h ==> print usage information and exit
        dumpimage -V ==> print version information and exit
 ```
 
 - - -
 
 ##### kwboot
 
 Boot Marvell Kirkwood (and others 32-bit) SoCs over a serial link.
 
 ```
 root@kali:~# kwboot -h
 kwboot version 2022.04+dfsg-2+b1
 Usage: kwboot [OPTIONS] [-b <image> | -D <image> | -b | -d ] [-B <baud> ] [-t] <TTY>
 
   -b <image>: boot <image> with preamble (Kirkwood, Avanta, Armada 370/XP/375/38x/39x)
   -D <image>: boot <image> without preamble (Dove)
   -b: enter xmodem boot mode
   -d: enter console debug mode
   -a: use timings for Armada XP
   -s <resp-timeo>: use specific response-timeout
   -o <block-timeo>: use specific xmodem block timeout
 
   -t: mini terminal
 
   -B <baud>: set baud rate
 
 ```
 
 - - -
 
 ##### mkeficapsule
 
 
 ```
 root@kali:~# mkeficapsule -h
 Usage: mkeficapsule [options] <image blob> <output file>
 Options:
 	-f, --fit                   FIT image type
 	-r, --raw                   raw image type
 	-g, --guid <guid string>    guid for image blob type
 	-i, --index <index>         update image index
 	-I, --instance <instance>   update hardware instance
 	-p, --private-key <privkey file>  private key file
 	-c, --certificate <cert file>     signer's certificate file
 	-m, --monotonic-count <count>     monotonic count
 	-d, --dump_sig              dump signature (*.p7)
 	-h, --help                  print a help message
 ```
 
 - - -
 
 ##### mkenvimage
 
 
 
 - - -
 
 ##### mkimage
 
 Generate image for U-Boot
 
 ```
 root@kali:~# mkimage -h
 mkimage: invalid option -- 'h'
 Error: Invalid option
 Usage: mkimage [-T type] -l image
           -l ==> list image header information
           -T ==> parse image file as 'type'
        mkimage [-x] -A arch -O os -T type -C comp -a addr -e ep -n name -d data_file[:data_file...] image
           -A ==> set architecture to 'arch'
           -O ==> set operating system to 'os'
           -T ==> set image type to 'type'
           -C ==> set compression type 'comp'
           -a ==> set load address to 'addr' (hex)
           -e ==> set entry point to 'ep' (hex)
           -n ==> set image name to 'name'
           -d ==> use image data from 'datafile'
           -x ==> set XIP (execute in place)
        mkimage [-D dtc_options] [-f fit-image.its|-f auto|-F] [-b <dtb> [-b <dtb>]] [-E] [-B size] [-i <ramdisk.cpio.gz>] fit-image
            <dtb> file is used with -f auto, it may occur multiple times.
           -D => set all options for device tree compiler
           -f => input filename for FIT source
           -i => input filename for ramdisk file
           -E => place data outside of the FIT structure
           -B => align size in hex for FIT structure and header
 Signing / verified boot options: [-k keydir] [-K dtb] [ -c <comment>] [-p addr] [-r] [-N engine]
           -k => set directory containing private keys
           -K => write public keys to this .dtb file
           -G => use this signing key (in lieu of -k)
           -c => add comment in signature node
           -F => re-sign existing FIT image
           -p => place external data at a static position
           -r => mark keys used as 'required' in dtb
           -N => openssl engine to use for signing
        mkimage -V ==> print version information and exit
 Use '-T list' to see a list of available image types
 ```
 
 - - -
 
 ##### mksunxiboot
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
