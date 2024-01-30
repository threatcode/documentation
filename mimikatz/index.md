---
Title: mimikatz
Homepage: https://blog.gentilkiwi.com/mimikatz
Repository: https://gitlab.com/kalilinux/packages/mimikatz
Architectures: all
Version: 2.2.0-git20220919-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords kali-tools-post-exploitation kali-tools-windows-resources 
Icon: images/mimikatz-logo.svg
PackagesInfo: |
 ### mimikatz
 
  Mimikatz uses admin rights on Windows to display passwords of currently logged
  in users in plaintext.
 
 **Installed size:** `2.54 MB`  
 **How to install:** `sudo apt install mimikatz`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 {{< /spoiler >}}
 
 ##### mimikatz
 
 
 ```
 root@kali:~# mimikatz -h
 
 > mimikatz ~ Uses admin rights on Windows to display passwords in plaintext
 
 /usr/share/windows-resources/mimikatz
 |-- Win32
 |   |-- mimidrv.sys
 |   |-- mimikatz.exe
 |   |-- mimilib.dll
 |   |-- mimilove.exe
 |   `-- mimispool.dll
 |-- kiwi_passwords.yar
 |-- mimicom.idl
 `-- x64
     |-- mimidrv.sys
     |-- mimikatz.exe
     |-- mimilib.dll
     `-- mimispool.dll
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
