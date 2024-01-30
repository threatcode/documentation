---
Title: p7zip
Homepage: http://p7zip.sourceforge.net/
Repository: https://salsa.debian.org/debian/p7zip
Architectures: any
Version: 16.02+dfsg-8
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-forensics kali-tools-respond 
Icon: images/p7zip-logo.svg
PackagesInfo: |
 ### p7zip
 
  p7zip is the Unix command-line port of 7-Zip, a file archiver that
  handles the 7z format which features very high compression ratios.
   
  p7zip provides:
   - /usr/bin/7zr
     a standalone minimal version of the 7-zip tool that only handles
     7z, LZMA and XZ archives. 7z compression is 30-50% better than ZIP
     compression.
   - /usr/bin/p7zip
     a gzip-like wrapper around 7zr.
   
  p7zip can be used with popular compression interfaces (such as File
  Roller or Nautilus).
   
  Another package, p7zip-full, provides 7z and 7za which support more
  compression formats.
 
 **Installed size:** `987 KB`  
 **How to install:** `sudo apt install p7zip`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### 7zr
 
 A file archiver with high compression ratio format
 
 ```
 root@kali:~# 7zr -h
 
 7-Zip (a) [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
 p7zip Version 16.02 (locale=C,Utf16=off,HugeFiles=on,64 bits,8 CPUs AMD Ryzen 7 3700X 8-Core Processor              (870F10),ASM,AES-NI)
 
 Usage: 7za <command> [<switches>...] <archive_name> [<file_names>...]
        [<@listfiles...>]
 
 <Commands>
   a : Add files to archive
   b : Benchmark
   d : Delete files from archive
   e : Extract files from archive (without using directory names)
   h : Calculate hash values for files
   i : Show information about supported formats
   l : List contents of archive
   rn : Rename files in archive
   t : Test integrity of archive
   u : Update files to archive
   x : eXtract files with full paths
 
 <Switches>
   -- : Stop switches parsing
   -ai[r[-|0]]{@listfile|!wildcard} : Include archives
   -ax[r[-|0]]{@listfile|!wildcard} : eXclude archives
   -ao{a|s|t|u} : set Overwrite mode
   -an : disable archive_name field
   -bb[0-3] : set output log level
   -bd : disable progress indicator
   -bs{o|e|p}{0|1|2} : set output stream for output/error/progress line
   -bt : show execution time statistics
   -i[r[-|0]]{@listfile|!wildcard} : Include filenames
   -m{Parameters} : set compression Method
     -mmt[N] : set number of CPU threads
   -o{Directory} : set Output directory
   -r[-|0] : Recurse subdirectories
   -sa{a|e|s} : set Archive name mode
   -scc{UTF-8|WIN|DOS} : set charset for for console input/output
   -scs{UTF-8|UTF-16LE|UTF-16BE|WIN|DOS|{id}} : set charset for list files
   -scrc[CRC32|CRC64|SHA1|SHA256|*] : set hash function for x, e, h commands
   -sdel : delete files after compression
   -seml[.] : send archive by email
   -sfx[{name}] : Create SFX archive
   -si[{name}] : read data from stdin
   -slp : set Large Pages mode
   -slt : show technical information for l (List) command
   -snh : store hard links as links
   -snl : store symbolic links as links
   -sni : store NT security information
   -sns[-] : store NTFS alternate streams
   -so : write data to stdout
   -spd : disable wildcard matching for file names
   -spe : eliminate duplication of root folder for extract command
   -spf : use fully qualified file paths
   -ssc[-] : set sensitive case mode
   -ssw : compress shared files
   -stl : set archive timestamp from the most recently modified file
   -stm{HexMask} : set CPU thread affinity mask (hexadecimal number)
   -stx{Type} : exclude archive type
   -t{Type} : Set type of archive
   -u[-][p#][q#][r#][x#][y#][z#][!newArchiveName] : Update options
   -v{Size}[b|k|m|g] : Create volumes
   -w[{path}] : assign Work directory. Empty path means a temporary directory
   -x[r[-|0]]{@listfile|!wildcard} : eXclude filenames
   -y : assume Yes on all queries
 ```
 
 - - -
 
 ##### p7zip
 
 Wrapper on 7-Zip file archiver with high compression ratio
 
 ```
 root@kali:~# p7zip -h
 Usage: /usr/bin/p7zip [options] [--] [ name ... ]
 
 Options:
     -c --stdout --to-stdout      output data to stdout
     -d --decompress --uncompress decompress file
     -f --force                   do not ask questions
     -k --keep                    keep original file
     -h --help                    print this help
     --                           treat subsequent arguments as file
                                  names, even if they start with a dash
 
 ```
 
 - - -
 
 ### p7zip-full
 
  p7zip is the Unix command-line port of 7-Zip, a file archiver that
  handles the 7z format which features very high compression ratios.
   
  p7zip-full provides utilities to pack and unpack 7z archives within
  a shell or using a GUI (such as Ark, File Roller or Nautilus).
   
  Installing p7zip-full allows File Roller to use the very efficient 7z
  compression format for packing and unpacking files and directories.
  Additionally, it provides the 7z and 7za commands.
   
  List of supported formats:
    - Packing / unpacking: 7z, ZIP, GZIP, BZIP2, XZ and TAR
    - Unpacking only: APM, ARJ, CAB, CHM, CPIO, CramFS, DEB, DMG, FAT,
      HFS, ISO, LZH, LZMA, LZMA2, MBR, MSI, MSLZ, NSIS, NTFS, RAR (only
      if non-free p7zip-rar package is installed), RPM, SquashFS, UDF,
      VHD, WIM, XAR and Z.
   
  The dependent package, p7zip, provides 7zr, a light version of 7za,
  and p7zip, a gzip-like wrapper around 7zr.
 
 **Installed size:** `4.55 MB`  
 **How to install:** `sudo apt install p7zip-full`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 * p7zip 
 {{< /spoiler >}}
 
 ##### 7z
 
 A file archiver with high compression ratio format
 
 ```
 root@kali:~# 7z -h
 
 7-Zip [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
 p7zip Version 16.02 (locale=C,Utf16=off,HugeFiles=on,64 bits,8 CPUs AMD Ryzen 7 3700X 8-Core Processor              (870F10),ASM,AES-NI)
 
 Usage: 7z <command> [<switches>...] <archive_name> [<file_names>...]
        [<@listfiles...>]
 
 <Commands>
   a : Add files to archive
   b : Benchmark
   d : Delete files from archive
   e : Extract files from archive (without using directory names)
   h : Calculate hash values for files
   i : Show information about supported formats
   l : List contents of archive
   rn : Rename files in archive
   t : Test integrity of archive
   u : Update files to archive
   x : eXtract files with full paths
 
 <Switches>
   -- : Stop switches parsing
   -ai[r[-|0]]{@listfile|!wildcard} : Include archives
   -ax[r[-|0]]{@listfile|!wildcard} : eXclude archives
   -ao{a|s|t|u} : set Overwrite mode
   -an : disable archive_name field
   -bb[0-3] : set output log level
   -bd : disable progress indicator
   -bs{o|e|p}{0|1|2} : set output stream for output/error/progress line
   -bt : show execution time statistics
   -i[r[-|0]]{@listfile|!wildcard} : Include filenames
   -m{Parameters} : set compression Method
     -mmt[N] : set number of CPU threads
   -o{Directory} : set Output directory
   -p{Password} : set Password
   -r[-|0] : Recurse subdirectories
   -sa{a|e|s} : set Archive name mode
   -scc{UTF-8|WIN|DOS} : set charset for for console input/output
   -scs{UTF-8|UTF-16LE|UTF-16BE|WIN|DOS|{id}} : set charset for list files
   -scrc[CRC32|CRC64|SHA1|SHA256|*] : set hash function for x, e, h commands
   -sdel : delete files after compression
   -seml[.] : send archive by email
   -sfx[{name}] : Create SFX archive
   -si[{name}] : read data from stdin
   -slp : set Large Pages mode
   -slt : show technical information for l (List) command
   -snh : store hard links as links
   -snl : store symbolic links as links
   -sni : store NT security information
   -sns[-] : store NTFS alternate streams
   -so : write data to stdout
   -spd : disable wildcard matching for file names
   -spe : eliminate duplication of root folder for extract command
   -spf : use fully qualified file paths
   -ssc[-] : set sensitive case mode
   -ssw : compress shared files
   -stl : set archive timestamp from the most recently modified file
   -stm{HexMask} : set CPU thread affinity mask (hexadecimal number)
   -stx{Type} : exclude archive type
   -t{Type} : Set type of archive
   -u[-][p#][q#][r#][x#][y#][z#][!newArchiveName] : Update options
   -v{Size}[b|k|m|g] : Create volumes
   -w[{path}] : assign Work directory. Empty path means a temporary directory
   -x[r[-|0]]{@listfile|!wildcard} : eXclude filenames
   -y : assume Yes on all queries
 ```
 
 - - -
 
 ##### 7za
 
 A file archiver with high compression ratio format
 
 ```
 root@kali:~# 7za -h
 
 7-Zip (a) [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
 p7zip Version 16.02 (locale=C,Utf16=off,HugeFiles=on,64 bits,8 CPUs AMD Ryzen 7 3700X 8-Core Processor              (870F10),ASM,AES-NI)
 
 Usage: 7za <command> [<switches>...] <archive_name> [<file_names>...]
        [<@listfiles...>]
 
 <Commands>
   a : Add files to archive
   b : Benchmark
   d : Delete files from archive
   e : Extract files from archive (without using directory names)
   h : Calculate hash values for files
   i : Show information about supported formats
   l : List contents of archive
   rn : Rename files in archive
   t : Test integrity of archive
   u : Update files to archive
   x : eXtract files with full paths
 
 <Switches>
   -- : Stop switches parsing
   -ai[r[-|0]]{@listfile|!wildcard} : Include archives
   -ax[r[-|0]]{@listfile|!wildcard} : eXclude archives
   -ao{a|s|t|u} : set Overwrite mode
   -an : disable archive_name field
   -bb[0-3] : set output log level
   -bd : disable progress indicator
   -bs{o|e|p}{0|1|2} : set output stream for output/error/progress line
   -bt : show execution time statistics
   -i[r[-|0]]{@listfile|!wildcard} : Include filenames
   -m{Parameters} : set compression Method
     -mmt[N] : set number of CPU threads
   -o{Directory} : set Output directory
   -p{Password} : set Password
   -r[-|0] : Recurse subdirectories
   -sa{a|e|s} : set Archive name mode
   -scc{UTF-8|WIN|DOS} : set charset for for console input/output
   -scs{UTF-8|UTF-16LE|UTF-16BE|WIN|DOS|{id}} : set charset for list files
   -scrc[CRC32|CRC64|SHA1|SHA256|*] : set hash function for x, e, h commands
   -sdel : delete files after compression
   -seml[.] : send archive by email
   -sfx[{name}] : Create SFX archive
   -si[{name}] : read data from stdin
   -slp : set Large Pages mode
   -slt : show technical information for l (List) command
   -snh : store hard links as links
   -snl : store symbolic links as links
   -sni : store NT security information
   -sns[-] : store NTFS alternate streams
   -so : write data to stdout
   -spd : disable wildcard matching for file names
   -spe : eliminate duplication of root folder for extract command
   -spf : use fully qualified file paths
   -ssc[-] : set sensitive case mode
   -ssw : compress shared files
   -stl : set archive timestamp from the most recently modified file
   -stm{HexMask} : set CPU thread affinity mask (hexadecimal number)
   -stx{Type} : exclude archive type
   -t{Type} : Set type of archive
   -u[-][p#][q#][r#][x#][y#][z#][!newArchiveName] : Update options
   -v{Size}[b|k|m|g] : Create volumes
   -w[{path}] : assign Work directory. Empty path means a temporary directory
   -x[r[-|0]]{@listfile|!wildcard} : eXclude filenames
   -y : assume Yes on all queries
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
