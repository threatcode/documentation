---
Title: extundelete
Homepage: http://extundelete.sourceforge.net/
Repository: https://salsa.debian.org/pkg-security-team/extundelete
Architectures: any
Version: 0.2.4-3
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-recover kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### extundelete
 
  extundelete uses the information stored in the partition's journal to attempt
  to recover a file that has been deleted. There is no guarantee that any
  particular file will be able to be undeleted.
 
 **Installed size:** `147 KB`  
 **How to install:** `sudo apt install extundelete`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcom-err2 
 * libext2fs2 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### extundelete
 
 Utility to undelete files from an ext3 or ext4 partition.
 
 ```
 root@kali:~# extundelete --help
 Usage: extundelete [options] [--] device-file
 Options:
   --version, -[vV]       Print version and exit successfully.
   --help,                Print this help and exit successfully.
   --superblock           Print contents of superblock in addition to the rest.
                          If no action is specified then this option is implied.
   --journal              Show content of journal.
   --after dtime          Only process entries deleted on or after 'dtime'.
   --before dtime         Only process entries deleted before 'dtime'.
 Actions:
   --inode ino            Show info on inode 'ino'.
   --block blk            Show info on block 'blk'.
   --restore-inode ino[,ino,...]
                          Restore the file(s) with known inode number 'ino'.
                          The restored files are created in ./RECOVERED_FILES
                          with their inode number as extension (ie, file.12345).
   --restore-file 'path'  Will restore file 'path'. 'path' is relative to root
                          of the partition and does not start with a '/'
                          The restored file is created in the current
                          directory as 'RECOVERED_FILES/path'.
   --restore-files 'path' Will restore files which are listed in the file 'path'.
                          Each filename should be in the same format as an option
                          to --restore-file, and there should be one per line.
   --restore-directory 'path'
                          Will restore directory 'path'. 'path' is relative to the
                          root directory of the file system.  The restored
                          directory is created in the output directory as 'path'.
   --restore-all          Attempts to restore everything.
   -j journal             Reads an external journal from the named file.
   -b blocknumber         Uses the backup superblock at blocknumber when opening
                          the file system.
   -B blocksize           Uses blocksize as the block size when opening the file
                          system.  The number should be the number of bytes.
   --log 0                Make the program silent.
   --log filename         Logs all messages to filename.
 --log D1=0,D2=filename   Custom control of log messages with comma-separated
    Examples below:       list of options.  Dn must be one of info, warn, or
    --log info,error      error.  Omission of the '=name' results in messages
    --log warn=0          with the specified level to be logged to the console.
    --log error=filename  If the parameter is '=0', logging for the specified
                          level will be turned off.  If the parameter is
                          '=filename', messages with that level will be written
                          to filename.
    -o directory          Save the recovered files to the named directory.
                          The restored files are created in a directory
                          named 'RECOVERED_FILES/' by default.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## extundelete Usage Example

Read the partition (`/dev/sda1`) and restore (`–restore-file`) the given file name (root/importantfile):

```
root@kali:~# extundelete /dev/sda1 --restore-file root/importantfile
WARNING: Extended attributes are not restored.
WARNING: EXT3_FEATURE_INCOMPAT_RECOVER is set.
The partition should be unmounted to undelete any files without further data loss.
If the partition is not currently mounted, this message indicates
it was improperly unmounted, and you should run fsck before continuing.
If you decide to continue, extundelete may overwrite some of the deleted
files and make recovering those files impossible.  You should unmount the
file system and check it with fsck before using extundelete.
Would you like to continue? (y/n)
y
Loading filesystem metadata ... 192 groups loaded.
Loading journal descriptors ... 29495 descriptors loaded.
Writing output to directory RECOVERED_FILES/
```
