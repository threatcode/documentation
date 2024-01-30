---
Title: code-oss
Homepage: https://github.com/microsoft/vscode
Repository: https://gitlab.com/kalilinux/packages/code-oss
Architectures: amd64 arm64
Version: 1.82.2+ds-0kali2
Metapackages: kali-linux-everything kali-linux-large 
Icon: images/code-oss-logo.svg
PackagesInfo: |
 ### code-oss
 
  This package contains code-oss, a code editor with what developers need for
  their core edit-build-debug cycle. It provides comprehensive code editing,
  navigation, and understanding support along with lightweight debugging, a rich
  extensibility model, and lightweight integration with existing tools.
   
  This package is built from Microsoft open source code named code-oss.
 
 **Installed size:** `319.18 MB`  
 **How to install:** `sudo apt install code-oss`  
 
 {{< spoiler "Dependencies:" >}}
 * nodejs
 {{< /spoiler >}}
 
 ##### code
 
 
 ```
 root@kali:~# code -h
 ┏━(Message from Kali developers)
 ┃ code is not the binary you may be expecting.
 ┃ You are looking for \"code-oss\"
 ┃ Starting code-oss for you...
 ┗━
 ```
 
 - - -
 
 ##### code-oss
 
 
 
 - - -
 
 ##### vscode
 
 
 ```
 root@kali:~# vscode -h
 ┏━(Message from Kali developers)
 ┃ vscode is not the binary you may be expecting.
 ┃ You are looking for \"code-oss\"
 ┃ Starting code-oss for you...
 ┗━
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
