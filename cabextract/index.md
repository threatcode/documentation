---
Title: cabextract
Homepage: 
Repository: 
Architectures: any
Version: 1.11-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cabextract
 
  Cabextract is a program which unpacks cabinet (.cab) files, which
  are a form of archive Microsoft uses to distribute their software
  and things like Windows Font Packs.
 
 **Installed size:** `83 KB`  
 **How to install:** `sudo apt install cabextract`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libmspack0 
 {{< /spoiler >}}
 
 ##### cabextract
 
 Program to extract files from Microsoft cabinet (.cab) archives
 
 ```
 root@kali:~# cabextract -h
 Usage: cabextract [options] [-d dir] <cabinet file(s)>
 
 This will extract all files from a cabinet or executable cabinet.
 For multi-part cabinets, only specify the first file in the set.
 
 Options:
   -v   --version       print version / list cabinet
   -h   --help          show this help page
   -l   --list          list contents of cabinet
   -t   --test          test cabinet integrity
   -q   --quiet         only print errors and warnings
   -L   --lowercase     make filenames lowercase
   -f   --fix           salvage as much as possible from corrupted cabinets
   -i   --interactive   prompt whether to overwrite existing files
   -n   --no-overwrite  don't overwrite (skip) existing files
   -k   --keep-symlinks follow symlinked files/dirs when extracting
   -p   --pipe          pipe extracted files to stdout
   -s   --single        restrict search to cabs on the command line
   -F   --filter        extract only files that match the given pattern
   -e   --encoding      assume non-UTF8 filenames have the given encoding
   -d   --directory     extract all files to the given directory
 
 cabextract 1.11 (C) 2000-2023 Stuart Caie <kyzer@cabextract.org.uk>
 This is free software with ABSOLUTELY NO WARRANTY.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
