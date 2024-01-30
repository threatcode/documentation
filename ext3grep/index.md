---
Title: ext3grep
Homepage: https://code.google.com/archive/p/ext3grep/
Repository: https://salsa.debian.org/pkg-security-team/ext3grep
Architectures: alpha amd64 arm64 armel armhf hurd-i386 i386 ia64 kfreebsd-amd64 kfreebsd-i386 mips64el mipsel ppc64el riscv64 sh4 x32
Version: 0.10.2-5
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-recover kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ext3grep
 
  ext3grep is a simple tool intended to aid anyone who accidentally
  deletes a file on an ext3 filesystem, only to find that they wanted
  it shortly thereafter.
   
  This package is useful in forensics investigations.
 
 **Installed size:** `293 KB`  
 **How to install:** `sudo apt install ext3grep`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### ext3grep
 
 Ext3 file recovery tool
 
 ```
 root@kali:~# ext3grep --help
 Running ext3grep version 0.10.2
 Usage: ext3grep [options] [--] device-file
 Options:
   --version, -[vV]       Print version and exit successfully.
   --help,                Print this help and exit successfully.
   --superblock           Print contents of superblock in addition to the rest.
                          If no action is specified then this option is implied.
   --print                Print content of block or inode, if any.
   --ls                   Print directories with only one line per entry.
                          This option is often needed to turn on filtering.
   --accept filen         Accept 'filen' as a legal filename. Can be used multi-
                          ple times. If you change any --accept you must remove
                          BOTH stage* files!
   --accept-all           Simply accept everything as filename.
   --journal              Show content of journal.
   --show-path-inodes     Show the inode of each directory component in paths.
 Filters:
   --group grp            Only process group 'grp'.
   --directory            Only process directory inodes.
   --after dtime          Only entries deleted on or after 'dtime'.
   --before dtime         Only entries deleted before 'dtime'.
   --deleted              Only show/process deleted entries.
   --allocated            Only show/process allocated inodes/blocks.
   --unallocated          Only show/process unallocated inodes/blocks.
   --reallocated          Do not suppress entries with reallocated inodes.
                          Inodes are considered 'reallocated' if the entry
                          is deleted but the inode is allocated, but also when
                          the file type in the dir entry and the inode are
                          different.
   --zeroed-inodes        Do not suppress entries with zeroed inodes. Linked
                          entries are always shown, regardless of this option.
   --depth depth          Process directories recursively up till a depth
                          of 'depth'.
 Actions:
   --inode-to-block ino   Print the block that contains inode 'ino'.
   --inode ino            Show info on inode 'ino'.
                          If --ls is used and the inode is a directory, then
                          the filters apply to the entries of the directory.
                          If you do not use --ls then --print is implied.
   --block blk            Show info on block 'blk'.
                          If --ls is used and the block is the first block
                          of a directory, then the filters apply to entries
                          of the directory.
                          If you do not use --ls then --print is implied.
   --histogram=[atime|ctime|mtime|dtime|group]
                          Generate a histogram based on the given specs.
                          Using atime, ctime or mtime will change the
                          meaning of --after and --before to those times.
   --journal-block jblk   Show info on journal block 'jblk'.
   --journal-transaction seq
                          Show info on transaction with sequence number 'seq'.
   --dump-names           Write the path of files to stdout.
                          This implies --ls but suppresses it's output.
   --search-start str     Find blocks that start with the fixed string 'str'.
   --search str           Find blocks that contain the fixed string 'str'.
   --search-inode blk     Find inodes that refer to block 'blk'.
   --search-zeroed-inodes Return allocated inode table entries that are zeroed.
   --inode-dirblock-table dir
                          Print a table for directory path 'dir' of directory
                          block numbers found and the inodes used for each file.
   --show-journal-inodes ino
                          Show copies of inode 'ino' still in the journal.
   --restore-inode ino[@seqnr][,ino[@seqnr],...]
                          Restore the file(s) with known inode number 'ino'.
                          The restored files are created in ./RESTORED_FILES/
                          with their inode number as extension (ie, inode.12345).
                          If '@seqnr' is provided then (only) the journal entry
                          with that sequence number is used, otherwise the latest
                          entry is used (if any). You can use that in the case a
                          a file was overwritten or truncated, rather than deleted.
   --restore-file 'path' [--restore-file 'path' ...]
                          Will restore file 'path'. 'path' is relative to the
                          root of the partition and does not start with a '/' (it
                          must be one of the paths returned by --dump-names).
                          The restored directory, file or symbolic link is
                          created in the current directory as 'RESTORED_FILES/path'.
   --restore-all          As --restore-file but attempts to restore everything.
                          The use of --after is highly recommended because the
                          attempt to restore very old files will only result in
                          them being hard linked to a more recently deleted file
                          and as such pollute the output.
   --show-hardlinks       Show all inodes that are shared by two or more files.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
