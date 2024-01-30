---
Title: peass-ng
Homepage: https://github.com/carlospolop/PEASS-ng
Repository: https://gitlab.com/kalilinux/packages/peass-ng
Architectures: all
Version: 20231112.0a42c550-0kali1
Metapackages: kali-linux-everything kali-tools-vulnerability 
Icon: images/peass-ng-logo.svg
PackagesInfo: |
 ### peass
 
  Privilege escalation tools for Windows and Linux/Unix* and MacOS.
   
  These tools search for possible local privilege escalation paths that you could
  exploit and print them to you with nice colors so you can recognize the
  misconfigurations easily.
 
 **Installed size:** `57.92 MB`  
 **How to install:** `sudo apt install peass`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 {{< /spoiler >}}
 
 ##### linpeas
 
 
 ```
 root@kali:~# linpeas -h
 
 > peass ~ Privilege Escalation Awesome Scripts SUITE
 
 /usr/share/peass/linpeas
 |-- linpeas.sh
 |-- linpeas_darwin_amd64
 |-- linpeas_darwin_arm64
 |-- linpeas_fat.sh
 |-- linpeas_linux_386
 |-- linpeas_linux_amd64
 |-- linpeas_linux_arm
 `-- linpeas_linux_arm64
 ```
 
 - - -
 
 ##### peass
 
 
 ```
 root@kali:~# peass -h
 
 > peass ~ Privilege Escalation Awesome Scripts SUITE
 
 /usr/share/peass/
 |-- linpeas
 |   |-- linpeas.sh
 |   |-- linpeas_darwin_amd64
 |   |-- linpeas_darwin_arm64
 |   |-- linpeas_fat.sh
 |   |-- linpeas_linux_386
 |   |-- linpeas_linux_amd64
 |   |-- linpeas_linux_arm
 |   `-- linpeas_linux_arm64
 `-- winpeas
     |-- winPEAS.bat
     |-- winPEASany.exe
     |-- winPEASany_ofs.exe
     |-- winPEASx64.exe
     |-- winPEASx64_ofs.exe
     |-- winPEASx86.exe
     `-- winPEASx86_ofs.exe
 ```
 
 - - -
 
 ##### winpeas
 
 
 ```
 root@kali:~# winpeas -h
 
 > peass ~ Privilege Escalation Awesome Scripts SUITE
 
 /usr/share/peass/winpeas
 |-- winPEAS.bat
 |-- winPEASany.exe
 |-- winPEASany_ofs.exe
 |-- winPEASx64.exe
 |-- winPEASx64_ofs.exe
 |-- winPEASx86.exe
 `-- winPEASx86_ofs.exe
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
