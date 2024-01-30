---
Title: hyperion
Homepage: http://www.nullsecurity.net/tools/binary.html
Repository: https://gitlab.com/kalilinux/packages/hyperion
Architectures: all
Version: 2.0-0kali4
Metapackages: kali-linux-everything kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hyperion
 
  This package contains a runtime encrypter for 32-bit portable executables. It
  is a reference implementation and bases on the paper "Hyperion: Implementation
  of a PE-Crypter". The paper describes the implementation details which
  aren't in the scope of this readme file.
  The crypter is started via the command line and encrypts an input executable
  with AES-128. The encrypted file decrypts itself on startup (bruteforcing the
  AES key which may take a few seconds) and generates a log file for debug
  purpose.
 
 **Installed size:** `1.17 MB`  
 **How to install:** `sudo apt install hyperion`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
