---
Title: shellter
Homepage: https://www.shellterproject.com/
Repository: https://gitlab.com/kalilinux/packages/shellter
Architectures: i386 amd64
Version: 7.2-0kali2
Metapackages: kali-linux-everything kali-tools-post-exploitation kali-tools-windows-resources 
Icon: images/shellter-logo.svg
PackagesInfo: |
 ### shellter
 
  Shellter is a dynamic shellcode injection tool aka dynamic PE infector. It can
  be used in order to inject shellcode into native Windows applications
  (currently 32-bit apps only). The shellcode can be something yours or
  something generated through a framework, such as Metasploit.
   
  Shellter takes advantage of the original structure of the PE file and doesn't
  apply any  modification such as changing memory access permissions in sections
  (unless the user wants to), adding an extra section with RWE access, and
  whatever would look dodgy under an AV scan.
 
 **Installed size:** `726 KB`  
 **How to install:** `sudo apt install shellter`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 * wine
 {{< /spoiler >}}
 
 ##### shellter
 
 
 ```
 root@kali:~# shellter -h
 ┏━(Message from Kali developers)
 ┃
 ┃ You may need to install the wine32 package first:
 ┃  # dpkg --add-architecture i386 && apt update && apt -y install wine32
 ┃
 ┗━
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

![shellter](images/shellter.png)

## shellter Usage Examples

```
root@kali:~# dpkg --add-architecture i386
root@kali:~# apt update && apt install wine32
root@kali:~# shellter
```
