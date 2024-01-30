---
Title: exe2hexbat
Homepage: https://github.com/g0tmi1k/exe2hex/
Repository: https://gitlab.com/kalilinux/packages/exe2hexbat
Architectures: all
Version: 1.5.1-0kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-post-exploitation 
Icon: images/exe2hexbat-logo.svg
PackagesInfo: |
 ### exe2hexbat
 
  A Python script to convert a Windows PE executable file to a batch file and
  vice versa.
 
 **Installed size:** `37 KB`  
 **How to install:** `sudo apt install exe2hexbat`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### exe2hex
 
 
 ```
 root@kali:~# exe2hex -h
 [*] exe2hex v1.5.1
 Usage: exe2hex [options]
 
 Options:
   -h, --help  show this help message and exit
   -x EXE      The EXE binary file to convert
   -s          Read from STDIN
   -b BAT      BAT output file (DEBUG.exe method - x86)
   -p POSH     PoSh output file (PowerShell method - x86/x64)
   -e          URL encode the output
   -r TEXT     pRefix - text to add before the command on each line
   -f TEXT     suFfix - text to add after the command on each line
   -l INT      Maximum HEX values per line
   -c          Clones and compress the file before converting (-cc for higher
               compression)
   -t          Create a Expect file, to automate to a Telnet session.
   -w          Create a Expect file, to automate to a WinEXE session.
   -v          Enable verbose mode
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
