---
Title: upx-ucl
Homepage: https://upx.github.io/
Repository: https://salsa.debian.org/debian/upx-ucl/
Architectures: any
Version: 3.96-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-exploitation kali-tools-forensics kali-tools-respond kali-tools-social-engineering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### upx-ucl
 
  UPX is an advanced executable file compressor. UPX will typically
  reduce the file size of programs and DLLs by around 50%-70%, thus
  reducing disk space, network load times, download times etc. The
  current version can compress executables for DOS, Linux/ELF (i386,
  amd64, ppc32) and some other files for different OS.
   
  NOTE: This package is based on the UCL library, which is licensed under GPL.
 
 **Installed size:** `1.97 MB`  
 **How to install:** `sudo apt install upx-ucl`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 * libucl1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### upx-ucl
 
 Compress or expand executable files
 
 ```
 root@kali:~# upx-ucl --help
                        Ultimate Packer for eXecutables
                           Copyright (C) 1996 - 2020
 UPX 3.96        Markus Oberhumer, Laszlo Molnar & John Reiser   Jan 23rd 2020
 
 Usage: upx-ucl [-123456789dlthVL] [-qvfk] [-o file] file..
 
 Commands:
   -1     compress faster                   -9    compress better
   --best compress best (can be slow for big files)
   -d     decompress                        -l    list compressed file
   -t     test compressed file              -V    display version number
   -h     give this help                    -L    display software license
 
 Options:
   -q     be quiet                          -v    be verbose
   -oFILE write output to 'FILE'
   -f     force compression of suspicious files
   --no-color, --mono, --color, --no-progress   change look
 
 Compression tuning options:
   --brute             try all available compression methods & filters [slow]
   --ultra-brute       try even more compression variants [very slow]
 
 Backup options:
   -k, --backup        keep backup files
   --no-backup         no backup files [default]
 
 Overlay options:
   --overlay=copy      copy any extra data attached to the file [default]
   --overlay=strip     strip any extra data attached to the file [DANGEROUS]
   --overlay=skip      don't compress a file with an overlay
 
 Options for djgpp2/coff:
   --coff              produce COFF output [default: EXE]
 
 Options for dos/com:
   --8086              make compressed com work on any 8086
 
 Options for dos/exe:
   --8086              make compressed exe work on any 8086
   --no-reloc          put no relocations in to the exe header
 
 Options for dos/sys:
   --8086              make compressed sys work on any 8086
 
 Options for ps1/exe:
   --8-bit             uses 8 bit size compression [default: 32 bit]
   --8mib-ram          8 megabyte memory limit [default: 2 MiB]
   --boot-only         disables client/host transfer compatibility
   --no-align          don't align to 2048 bytes [enables: --console-run]
 
 Options for watcom/le:
   --le                produce LE output [default: EXE]
 
 Options for win32/pe, win64/pe, rtm32/pe & arm/pe:
   --compress-exports=0    do not compress the export section
   --compress-exports=1    compress the export section [default]
   --compress-icons=0      do not compress any icons
   --compress-icons=1      compress all but the first icon
   --compress-icons=2      compress all but the first icon directory [default]
   --compress-icons=3      compress all icons
   --compress-resources=0  do not compress any resources at all
   --keep-resource=list    do not compress resources specified by list
   --strip-relocs=0        do not strip relocations
   --strip-relocs=1        strip relocations [default]
 
 Options for linux/elf:
   --preserve-build-id     copy .gnu.note.build-id to compressed output
 
 file..   executables to (de)compress
 
 This version supports:
     amd64-darwin.dylib                   dylib/amd64
     amd64-darwin.macho                   macho/amd64
     amd64-linux.elf                      linux/amd64
     amd64-linux.kernel.vmlinux           vmlinux/amd64
     amd64-win64.pe                       win64/pe
     arm-darwin.macho                     macho/arm
     arm-linux.elf                        linux/arm
     arm-linux.kernel.vmlinux             vmlinux/arm
     arm-linux.kernel.vmlinuz             vmlinuz/arm
     arm-wince.pe                         arm/pe
     arm64-darwin.macho                   macho/arm64
     arm64-linux.elf                      linux/arm64
     armeb-linux.elf                      linux/armeb
     armeb-linux.kernel.vmlinux           vmlinux/armeb
     fat-darwin.macho                     macho/fat
     i086-dos16.com                       dos/com
     i086-dos16.exe                       dos/exe
     i086-dos16.sys                       dos/sys
     i386-bsd.elf.execve                  bsd.exec/i386
     i386-darwin.macho                    macho/i386
     i386-dos32.djgpp2.coff               djgpp2/coff
     i386-dos32.tmt.adam                  tmt/adam
     i386-dos32.watcom.le                 watcom/le
     i386-freebsd.elf                     freebsd/i386
     i386-linux.elf                       linux/i386
     i386-linux.elf.execve                linux.exec/i386
     i386-linux.elf.shell                 linux.sh/i386
     i386-linux.kernel.bvmlinuz           bvmlinuz/i386
     i386-linux.kernel.vmlinux            vmlinux/i386
     i386-linux.kernel.vmlinuz            vmlinuz/i386
     i386-netbsd.elf                      netbsd/i386
     i386-openbsd.elf                     openbsd/i386
     i386-win32.pe                        win32/pe
     m68k-atari.tos                       atari/tos
     mips-linux.elf                       linux/mips
     mipsel-linux.elf                     linux/mipsel
     mipsel.r3000-ps1                     ps1/exe
     powerpc-darwin.macho                 macho/ppc32
     powerpc-linux.elf                    linux/ppc32
     powerpc-linux.kernel.vmlinux         vmlinux/ppc32
     powerpc64-linux.elf                  linux/ppc64
     powerpc64le-darwin.macho             macho/ppc64le
     powerpc64le-linux.elf                linux/ppc64le
     powerpc64le-linux.kernel.vmlinux     vmlinux/ppc64le
 
 UPX comes with ABSOLUTELY NO WARRANTY; for details visit https://upx.github.io
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
