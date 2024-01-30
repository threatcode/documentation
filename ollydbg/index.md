---
Title: ollydbg
Homepage: http://www.ollydbg.de/
Repository: https://gitlab.com/kalilinux/packages/ollydbg
Architectures: all
Version: 1.10-1kali5
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-reverse-engineering kali-tools-windows-resources 
Icon: images/ollydbg-logo.svg
PackagesInfo: |
 ### ollydbg
 
  OllyDbg is a 32-bit assembler level analysing debugger for
  Microsoft Windows. Emphasis on binary code analysis makes
  it particularly useful in cases where source is
  unavailable.
 
 **Installed size:** `2.50 MB`  
 **How to install:** `sudo apt install ollydbg`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 * wine
 {{< /spoiler >}}
 
 ##### ollydbg
 
 
 ```
 root@kali:~# ollydbg -h
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

```
wine /usr/share/ollydbg/OLLYDBG.EXE
```

![ollydbg](images/ollydbg-01.png)

![ollydbg](images/ollydbg-02-wget.png)
