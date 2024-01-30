---
Title: kali-defaults
Homepage: https://www.kali.org
Repository: https://gitlab.com/kalilinux/packages/kali-defaults
Architectures: all
Version: 2023.4.2
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-database kali-tools-forensics kali-tools-information-gathering kali-tools-passwords kali-tools-post-exploitation kali-tools-respond kali-tools-reverse-engineering kali-tools-vulnerability kali-tools-web kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### kali-defaults
 
  This package implements various default settings within Kali.
   
  The size of this package (including its dependencies) should be rather limited
  because it is included in all Kali images, even minimalistic ones such as
  docker images.
 
 **Installed size:** `1.23 MB`  
 **How to install:** `sudo apt install kali-defaults`  
 
 ##### kali-deprecated
 
 
 ```
 root@kali:~# kali-deprecated -h
 [-] ERROR: Missing commands. /usr/bin/kali-deprecated <old-command> <new-command> [<url>]
 ```
 
 - - -
 
 ##### kali-motd
 
 
 
 - - -
 
 ##### kali-setup
 
 
 ```
 root@kali:~# kali-setup -h
 ┏━(Message from Kali developers)
 ┃
 ┃ The command kali-setup is deprecated. Please use kali-tweaks instead.
 ┃
 ┗━
 ```
 
 - - -
 
 ##### kali-treecd
 
 
 
 - - -
 
 ##### kali-winexec
 
 
 
 - - -
 
 ### kali-defaults-desktop
 
  This package implements a subset of various default settings within Kali, in
  particular those that are used by graphical desktops.
   
  The purpose of this package is mainly to host all configuration changes that
  have a high cost in terms of diskspace due to the size of the dependencies.
  This includes notably all gsettings overrides.
 
 **Installed size:** `27 KB`  
 **How to install:** `sudo apt install kali-defaults-desktop`  
 
 {{< spoiler "Dependencies:" >}}
 * dconf-gsettings-backend | gsettings-backend
 * kali-defaults
 * libglib2.0-bin
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
