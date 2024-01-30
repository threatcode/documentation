---
Title: dwarf2json
Homepage: https://github.com/volatilityfoundation/dwarf2json
Repository: https://gitlab.com/kalilinux/packages/dwarf2json
Architectures: any
Version: 0.6.0~git20200714-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dwarf2json
 
  This package contains a Go utility that processes files containing symbol and
  type information to generate Volatilty3 Intermediate Symbol File (ISF) JSON
  output suitable for Linux and macOS analysis.
 
 **Installed size:** `2.53 MB`  
 **How to install:** `sudo apt install dwarf2json`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### dwarf2json
 
 
 ```
 root@kali:~# dwarf2json -h
 Usage: dwarf2json COMMAND
 
 A tool for generating intermediate symbol file (ISF)
 
 Commands:
   linux  generate ISF for Linux analysis
   mac    generate ISF for macOS analysis
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
