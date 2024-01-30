---
Title: mfterm
Homepage: https://github.com/4ZM/mfterm
Repository: https://gitlab.com/kalilinux/packages/mfterm
Architectures: any
Version: 1.0.7+git20190127-0kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-rfid kali-tools-wireless 
Icon: images/mfterm-logo.svg
PackagesInfo: |
 ### mfterm
 
  mfterm is a terminal interface for working with Mifare Classic tags.
  Tab completion on commands is available. Also, commands that have file name
  arguments provide tab completion on files. There is also a command history,
  like in most normal shells.
 
 **Installed size:** `106 KB`  
 **How to install:** `sudo apt install mfterm`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnfc6 
 * libreadline8 
 * libssl3 
 {{< /spoiler >}}
 
 ##### mfterm
 
 The Mifare Terminal
 
 ```
 root@kali:~# mfterm -h
 A terminal interface for working with Mifare Classic tags.
 Usage: mfterm [-v] [-h] [-k keyfile]
 
 Options: 
   --help          (-h)   Show this help message.
   --version       (-v)   Display version information.
   --tag=tagfile   (-t)   Load a tag from the specified file.
   --keys=keyfile  (-k)   Load keys from the specified file.
   --dict=dictfile (-d)   Load dictionary from the specified file.
 
 Report bugs to: anders@4zm.org
 mfterm home page: <https://github.com/4zm/mfterm>
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
