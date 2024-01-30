---
Title: rsakeyfind
Homepage: https://citp.princeton.edu/our-work/memory/code/
Repository: https://salsa.debian.org/pkg-security-team/rsakeyfind
Architectures: any
Version: 1:1.0-8
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rsakeyfind
 
  rsakeyfind is a tool that locates BER-encoded RSA private keys in MEMORY-IMAGE.
  If a MODULUS-FILE is specified, it will locate private and public keys matching
  the hex-encoded modulus read from this file.
   
  This package is useful to several activities, as forensics investigations.
 
 **Installed size:** `34 KB`  
 **How to install:** `sudo apt install rsakeyfind`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### rsakeyfind
 
 Locates BER-encoded RSA private keys in memory images.
 
 ```
 root@kali:~# man rsakeyfind
 rsakeyfind(1)                    User Commands                   rsakeyfind(1)
 
 NAME
        rsakeyfind - Locates BER-encoded RSA private keys in memory images.
 
 SYNOPSIS
        rsakeyfind MEMORY-IMAGE [MODULUS-FILE]
 
 DESCRIPTION
        rsakeyfind  is a tool that locates BER-encoded RSA private keys in MEM-
        ORY-IMAGE.  If a MODULUS-FILE is specified, it will locate private  and
        public keys matching the hex-encoded modulus read from this file.
 
 BUGS
        Likely.
 
 SEE ALSO
        aesfix(1), biosmemimage(1), aeskeyfind(1)
 
 AUTHOR
        rsakeyfind was written by Nadia Heninger and J. Alex Halderman.
 
        This manual page was written by Jacob Appelbaum <jacob@appelbaum.net>
        for the Debian system (but may be used by others).  Permission is
        granted to copy, distribute and/or modify this document under the terms
        of the GNU General Public License, Version 2 or any later version pub-
        lished by the Free Software Foundation.
 
 User Commands                     08-17-2008                     rsakeyfind(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
