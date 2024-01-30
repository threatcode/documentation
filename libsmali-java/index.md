---
Title: libsmali-java
Homepage: https://github.com/JesusFreke/smali
Repository: https://salsa.debian.org/android-tools-team/libsmali-java
Architectures: all
Version: 2.5.2.git2771eae-4
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-reverse-engineering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libsmali-java
 
  smali/baksmali is an assembler/disassembler for the dex format used by dalvik,
  Android's Java VM implementation. The syntax is loosely based on
  Jasmin's/dedexer's syntax and supports the full functionality of the dex
  format like annotations, debug info and line info.
 
 **Installed size:** `1.57 MB`  
 **How to install:** `sudo apt install libsmali-java`  
 
 {{< spoiler "Dependencies:" >}}
 * java-wrappers
 * libantlr3-runtime-java
 * libguava-java
 * libjcommander-java
 {{< /spoiler >}}
 
 ##### baksmali
 
 
 ```
 root@kali:~# baksmali -h
 usage: baksmali [--version] [--help] [<command [<args>]]
 
 Options:
   --help,-h,-? - Show usage information
   --version,-v - Print the version of baksmali and then exit
 
 Commands:
   deodex(de,x) - Deodexes an odex/oat file
   disassemble(dis,d) - Disassembles a dex file.
   dump(du) - Prints an annotated hex dump for the given dex file
   help(h) - Shows usage information
   list(l) - Lists various objects in a dex file.
 
 See baksmali help <command> for more information about a specific command
 ```
 
 - - -
 
 ##### smali
 
 
 ```
 root@kali:~# smali -h
 usage: smali [-v] [-h] [<command [<args>]]
 
 Options:
   -h,-?,--help - Show usage information
   -v,--version - Print the version of baksmali and then exit
 
 Commands:
   assemble(ass,as,a) - Assembles smali files into a dex file.
   help(h) - Shows usage information
 
 See smali help <command> for more information about a specific command
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
