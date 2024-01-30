---
Title: fatcat
Homepage: https://github.com/Gregwar/fatcat
Repository: https://salsa.debian.org/pkg-security-team/fatcat
Architectures: any
Version: 1.1.1-3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### fatcat
 
  fatcat is a tool to explore, extract, repair and forensic FAT filesystem.
  Its features:
      - Get information about FAT filesystem;
      - Explore FAT file system;
      - Read file or extract directories;
      - Retrieve file & directories that are deleted;
      - Backup & restore the FAT tables;
      - Hack the FAT table by writing on it;
      - Hack the entries by changing clusters and file sizes;
      - Perform a search for orphaned files & directories;
      - Compare and merge the FAT tables;
      - Repair unallocated directories &  files;
      - Supports FAT12, FAT16 and FAT32.
 
 **Installed size:** `145 KB`  
 **How to install:** `sudo apt install fatcat`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### fatcat
 
 FAT filesystem explore, extract, repair, and forensic tool
 
 ```
 root@kali:~# fatcat -h
 fatcat v1.1.0, Gregwar <g.passault@gmail.com>
 
 Usage: fatcat disk.img [options]
   -i: display information about disk
   -O [offset]: global offset (may be partition place)
   -F [format]: output format (default, json)
 
 Browsing & extracting:
   -l [dir]: list files and directories in the given path
   -L [cluster]: list files and directories in the given cluster
   -r [path]: reads the file given by the path
   -R [cluster]: reads the data from given cluster
   -s [size]: specify the size of data to read from the cluster
   -d: enable listing of deleted files
   -x [directory]: extract all files to a directory, deleted files included if -d
                   will start with rootDirectory, unless -c is provided
 * -S: write scamble data in unallocated sectors
 * -z: write scamble data in unallocated sectors
 
 FAT Hacking
   -@ [cluster]: Get the cluster address and information
   -2: analysis & compare the 2 FATs
   -b [file]: backup the FATs (see -t)
 * -p [file]: restore (patch) the FATs (see -t)
 * -w [cluster] -v [value]: write next cluster (see -t)
   -t [table]: specify which table to write (0:both, 1:first, 2:second)
 * -m: merge the FATs
   -o: search for orphan files and directories
 * -f: try to fix reachable directories
 
 Entries hacking
   -e [path]: sets the entry to hack, combined with:
 * -c [cluster]: sets the entry cluster
 * -s [size]: sets the entry size
 * -a [attributes]: sets the entry attributes
   -k [cluster]: try to find an entry that point to that cluster
 
 *: These flags writes on the disk, and may damage it, be careful
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
