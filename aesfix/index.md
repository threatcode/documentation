---
Title: aesfix
Homepage: https://citp.princeton.edu/our-work/memory/code/
Repository: https://salsa.debian.org/pkg-security-team/aesfix
Architectures: any
Version: 1.0.1-8
Metapackages: kali-linux-everything kali-tools-crypto-stego 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### aesfix
 
  This program illustrates a technique for correcting bit errors in an AES
  key schedule. It should be used with the output of the aeskeyfind program.
   
  It is limited to AES-128 key schedules, and it can only correct unidirectional
  1->0 bit errors.  For the most part it has been optimized for readability
  rather than performance.
   
  This package is useful to several activities, as forensics investigations.
 
 **Installed size:** `41 KB`  
 **How to install:** `sudo apt install aesfix`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### aesfix
 
 Correct bit errors in an AES key schedules
 
 ```
 root@kali:~# man aesfix
 aesfix(1)                        User Commands                       aesfix(1)
 
 NAME
        aesfix - Correct bit errors in an AES key schedules
 
 SYNOPSIS
        aesfix SCHEDULE-FILE
 
 DESCRIPTION
        Corrects bit errors in an AES key schedule read from the specified hex-
        encoded file.
 
 BUGS
        Likely.
 
 SEE ALSO
        biosmemimage(1), aeskeyfind(1) aesfix(1)
 
 AUTHOR
        aesfix was written by Nadia Heninger and J. Alex Halderman.
 
        This manual page was written by Jacob Appelbaum <jacob@appelbaum.net>
        for the Debian system (but may be used by others).  Permission is
        granted to copy, distribute and/or modify this document under the terms
        of the GNU General Public License, Version 2 or any later version pub-
        lished by the Free Software Foundation.
 
 User Commands                     08-17-2008                         aesfix(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
