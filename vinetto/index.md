---
Title: vinetto
Homepage: https://github.com/AtesComp/Vinetto
Repository: https://salsa.debian.org/pkg-security-team/vinetto
Architectures: all
Version: 1:0.8.0-3
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### vinetto
 
  vinetto is a console program to extract thumbnail pictures and their metadata
  from Thumbs.db files, that are generated under Microsoft Windows.
   
  vinetto can help *nix-based forensics investigators to:
   
    - easily preview thumbnails of deleted pictures on Windows systems;
    - obtain information (dates, path, ...) about deleted pictures.
 
 **Installed size:** `76 KB`  
 **How to install:** `sudo apt install vinetto`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-pil
 * python3-setuptools
 {{< /spoiler >}}
 
 ##### vinetto
 
 Extract thumbnails and associated metadata from Thumbs.db files
 
 ```
 root@kali:~# vinetto -h
 usage: vinetto [-h] [--version] [-o DIR] [-H] [-U] [-q] [-s] thumbfile
 
 Vinetto - The Thumbnail File Parser
 
 positional arguments:
   thumbfile   an input thumbnail file, like "Thumb.db"
 
 options:
   -h, --help  show this help message and exit
   --version   show program's version number and exit
   -o DIR      write thumbnails to DIR
   -H          write html report to DIR (requires option -o)
   -U          use utf8 encodings
   -q          quiet output
   -s          create symlink from the the image realname to the numbered name
               in DIR/.thumbs (requires option -o)
               NOTE: A Catalog containing the realname must exist for this
                     option to produce results
 
 --- Vinetto 0.8.0 ---
 Based on the original Vinetto by Michel Roukine
 Updated by Keven L. Ates
 Vinetto is open source software
   See: https://github.com/AtesComp/Vinetto
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
