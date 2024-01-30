---
Title: ssdeep
Homepage: https://github.com/ssdeep-project/ssdeep
Repository: https://salsa.debian.org/pkg-security-team/ssdeep
Architectures: any
Version: 2.14.1+git20180629.57fcfff-3
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: images/ssdeep-logo.svg
PackagesInfo: |
 ### libfuzzy-dev
 
  ssdeep is a tool for recursive computing and matching of Context Triggered
  Piecewise Hashing (aka Fuzzy Hashing).
   
  Fuzzy hashing is a method for comparing similar but not identical files.
  This tool can be used to compare files like regular hashing does (like
  md5sum or sha1sum) but it will find similar files with little differences.
   
  For example, it can be used to identify modified versions of known files
  even if data has been inserted, modified, or deleted in the new files.
   
  This package contains the developments files.
 
 **Installed size:** `59 KB`  
 **How to install:** `sudo apt install libfuzzy-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libfuzzy2 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libfuzzy2
 
  ssdeep is a tool for recursive computing and matching of Context Triggered
  Piecewise Hashing (aka Fuzzy Hashing).
   
  Fuzzy hashing is a method for comparing similar but not identical files.
  This tool can be used to compare files like regular hashing does (like
  md5sum or sha1sum) but it will find similar files with little differences.
   
  For example, it can be used to identify modified versions of known files
  even if data has been inserted, modified, or deleted in the new files.
   
  This package contains the library.
 
 **Installed size:** `49 KB`  
 **How to install:** `sudo apt install libfuzzy2`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### ssdeep
 
  ssdeep is a tool for recursive computing and matching of Context Triggered
  Piecewise Hashing (aka Fuzzy Hashing).
   
  Fuzzy hashing is a method for comparing similar but not identical files.
  This tool can be used to compare files like regular hashing does (like
  md5sum or sha1sum) but it will find similar files with little differences.
   
  For example, it can be used to identify modified versions of known files
  even if data has been inserted, modified, or deleted in the new files.
   
  This package is useful in forensics investigations.
 
 **Installed size:** `82 KB`  
 **How to install:** `sudo apt install ssdeep`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### ssdeep
 
 Computes context triggered piecewise hashes (fuzzy hashes)
 
 ```
 root@kali:~# ssdeep -h
 ssdeep version 2.14.1 by Jesse Kornblum and the ssdeep Project
 For copyright information, see man page or README.TXT.
 
 Usage: ssdeep [-m file] [-k file] [-dpgvrsblcxa] [-t val] [-h|-V] [FILES]
 -m - Match FILES against known hashes in file
 -k - Match signatures in FILES against signatures in file
 -d - Directory mode, compare all files in a directory
 -p - Pretty matching mode. Similar to -d but includes all matches
 -g - Cluster matches together
 -v - Verbose mode. Displays filename as its being processed
 -r - Recursive mode
 -s - Silent mode; all errors are suppressed
 -b - Uses only the bare name of files; all path information omitted
 -l - Uses relative paths for filenames
 -c - Prints output in CSV format
 -x - Compare FILES as signature files
 -a - Display all matches, regardless of score
 -t - Only displays matches above the given threshold
 -h - Display this help message
 -V - Display version number and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
