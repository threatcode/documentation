---
Title: multimac
Homepage: https://sourceforge.net/projects/multimac/
Repository: https://gitlab.com/kalilinux/packages/multimac
Architectures: any
Version: 1.0.3-1kali3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### multimac
 
  Multimac is a linux virtual ethernet tap allocator to
  emulate and use multiple virtual interfaces (with different
  MAC addresses) on a LAN using a single network adapter.
 
 **Installed size:** `28 KB`  
 **How to install:** `sudo apt install multimac`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### multimac
 
 
 ```
 root@kali:~# multimac -h
 Usage: multimac <number of taps>
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
