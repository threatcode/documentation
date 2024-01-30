---
Title: metacam
Homepage: http://www.cheeseplant.org/~daniel/pages/metacam.html
Repository: https://salsa.debian.org/pkg-security-team/metacam
Architectures: any
Version: 1.2-14
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### metacam
 
  EXIF (Exchangeable Image File Format) is a standard for storing interchange
  information in image files, especially those using JPEG compression. Most
  digital cameras, including mobile phones, now use the EXIF format.
   
  The format is part of the DCF standard created by JEIDA to encourage the
  interoperability between imaging devices. In addition to the standard EXIF
  fields, MetaCam also supports vendor-specific extensions from Nikon, Olympus,
  Canon and Casio.
   
  This program is useful in forensics investigations.
 
 **Installed size:** `144 KB`  
 **How to install:** `sudo apt install metacam`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### metacam
 
 Extract EXIF information from digital camera files
 
 ```
 root@kali:~# metacam -h
 Usage: metacam <options> [filename(s)...]
 
        -h,--help           Display this help
        -v,--verbose        Display unknown tags too
        -a,--all            Display ALL tags (implies -v)
        -x,--xml            Output as XML
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
