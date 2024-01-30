---
Title: imhex
Homepage: https://github.com/WerWolv/ImHex
Repository: https://gitlab.com/kalilinux/packages/imhex
Architectures: amd64 arm64
Version: 1.31.0+ds-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### imhex
 
  This package contains a Hex Editor for Reverse Engineers, Programmers and
  people who value their retinas when working at 3 AM.
 
 **Installed size:** `38.57 MB`  
 **How to install:** `sudo apt install imhex`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcurl4 
 * libdbus-1-3 
 * libfreetype6 
 * libgcc-s1 
 * libglfw3 
 * libmagic1 
 * libmbedcrypto7 
 * libopengl0
 * libstdc++6 
 * libyara10 
 {{< /spoiler >}}
 
 ##### imhex
 
 
 ```
 root@kali:~# imhex --help
 ImHex - A Hex Editor for Reverse Engineers, Programmers and people who value their retinas when working at 3 AM.
 
 usage: imhex [subcommand] [options]
 Available subcommands:
     --help           Print help about this command
     --version        Print ImHex version
     --plugins        Lists all plugins that have been installed
     --open           Open files passed as argument. [default]
     --calc           Evaluate a mathematical expression
     --hash           Calculate the hash of a file
     --encode         Encode a string
     --decode         Decode a string
     --magic          Identify file types
     --pl             Interact with the pattern language
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
