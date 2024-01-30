---
Title: rifiuti2
Homepage: https://abelcheung.github.io/rifiuti2
Repository: https://salsa.debian.org/pkg-security-team/rifiuti2
Architectures: any
Version: 0.7.0-3
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rifiuti2
 
  Rifiuti2 analyses recycle bin files from Windows. Analysis of Windows
  recycle bin is usually carried out during Windows computer forensics.
   
  Rifiuti2 can extract file deletion time, original path and size of deleted
  files and whether the deleted files have been moved out from the recycle
  bin since they are trashed.
   
  Rifiuti2 is a rewrite of rifiuti, which is originally written for identical
  purpose. Then it was extended to cover more functionalities, such as:
   
    * Handles recycle bin up to Windows 10;
    * Handles ancient Windows like 95, NT4 and ME;
    * Supports all localized versions of Windows - both Unicode-based ones
      and legacy ones (using ANSI code page);
    * Supports output in XML format as well as original tab-delimited text.
   
  Rifiuti2 is designed to be portable and runs on command line environment. Two
  programs rifiuti and rifiuti-vista are chosen depending on relevant Windows
  recycle bin format.
 
 **Installed size:** `134 KB`  
 **How to install:** `sudo apt install rifiuti2`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libglib2.0-0 
 {{< /spoiler >}}
 
 ##### rifiuti-vista
 
 MS Windows recycle bin analysis tool
 
 ```
 root@kali:~# rifiuti-vista -h
 Usage:
   rifiuti-vista [OPTION?] DIR_OR_FILE
 
 Parse index files in C:\$Recycle.bin style folder and dump recycle bin data.  Can also dump a single index file.
 
 Help Options:
   -h, --help                 Show help options
   --help-all                 Show all help options
   --help-text                Show plain text output options
 
 Application Options:
   -o, --output=FILE          Write output to FILE
   -x, --xml                  Output in XML format instead of tab-delimited values
   -z, --localtime            Present deletion time in time zone of local system (default is UTC)
   -v, --version              Print version information and exit
 
 Report bugs to https://github.com/abelcheung/rifiuti2/issues
 ```
 
 - - -
 
 ##### rifiuti2
 
 MS Windows recycle bin analysis tool
 
 ```
 root@kali:~# rifiuti2 -h
 Usage:
   rifiuti2 [OPTION?] INFO2
 
 Parse INFO2 file and dump recycle bin data.
 
 Help Options:
   -h, --help                         Show help options
   --help-all                         Show all help options
   --help-text                        Show plain text output options
 
 Application Options:
   -o, --output=FILE                  Write output to FILE
   -x, --xml                          Output in XML format instead of tab-delimited values
   -z, --localtime                    Present deletion time in time zone of local system (default is UTC)
   -v, --version                      Print version information and exit
   -l, --legacy-filename=CODEPAGE     Show legacy (8.3) path if available and specify its CODEPAGE
 
 Report bugs to https://github.com/abelcheung/rifiuti2/issues
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
