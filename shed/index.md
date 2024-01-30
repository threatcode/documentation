---
Title: shed
Homepage: http://shed.sf.net
Repository: https://salsa.debian.org/pkg-security-team/shed
Architectures: any
Version: 1.15-5
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### shed
 
  shed (Simple Hex Editor) is an easy application for viewing and editing
  files in text mode, using ncurses. The main features are:
   
    - Displays each byte as ascii, hex, decimal, octal and binary;
    - Allows changes to be input in all of the above displayed modes,
      with bit toggling in the binary column;
    - Simple Pico-style interface;
    - Search resource;
    - Can dump information to file;
    - Small memory requirements because file is not loaded into memory;
    - Large file support.
   
  shed is useful in forensics investigations.
 
 **Installed size:** `58 KB`  
 **How to install:** `sudo apt install shed`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libncurses6 
 * libtinfo6 
 {{< /spoiler >}}
 
 ##### shed
 
 Simple hex editor with a pico-style interface
 
 ```
 root@kali:~# shed -h
 usage: shed [OPTIONS] [FILE]
 
 options:
   -r / --readonly       open FILE read only
   -s / --start=OFFSET   position cursor to offset
   -H / --hex            start with hex offsets
   -L / --length         set length (for device files)
   -h / --help           show help and exit
   -v / --version        show version and exit
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
