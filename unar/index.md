---
Title: unar
Homepage: https://theunarchiver.com/command-line
Repository: https://salsa.debian.org/debian/unar
Architectures: any
Version: 1.10.7+ds1+really1.10.1-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### unar
 
  The Unarchiver is an archive unpacker program with support for the popular
  zip, RAR, 7z, tar, gzip, bzip2, LZMA, XZ, CAB, MSI, NSIS, EXE, ISO, BIN, and
  split file formats, as well as the old Stuffit, Stuffit X, DiskDouble, Compact
  Pro, Packit, cpio, compress (.Z), ARJ, ARC, PAK, ACE, ZOO, LZH, ADF, DMS, LZX,
  PowerPacker, LBR, Squeeze, Crunch, and other old formats.
   
  This package contains the lsar tool which lists the contents of archives and
  the unar tool which extracts those contents.
 
 **Installed size:** `5.84 MB`  
 **How to install:** `sudo apt install unar`  
 
 {{< spoiler "Dependencies:" >}}
 * gnustep-base-runtime 
 * libbz2-1.0
 * libc6 
 * libgcc-s1 
 * libgnustep-base1.29 
 * libicu72 
 * libobjc4 
 * libstdc++6 
 * libwavpack1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### lsar
 
 List archive file contents
 
 ```
 root@kali:~# lsar -h
 lsar v1.10.1, a tool for listing the contents of archive files.
 Usage: lsar [options] archive [files ...]
 
 Available options:
 -long (-l)                      Print more information about each file in the
                                 archive.
 -verylong (-L)                  Print all available information about each file
                                 in the archive.
 -test (-t)                      Test the integrity of the files in the archive,
                                 if possible.
 -password (-p) <string>         The password to use for decrypting protected
                                 archives.
 -encoding (-e) <encoding name>  The encoding to use for filenames in the
                                 archive, when it is not known. If not specified,
                                 the program attempts to auto-detect the encoding
                                 used. Use "help" or "list" as the argument to
                                 give a listing of all supported encodings.
 -password-encoding (-E) <name>  The encoding to use for the password for the
                                 archive, when it is not known. If not specified,
                                 then either the encoding given by the -encoding
                                 option or the auto-detected encoding is used.
 -print-encoding (-pe)           Print the auto-detected encoding and the
                                 confidence factor after the file list
 -indexes (-i)                   Instead of specifying the files to list as
                                 filenames or wildcard patterns, specify them as
                                 indexes.
 -json (-j)                      Print the listing in JSON format.
 -json-ascii (-ja)               Print the listing in JSON format, encoded as
                                 pure ASCII text.
 -no-recursion (-nr)             Do not attempt to list archives contained in
                                 other archives. For instance, when unpacking a
                                 .tar.gz file, only list the .gz file and not its
                                 contents.
 -help (-h)                      Display this information.
 -version (-v)                   Print version and exit.
 ```
 
 - - -
 
 ##### unar
 
 Extract archive file contents
 
 ```
 root@kali:~# unar -h
 unar v1.10.1, a tool for extracting the contents of archive files.
 Usage: unar [options] archive [files ...]
 
 Available options:
 -output-directory (-o) <string>    The directory to write the contents of the
                                    archive to. Defaults to the current
                                    directory. If set to a single dash (-), no
                                    files will be created, and all data will be
                                    output to stdout.
 -force-overwrite (-f)              Always overwrite files when a file to be
                                    unpacked already exists on disk. By default,
                                    the program asks the user if possible,
                                    otherwise skips the file.
 -force-rename (-r)                 Always rename files when a file to be
                                    unpacked already exists on disk.
 -force-skip (-s)                   Always skip files when a file to be unpacked
                                    already exists on disk.
 -force-directory (-d)              Always create a containing directory for the
                                    contents of the unpacked archive. By default,
                                    a directory is created if there is more than
                                    one top-level file or folder.
 -no-directory (-D)                 Never create a containing directory for the
                                    contents of the unpacked archive.
 -password (-p) <string>            The password to use for decrypting protected
                                    archives.
 -encoding (-e) <encoding name>     The encoding to use for filenames in the
                                    archive, when it is not known. If not
                                    specified, the program attempts to
                                    auto-detect the encoding used. Use "help" or
                                    "list" as the argument to give a listing of
                                    all supported encodings.
 -password-encoding (-E) <name>     The encoding to use for the password for the
                                    archive, when it is not known. If not
                                    specified, then either the encoding given by
                                    the -encoding option or the auto-detected
                                    encoding is used.
 -indexes (-i)                      Instead of specifying the files to unpack as
                                    filenames or wildcard patterns, specify them
                                    as indexes, as output by lsar.
 -no-recursion (-nr)                Do not attempt to extract archives contained
                                    in other archives. For instance, when
                                    unpacking a .tar.gz file, only unpack the .gz
                                    file and not its contents.
 -copy-time (-t)                    Copy the file modification time from the
                                    archive file to the containing directory, if
                                    one is created.
 -forks (-k) <visible|hidden|skip>  How to handle Mac OS resource forks.
                                    "visible" creates AppleDouble files with the
                                    extension ".rsrc", "hidden" creates
                                    AppleDouble files with the prefix "._", and
                                    "skip" discards all resource forks. Defaults
                                    to "visible".
 -quiet (-q)                        Run in quiet mode.
 -version (-v)                      Print version and exit.
 -help (-h)                         Display this information.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
