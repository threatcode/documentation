---
Title: hashdeep
Homepage: http://md5deep.sf.net
Repository: https://salsa.debian.org/pkg-security-team/hashdeep
Architectures: any
Version: 4.4-7.1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/hashdeep-logo.svg
PackagesInfo: |
 ### hashdeep
 
  hashdeep is a set of tools to compute MD5, SHA1, SHA256, tiger
  and whirlpool hashsums of arbitrary number of files recursively.
   
  The main hashdeep features are:
   
    * It can compare those hashsums with a list of known hashes;
    * The tools can display those that match the list or those that
      does not match;
    * It can  display a time estimation when processing large files.
    * It can do piecewise hashing (hash input files in arbitrary
      sized blocks).
   
  This package is useful in forensics investigations.
 
 **Installed size:** `1.50 MB`  
 **How to install:** `sudo apt install hashdeep`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### hashdeep
 
 Compute, compare, or audit multiple message digests
 
 ```
 root@kali:~# hashdeep -h
 hashdeep version 4.4 by Jesse Kornblum and Simson Garfinkel.
 $ hashdeep [OPTION]... [FILES]...
 -c <alg1,[alg2]> - Compute hashes only. Defaults are MD5 and SHA-256
                    legal values: md5,sha1,sha256,tiger,whirlpool,
 -p <size> - piecewise mode. Files are broken into blocks for hashing
 -r        - recursive mode. All subdirectories are traversed
 -d        - output in DFXML (Digital Forensics XML)
 -k <file> - add a file of known hashes
 -a        - audit mode. Validates FILES against known hashes. Requires -k
 -m        - matching mode. Requires -k
 -x        - negative matching mode. Requires -k
 -w        - in -m mode, displays which known file was matched
 -M and -X act like -m and -x, but display hashes of matching files
 -e        - compute estimated time remaining for each file
 -s        - silent mode. Suppress all error messages
 -b        - prints only the bare name of files; all path information is omitted
 -l        - print relative paths for filenames
 -i/-I     - only process files smaller than the given threshold
 -o        - only process certain types of files. See README/manpage
 -v        - verbose mode. Use again to be more verbose
 -d        - output in DFXML; -W FILE - write to FILE.
 -j <num>  - use num threads (default 8)
 ```
 
 - - -
 
 ##### md5deep
 
 Compute and compare MD5 message digests
 
 ```
 root@kali:~# md5deep -h
 md5deep version 4.4 by Jesse Kornblum and Simson Garfinkel.
 $ md5deep [OPTION]... [FILES]...
 See the man page or README.txt file or use -hh for the full list of options
 -p <size> - piecewise mode. Files are broken into blocks for hashing
 -r        - recursive mode. All subdirectories are traversed
 -e        - show estimated time remaining for each file
 -s        - silent mode. Suppress all error messages
 -z        - display file size before hash
 -m <file> - enables matching mode. See README/man page
 -x <file> - enables negative matching mode. See README/man page
 -M and -X are the same as -m and -x but also print hashes of each file
 -w        - displays which known file generated a match
 -n        - displays known hashes that did not match any input files
 -a and -A add a single hash to the positive or negative matching set
 -b        - prints only the bare name of files; all path information is omitted
 -l        - print relative paths for filenames
 -t        - print GMT timestamp (ctime)
 -i/I <size> - only process files smaller/larger than SIZE
 -v        - display version number and exit
 -d        - output in DFXML; -u - Escape Unicode; -W FILE - write to FILE.
 -j <num>  - use num threads (default 8)
 -Z - triage mode;   -h - help;   -hh - full help
 ```
 
 - - -
 
 ##### sha1deep
 
 Compute and compare SHA-1 message digests
 
 ```
 root@kali:~# sha1deep -h
 sha1deep version 4.4 by Jesse Kornblum and Simson Garfinkel.
 $ sha1deep [OPTION]... [FILES]...
 See the man page or README.txt file or use -hh for the full list of options
 -p <size> - piecewise mode. Files are broken into blocks for hashing
 -r        - recursive mode. All subdirectories are traversed
 -e        - show estimated time remaining for each file
 -s        - silent mode. Suppress all error messages
 -z        - display file size before hash
 -m <file> - enables matching mode. See README/man page
 -x <file> - enables negative matching mode. See README/man page
 -M and -X are the same as -m and -x but also print hashes of each file
 -w        - displays which known file generated a match
 -n        - displays known hashes that did not match any input files
 -a and -A add a single hash to the positive or negative matching set
 -b        - prints only the bare name of files; all path information is omitted
 -l        - print relative paths for filenames
 -t        - print GMT timestamp (ctime)
 -i/I <size> - only process files smaller/larger than SIZE
 -v        - display version number and exit
 -d        - output in DFXML; -u - Escape Unicode; -W FILE - write to FILE.
 -j <num>  - use num threads (default 8)
 -Z - triage mode;   -h - help;   -hh - full help
 ```
 
 - - -
 
 ##### sha256deep
 
 Compute and compare SHA-256 message digests
 
 ```
 root@kali:~# sha256deep -h
 sha256deep version 4.4 by Jesse Kornblum and Simson Garfinkel.
 $ sha256deep [OPTION]... [FILES]...
 See the man page or README.txt file or use -hh for the full list of options
 -p <size> - piecewise mode. Files are broken into blocks for hashing
 -r        - recursive mode. All subdirectories are traversed
 -e        - show estimated time remaining for each file
 -s        - silent mode. Suppress all error messages
 -z        - display file size before hash
 -m <file> - enables matching mode. See README/man page
 -x <file> - enables negative matching mode. See README/man page
 -M and -X are the same as -m and -x but also print hashes of each file
 -w        - displays which known file generated a match
 -n        - displays known hashes that did not match any input files
 -a and -A add a single hash to the positive or negative matching set
 -b        - prints only the bare name of files; all path information is omitted
 -l        - print relative paths for filenames
 -t        - print GMT timestamp (ctime)
 -i/I <size> - only process files smaller/larger than SIZE
 -v        - display version number and exit
 -d        - output in DFXML; -u - Escape Unicode; -W FILE - write to FILE.
 -j <num>  - use num threads (default 8)
 -Z - triage mode;   -h - help;   -hh - full help
 ```
 
 - - -
 
 ##### tigerdeep
 
 Compute and compare Tiger message digests
 
 ```
 root@kali:~# tigerdeep -h
 tigerdeep version 4.4 by Jesse Kornblum and Simson Garfinkel.
 $ tigerdeep [OPTION]... [FILES]...
 See the man page or README.txt file or use -hh for the full list of options
 -p <size> - piecewise mode. Files are broken into blocks for hashing
 -r        - recursive mode. All subdirectories are traversed
 -e        - show estimated time remaining for each file
 -s        - silent mode. Suppress all error messages
 -z        - display file size before hash
 -m <file> - enables matching mode. See README/man page
 -x <file> - enables negative matching mode. See README/man page
 -M and -X are the same as -m and -x but also print hashes of each file
 -w        - displays which known file generated a match
 -n        - displays known hashes that did not match any input files
 -a and -A add a single hash to the positive or negative matching set
 -b        - prints only the bare name of files; all path information is omitted
 -l        - print relative paths for filenames
 -t        - print GMT timestamp (ctime)
 -i/I <size> - only process files smaller/larger than SIZE
 -v        - display version number and exit
 -d        - output in DFXML; -u - Escape Unicode; -W FILE - write to FILE.
 -j <num>  - use num threads (default 8)
 -Z - triage mode;   -h - help;   -hh - full help
 ```
 
 - - -
 
 ##### whirlpooldeep
 
 Compute and compare Whirlpool message digests
 
 ```
 root@kali:~# whirlpooldeep -h
 whirlpooldeep version 4.4 by Jesse Kornblum and Simson Garfinkel.
 $ whirlpooldeep [OPTION]... [FILES]...
 See the man page or README.txt file or use -hh for the full list of options
 -p <size> - piecewise mode. Files are broken into blocks for hashing
 -r        - recursive mode. All subdirectories are traversed
 -e        - show estimated time remaining for each file
 -s        - silent mode. Suppress all error messages
 -z        - display file size before hash
 -m <file> - enables matching mode. See README/man page
 -x <file> - enables negative matching mode. See README/man page
 -M and -X are the same as -m and -x but also print hashes of each file
 -w        - displays which known file generated a match
 -n        - displays known hashes that did not match any input files
 -a and -A add a single hash to the positive or negative matching set
 -b        - prints only the bare name of files; all path information is omitted
 -l        - print relative paths for filenames
 -t        - print GMT timestamp (ctime)
 -i/I <size> - only process files smaller/larger than SIZE
 -v        - display version number and exit
 -d        - output in DFXML; -u - Escape Unicode; -W FILE - write to FILE.
 -j <num>  - use num threads (default 8)
 -Z - triage mode;   -h - help;   -hh - full help
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
