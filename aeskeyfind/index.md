---
Title: aeskeyfind
Homepage: https://citp.princeton.edu/our-work/memory/code/
Repository: https://salsa.debian.org/pkg-security-team/aeskeyfind
Architectures: amd64 i386
Version: 1:1.0-11
Metapackages: kali-linux-everything kali-tools-crypto-stego 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### aeskeyfind
 
  This program illustrates automatic techniques for locating 128-bit and
  256-bit AES keys in a captured memory image.
   
  The program uses various algorithms and also performs a simple entropy
  test to filter out blocks that are not keys.  It counts the number of
  repeated bytes and skips blocks that have too many repeats.
   
  This method works even if several bits of the key schedule have been
  corrupted due to memory decay.
   
  This package is useful to several activities, as forensics investigations.
 
 **Installed size:** `33 KB`  
 **How to install:** `sudo apt install aeskeyfind`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### aeskeyfind
 
 Locates 128-bit and 256-bit AES keys in a captured memory image.
 
 ```
 root@kali:~# aeskeyfind --help
 aeskeyfind: invalid option -- '-'
 Usage: aeskeyfind [OPTION]... MEMORY-IMAGE
 Locates scheduled 128-bit and 256-bit AES keys in MEMORY-IMAGE.
 
 	-v		verbose output -- prints the extended keys and 
 			the constraints on the rows of the key schedule
 	-q		don't display a progress bar
 	-t THRESHOLD	sets the maximum number of bit errors allowed 
 			in a candidate key schedule (default = 10)
 	-h		displays this help message
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
