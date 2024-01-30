---
Title: plocate
Homepage: https://plocate.sesse.net/
Repository: 
Architectures: any
Version: 1.1.19-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### plocate
 
  plocate is a locate(1) based on posting lists, giving much faster searches
  on a much smaller index. It is a drop-in replacement for mlocate in nearly
  all aspects, and is fast on SSDs and non-SSDs alike.
 
 **Installed size:** `540 KB`  
 **How to install:** `sudo apt install plocate`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 * liburing2 
 * libzstd1 
 {{< /spoiler >}}
 
 ##### plocate
 
 Find files by name, quickly
 
 ```
 root@kali:~# plocate -h
 Usage: plocate [OPTION]... PATTERN...
 
   -b, --basename         search only the file name portion of path names
   -c, --count            print number of matches instead of the matches
   -d, --database DBPATH  search for files in DBPATH
                          (default is /var/lib/plocate/plocate.db)
   -i, --ignore-case      search case-insensitively
   -l, --limit LIMIT      stop after LIMIT matches
   -0, --null             delimit matches by NUL instead of newline
   -N, --literal          do not quote filenames, even if printing to a tty
   -r, --regexp           interpret patterns as basic regexps (slow)
       --regex            interpret patterns as extended regexps (slow)
   -w, --wholename        search the entire path name (default; see -b)
       --help             print this help
       --version          print version information
 ```
 
 - - -
 
 ##### plocate-build
 
 Generate index for plocate
 
 ```
 root@kali:~# plocate-build -h
 Usage: plocate-build MLOCATE_DB PLOCATE_DB
 
 Generate plocate index from mlocate.db, typically /var/lib/mlocate/mlocate.db.
 Normally, the destination should be /var/lib/mlocate/plocate.db.
 
   -b, --block-size SIZE  number of filenames to store in each block (default 32)
   -p, --plaintext        input is a plaintext file, not an mlocate database
   -l, --require-visibility FLAG  check visibility before reporting files
       --help             print this help
       --version          print version information
 ```
 
 - - -
 
 ##### updatedb.plocate
 
 Update a database for plocate
 
 ```
 root@kali:~# updatedb.plocate -h
 Usage: updatedb [OPTION]...
 Update a plocate database.
 
   -f, --add-prunefs FS           omit also FS (space-separated)
   -n, --add-prunenames NAMES     omit also NAMES (space-separated)
   -e, --add-prunepaths PATHS     omit also PATHS (space-separated)
       --add-single-prunepath PATH  omit also PATH
   -U, --database-root PATH       the subtree to store in database (default "/")
   -h, --help                     print this help
   -o, --output FILE              database to update (default
                                  `/var/lib/plocate/plocate.db')
   -b, --block-size SIZE          number of filenames to store
                                  in each block (default 32)
       --prune-bind-mounts FLAG   omit bind mounts (default "no")
       --prunefs FS               filesystems to omit from database
       --prunenames NAMES         directory names to omit from database
       --prunepaths PATHS         paths to omit from database
   -l, --require-visibility FLAG  check visibility before reporting files
                                  (default "yes")
   -v, --verbose                  print paths of files as they are found
   -V, --version                  print version information
 
 The configuration defaults to values read from
 `/etc/updatedb.conf'.
 
 Report bugs to steinar+plocate@gunderson.no.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
