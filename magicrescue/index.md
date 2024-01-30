---
Title: magicrescue
Homepage: https://github.com/jbj/magicrescue
Repository: https://salsa.debian.org/pkg-security-team/magicrescue
Architectures: any
Version: 1.1.10+dfsg-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/magicrescue-logo.svg
PackagesInfo: |
 ### magicrescue
 
  Magic Rescue scans a block device for file types it knows how to recover
  and calls an external program to extract them. It looks at "magic bytes"
  (file patterns) in file contents, so it can be used both as an undelete
  utility and for recovering a corrupted drive or partition. As long as
  the file data is there, it will find it.
   
  Magic Rescue uses files called 'recipes'. These files have strings and
  commands to identify and extract data from devices or forensics images.
  So, you can write your own recipes. Currently, there are the following
  recipes: avi, canon-cr2, elf, flac, gpl, gzip, jpeg-exif, jpeg-jfif,
  mbox, mbox-mozilla-inbox, mbox-mozilla-sent, mp3-id3v1, mp3-id3v2,
  msoffice, nikon-raw, perl, png, ppm, sqlite and zip.
   
  This package provides magicrescue, dupemap and magicsort commands.
  magicrescue is a carver and it is useful in forensics investigations.
 
 **Installed size:** `255 KB`  
 **How to install:** `sudo apt install magicrescue`  
 
 {{< spoiler "Dependencies:" >}}
 * dcraw
 * flac
 * libc6 
 * libgdbm-compat4 
 * libjpeg-turbo-progs
 * mpg123
 * sqlite3
 * unzip
 * zip
 {{< /spoiler >}}
 
 ##### dupemap
 
 Creates a database of file checksums and uses it to eliminate duplicates
 
 ```
 root@kali:~# dupemap -h
 Usage: dupemap [OPTIONS] OPERATION PATH...
 Where OPERATION is one of the operations listed in the manpage.
 
 Options:
   -d DATABASE   Read/write from a database on disk
   -I FILE       Read input file names from this file ("-" for stdin)
   -m MINSIZE    Exclude files below this size
   -M MAXSIZE    Exclude files above this size
 ```
 
 - - -
 
 ##### magicrescue
 
 Scans a block device and extracts known file types by looking at magic bytes.
 
 ```
 root@kali:~# magicrescue -h
 Usage: magicrescue [-I FILE] [-M MODE] [-O [+-=][0x]OFFSET] [-b BLOCKSIZE]
 	-d OUTPUT_DIR -r RECIPE1 [-r RECIPE2 [...]] DEVICE1 [DEVICE2 [...]]
 
   -b  Only consider files starting at a multiple of BLOCKSIZE.
   -d  Mandatory.  Output directory for found files.
   -r  Mandatory.  Recipe name, file or directory.
   -I  Read input file names from this file ("-" for stdin)
   -M  Produce machine-readable output to stdout.
   -O  Resume from specified offset (hex or decimal) in the first device.
 
 ```
 
 - - -
 
 ##### magicsort
 
 Categorize files by their file(1) magic
 
 ```
 root@kali:~# magicsort -h
 Usage: magicsort DIRECTORY
 Will invoke your system's file(1) utility to categorize all the files found
 by magicrescue.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
