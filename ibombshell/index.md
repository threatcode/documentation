---
Title: ibombshell
Homepage: https://github.com/Telefonica/ibombshell
Repository: https://gitlab.com/kalilinux/packages/ibombshell
Architectures: all
Version: 0~git20201107-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ibombshell
 
  This package contains a tool written in Powershell that allows you to have a
  prompt at any time with post-exploitation functionalities (and in some cases
  exploitation). It is a shell that is downloaded directly to memory providing
  access to a large number of pentesting features. These functionalities can be
  downloaded directly to memory, in the form of a Powershell function. This form
  of execution is known as everywhere.
   
  In addition, ibombshell provides a second execution mode called Silently, so
  the pentester can execute an instance of ibombshell (called warrior). The
  compromised computer will be connected to a C2 panel through HTTP. Therefore,
  it will be possible to control the warrior and be able to load functions in
  memory that help the pentester. This is happening whithin the
  post-exploitation phase.
 
 **Installed size:** `4.94 MB`  
 **How to install:** `sudo apt install ibombshell`  
 
 {{< spoiler "Dependencies:" >}}
 * powershell
 * python3-pynput
 * python3-termcolor
 {{< /spoiler >}}
 
 ##### ibombshell
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
