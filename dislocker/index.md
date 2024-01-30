---
Title: dislocker
Homepage: https://github.com/Aorimn/dislocker
Repository: https://salsa.debian.org/pkg-security-team/dislocker
Architectures: any
Version: 0.7.3-3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dislocker
 
  Dislocker has been designed to read BitLocker encrypted partitions under
  a Linux system. The driver used to read volumes encrypted in Windows system
  versions of the Vista to 10 and BitLocker-To-Go encrypted partitions, that's
  USB/FAT32 partitions.
   
  The software works with driver composed of a library, with multiple binaries
  using this library. Decrypting the partition, you have to give it a mount
  point where, once keys are decrypted, a file named dislocker-file appears.
  This file is a virtual NTFS partition, so you can mount it as any NTFS
  partition and then read from or write to it. Writing to the NTFS virtual
  file will change the underlying BitLocker partition content. To use
  dislocker-find Ruby is required.
   
  This tool is useful in cryptography managing and forensics investigations.
 
 **Installed size:** `94 KB`  
 **How to install:** `sudo apt install dislocker`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libdislocker0.7 
 * libfuse2 
 * libruby3.1 
 {{< /spoiler >}}
 
 ##### dislocker
 
 Read/write BitLocker encrypted volumes under Linux, OSX and FreeBSD.
 
 ```
 root@kali:~# dislocker -h
 dislocker by Romain Coltel, v0.7.2 (compiled for Linux/x86_64)
 
 Usage: dislocker [-hqrsv] [-l LOG_FILE] [-O OFFSET] [-V VOLUME DECRYPTMETHOD -F[N]] [-- ARGS...]
     with DECRYPTMETHOD = -p[RECOVERY_PASSWORD]|-f BEK_FILE|-u[USER_PASSWORD]|-k FVEK_FILE|-K VMK_FILE|-c
 
 Options:
     -c, --clearkey        decrypt volume using a clear key (default)
     -f, --bekfile BEKFILE
                           decrypt volume using the bek file (on USB key)
     -F, --force-block=[N] force use of metadata block number N (1, 2 or 3)
     -h, --help            print this help and exit
     -k, --fvek FVEK_FILE  decrypt volume using the FVEK directly
     -K, --vmk VMK_FILE    decrypt volume using the VMK directly
     -l, --logfile LOG_FILE
                           put messages into this file (stdout by default)
     -O, --offset OFFSET   BitLocker partition offset, in bytes (default is 0)
     -p, --recovery-password=[RECOVERY_PASSWORD]
                           decrypt volume using the recovery password method
     -q, --quiet           do NOT display anything
     -r, --readonly        do not allow one to write on the BitLocker volume
     -s, --stateok         do not check the volume's state, assume it's ok to mount it
     -u, --user-password=[USER_PASSWORD]
                           decrypt volume using the user password method
     -v, --verbosity       increase verbosity (CRITICAL errors are displayed by default)
     -V, --volume VOLUME   volume to get metadata and keys from
 
     --                    end of program options, beginning of FUSE's ones
 
   ARGS are any arguments you want to pass to FUSE. You need to pass at least
 the mount-point.
 
 ```
 
 - - -
 
 ##### dislocker-bek
 
 Reads .BEK files and prints information about them
 
 ```
 root@kali:~# dislocker-bek -h
 Usage: dislocker-bek [-h] [-f file.bek]
   Reads .BEK files and prints information about them
 ```
 
 - - -
 
 ##### dislocker-file
 
 Read BitLocker encrypted volumes under Linux, OSX and FreeBSD.
 
 ```
 root@kali:~# dislocker-file -h
 dislocker by Romain Coltel, v0.7.2 (compiled for Linux/x86_64)
 
 Usage: dislocker [-hqrsv] [-l LOG_FILE] [-O OFFSET] [-V VOLUME DECRYPTMETHOD -F[N]] [-- ARGS...]
     with DECRYPTMETHOD = -p[RECOVERY_PASSWORD]|-f BEK_FILE|-u[USER_PASSWORD]|-k FVEK_FILE|-K VMK_FILE|-c
 
 Options:
     -c, --clearkey        decrypt volume using a clear key (default)
     -f, --bekfile BEKFILE
                           decrypt volume using the bek file (on USB key)
     -F, --force-block=[N] force use of metadata block number N (1, 2 or 3)
     -h, --help            print this help and exit
     -k, --fvek FVEK_FILE  decrypt volume using the FVEK directly
     -K, --vmk VMK_FILE    decrypt volume using the VMK directly
     -l, --logfile LOG_FILE
                           put messages into this file (stdout by default)
     -O, --offset OFFSET   BitLocker partition offset, in bytes (default is 0)
     -p, --recovery-password=[RECOVERY_PASSWORD]
                           decrypt volume using the recovery password method
     -q, --quiet           do NOT display anything
     -r, --readonly        do not allow one to write on the BitLocker volume
     -s, --stateok         do not check the volume's state, assume it's ok to mount it
     -u, --user-password=[USER_PASSWORD]
                           decrypt volume using the user password method
     -v, --verbosity       increase verbosity (CRITICAL errors are displayed by default)
     -V, --volume VOLUME   volume to get metadata and keys from
 
     --                    end of program options, beginning of FUSE's ones
 
   ARGS are any arguments you want to pass to FUSE. You need to pass at least
 the mount-point.
 
 ```
 
 - - -
 
 ##### dislocker-find
 
 Find BitLocker-encrypted volumes.
 
 ```
 root@kali:~# dislocker-find -h
 Usage: /usr/bin/dislocker-find [-h] [files...]
   Try to find partitions which are BitLocker-encrypted. Each found is
    printed on stdout.
   If one or more file is passed as argument, /usr/bin/dislocker-find will print each
    file which is a BitLocker-encrypted volume.
   The number of partition found is returned (in $? in sh).
 ```
 
 - - -
 
 ##### dislocker-fuse
 
 Read/write BitLocker encrypted volumes under Linux, OSX and FreeBSD.
 
 ```
 root@kali:~# dislocker-fuse -h
 dislocker by Romain Coltel, v0.7.2 (compiled for Linux/x86_64)
 
 Usage: dislocker [-hqrsv] [-l LOG_FILE] [-O OFFSET] [-V VOLUME DECRYPTMETHOD -F[N]] [-- ARGS...]
     with DECRYPTMETHOD = -p[RECOVERY_PASSWORD]|-f BEK_FILE|-u[USER_PASSWORD]|-k FVEK_FILE|-K VMK_FILE|-c
 
 Options:
     -c, --clearkey        decrypt volume using a clear key (default)
     -f, --bekfile BEKFILE
                           decrypt volume using the bek file (on USB key)
     -F, --force-block=[N] force use of metadata block number N (1, 2 or 3)
     -h, --help            print this help and exit
     -k, --fvek FVEK_FILE  decrypt volume using the FVEK directly
     -K, --vmk VMK_FILE    decrypt volume using the VMK directly
     -l, --logfile LOG_FILE
                           put messages into this file (stdout by default)
     -O, --offset OFFSET   BitLocker partition offset, in bytes (default is 0)
     -p, --recovery-password=[RECOVERY_PASSWORD]
                           decrypt volume using the recovery password method
     -q, --quiet           do NOT display anything
     -r, --readonly        do not allow one to write on the BitLocker volume
     -s, --stateok         do not check the volume's state, assume it's ok to mount it
     -u, --user-password=[USER_PASSWORD]
                           decrypt volume using the user password method
     -v, --verbosity       increase verbosity (CRITICAL errors are displayed by default)
     -V, --volume VOLUME   volume to get metadata and keys from
 
     --                    end of program options, beginning of FUSE's ones
 
   ARGS are any arguments you want to pass to FUSE. You need to pass at least
 the mount-point.
 
 ```
 
 - - -
 
 ##### dislocker-metadata
 
 Printing information about a BitLocker-encrypted volume
 
 ```
 root@kali:~# dislocker-metadata -h
 Usage: dislocker [-hov] [-V VOLUME]
 
     -h         print this help and exit
     -o         partition offset
     -v         increase verbosity to debug level
     -V VOLUME  volume to get metadata from
 ```
 
 - - -
 
 ### libdislocker0-dev
 
  Dislocker has been designed to read BitLocker encrypted partitions under
  a Linux system. The driver used to read volumes encrypted in Windows system
  versions of the Vista to 10 and BitLocker-To-Go encrypted partitions, that's
  USB/FAT32 partitions.
   
  The software works with driver composed of a library, with multiple binaries
  using this library. Decrypting the partition, you have to give it a mount
  point where, once keys are decrypted, a file named dislocker-file appears.
  This file is a virtual NTFS partition, so you can mount it as any NTFS
  partition and then read from or write to it. Writing to the NTFS virtual
  file will change the underlying BitLocker partition content.
   
  This package provides the development files.
 
 **Installed size:** `136 KB`  
 **How to install:** `sudo apt install libdislocker0-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libdislocker0.7 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libdislocker0.7
 
  Dislocker has been designed to read BitLocker encrypted partitions under
  a Linux system. The driver used to read volumes encrypted in Windows system
  versions of the Vista to 10 and BitLocker-To-Go encrypted partitions, that's
  USB/FAT32 partitions.
   
  The software works with driver composed of a library, with multiple binaries
  using this library. Decrypting the partition, you have to give it a mount
  point where, once keys are decrypted, a file named dislocker-file appears.
  This file is a virtual NTFS partition, so you can mount it as any NTFS
  partition and then read from or write to it. Writing to the NTFS virtual
  file will change the underlying BitLocker partition content.
   
  This package provides the runtime library.
 
 **Installed size:** `139 KB`  
 **How to install:** `sudo apt install libdislocker0.7`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libmbedcrypto7 
 * libruby3.1 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
