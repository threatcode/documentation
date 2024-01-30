---
Title: passdetective
Homepage: https://github.com/aydinnyunus/PassDetective
Repository: https://gitlab.com/kalilinux/packages/passdetective
Architectures: any
Version: 1.0.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### passdetective
 
  This package contains a command-line tool that scans the shell command
  history for mistakenly written passwords, API keys, and secrets. It uses
  regular expressions to identify potential sensitive information and helps
  avoid accidentally exposing sensitive data in the command history.
 
 **Installed size:** `3.34 MB`  
 **How to install:** `sudo apt install passdetective`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### PassDetective
 
 
 ```
 root@kali:~# PassDetective -h
 The "extract" command allows you to automatically extract passwords from shell history change descriptions.
 By analyzing the history of shell commands, this tool can identify and extract passwords that were used during
 previous commands and display them for further inspection or use.
 
 Usage:
   PassDetective [flags]
   PassDetective [command]
 
 Available Commands:
   completion  Generate the autocompletion script for the specified shell
   extract     Extract passwords from shell history
   help        Help about any command
 
 Flags:
   -h, --help   Help message for PassDetective
 
 Use "PassDetective [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
