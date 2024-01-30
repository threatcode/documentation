---
Title: havoc
Homepage: https://github.com/HavocFramework/Havoc
Repository: https://gitlab.com/kalilinux/packages/havoc
Architectures: amd64
Version: 0.6~git20231012.08a8826-0kali1
Metapackages: kali-linux-everything 
Icon: images/havoc-logo.svg
PackagesInfo: |
 ### havoc
 
  Havoc is a modern and malleable post-exploitation command and control framework
 
 **Installed size:** `19.90 MB`  
 **How to install:** `sudo apt install havoc`  
 
 {{< spoiler "Dependencies:" >}}
 * gcc-mingw-w64-i686-win32
 * gcc-mingw-w64-x86-64-win32
 * libc6 
 * libfmt9 
 * libgcc-s1 
 * libpython3.11 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5sql5 
 * libqt5websockets5 
 * libqt5widgets5 
 * libspdlog1.12-fmt9
 * libstdc++6 
 * nasm
 {{< /spoiler >}}
 
 ##### havoc
 
 
 ```
 root@kali:~# havoc -h
 Havoc Framework [Version: 0.6] [CodeName: Hierophant Green]
 
 Usage:
   havoc [flags]
   havoc [command]
 
 Available Commands:
   client      client command
   help        Help about any command
   server      teamserver command
 
 Flags:
   -h, --help   help for havoc
 
 Use "havoc [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
