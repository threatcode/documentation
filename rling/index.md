---
Title: rling
Homepage: https://github.com/Cynosureprime/rling
Repository: https://gitlab.com/kalilinux/packages/rling
Architectures: amd64
Version: 0~git20230629.ec27d46-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rling
 
  This package is similar to the rli utility found in hashcat-utils, but much,
  much faster. rli compares a single file against another file(s) and removes
  all duplicates.
 
 **Installed size:** `158 KB`  
 **How to install:** `sudo apt install rling`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libjudydebian1
 {{< /spoiler >}}
 
 ##### dedupe
 
 
 
 - - -
 
 ##### getpass
 
 Get a password
 
 ```
 root@kali:~# getpass -h
 getpass Version 1.7 2020/07/31 02:36:55 dlr Exp dlr $
 
 extract passwords from result files
 
 	-c [colspec]	Set extraction to N-, N-M, or -M like cut
 	-d [val]	Set delimiter to character, decimal value, or 0x-style hex value
 	-f [field]	Set extraction to field number. Starts at 1
 	-n		Disable extension exclusion entirely (equivalent to -x /dev/null)
 	-t		Disable extension expansion (file.txt -> file.txt.[hashtype], etc.)
 	-x [file]	Read excluded extension list from file, replacing default
 	-h		This help
 	-S exp		Sets $HEX[] conversion for char or range
 	-U exp		Resets $HEX[] conversion for char or range
 			Specify a character like a,b,c, or a range like a-f,
 			0x61-0x66 or as decimal values line 0-32.
 
 Default excluded extensions:
 	.txt .orig .test .csalt.txt .fixme .new 
 
 ```
 
 - - -
 
 ##### rehex
 
 
 
 - - -
 
 ##### rling
 
 
 ```
 root@kali:~# rling --help
 rling: unrecognized option '--help'
 rling version: 1.74 2020/08/24 14:25:43 dlr Exp dlr $
 
 rling - remove matching lines from a file
 rling input output [remfil1 remfile2 ...]
 
 	-i		Ignore any error/missing files on remove list
 	-d		Removes duplicate lines from input (on by default)
 	-D file		Write duplicates to file
 	-n		Do not remove duplicate lines from input
 	-c		Output lines common to input and remove files
 	-s		Sort output. Default is input order.
 			This will make the -b and -f options substantially faster
 	-t number	Number of threads to use
 	-p prime	Force size of hash table
 	-b		Use binary search vs hash (slower, but less memory)
 	-2		Use rli2 mode - all files must be sorted. Low mem usage.
 	-f		Use files instead of memory (slower, but small memory)
 	-l [len]		Limit all matching to a specific length.
 	-M memsize	Maximum memory to use for -f mode
 	-T path		Directory to store temp files in
 	-q [cahwl]	Do frequency analysis on input
 			a - all output, c - count, l - length, w - word,
 			s - running statistics, h - append histogram
 			Additional files will be matched against input files
 	-h		This help
 
 	stdin and stdout can be used in the place of any filename
 ```
 
 - - -
 
 ##### splitlen
 
 
 ```
 root@kali:~# splitlen -h
 splitlen Version 1.10 2020/09/01 21:51:47 dlr Exp dlr $
 
 splitlen -o filename file [..file]
 	-u		Remove $HEX[] encoding from input
 	-o filename	Output to filename, modified with lengths
 			The char # will be replaced with _length in filename
 			If no # is in filename, _len will len appended to name
 	-c char		Use char as place to insert number in -o file
 	-s		Sorts by length into a single output file.
 	-M size		Sets the final buffer size for -s option
 	-S exp		Sets $HEX[] conversion for char or range
 	-U exp		Resets $HEX[] conversion for char or range
 			Specify a character like a,b,c, or a range like a-f,
 			0x61-0x66 or as decimal values line 0-32.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
