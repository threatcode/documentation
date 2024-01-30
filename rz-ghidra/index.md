---
Title: rz-ghidra
Homepage: https://github.com/rizinorg/rz-ghidra
Repository: https://gitlab.com/kalilinux/packages/rz-ghidra
Architectures: amd64 arm64 armhf i386 mipsel
Version: 0.6.0-0kali1
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-hardware kali-tools-respond kali-tools-reverse-engineering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rz-ghidra
 
  This is an integration of the Ghidra decompiler and Sleigh Disassembler
  for rizin. It is solely based on the decompiler part of Ghidra, which is
  written entirely in C++, so Ghidra itself is not required at all and the
  plugin can be built self-contained.
 
 **Installed size:** `427.63 MB`  
 **How to install:** `sudo apt install rz-ghidra`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libqt5core5a 
 * librizin0 
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
