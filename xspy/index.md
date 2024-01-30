---
Title: xspy
Homepage: https://www.kali.org
Repository: https://gitlab.com/kalilinux/packages/xspy
Architectures: any
Version: 1.1-1kali4
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### xspy
 
  Sniffs keystrokes on remote or local
  X-Windows servers.
 
 **Installed size:** `25 KB`  
 **How to install:** `sudo apt install xspy`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libx11-6
 {{< /spoiler >}}
 
 ##### xspy
 
 
 ```
 root@kali:~# xspy -h
 xspy: can't open display -h:0
 blah.... 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## xspy Usage Example

```
root@kali:~# xspy
opened :0.0 for snoopng

id
idBackSpaceBackSpacels
whoami
```
