---
Title: rfdump
Homepage: http://www.rfdump.org/
Repository: https://salsa.debian.org/pkg-security-team/rfdump
Architectures: any
Version: 1.6-9.1
Metapackages: kali-linux-everything kali-tools-rfid kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rfdump
 
  RFDump is a tool to decode RFID tags and show their meta information:
  tag ID, tag type, manufacturer etc. The user data memory of a tag can
  be displayed and modified using either a hex or an ASCII editor. In
  addition, the integrated cookie feature demonstrates how easy it is
  for a company to abuse RFID technology to spy on their customers.
  RFDump works with the ACG multi-tag reader or similar card reader
  hardware.
 
 **Installed size:** `250 KB`  
 **How to install:** `sudo apt install rfdump`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libexpat1 
 * libglib2.0-0 
 * libgtk-3-0 
 {{< /spoiler >}}
 
 ##### rfdump
 
 Tool to detect RFID-Tags and show their meta information
 
 ```
 root@kali:~# man rfdump
 RFDUMP(1)                   General Commands Manual                  RFDUMP(1)
 
 NAME
        rfdump -- Tool to detect RFID-Tags and show their meta information
 
 SYNOPSIS
        rfdump [-p /dev/ttyS?]  [--setupreader]  [file.xml]
 
 DESCRIPTION
        This manual page documents briefly the rfdump command.
 
        This  manual  page  was written for the Debian distribution because the
        original program does not have a manual page.
 
        rfdump is a tool to detect RFID-Tags and show their  meta  information:
        Tag  ID, Tag Type, manufacturer etc. The User-Data of a tag can be dis-
        played and modified using either a Hex or an ASCII editor. In addition,
        the integrated cookie feature demonstrates how easy it is for a company
        to abuse RFID technology to spy on their customers.  rfdump works  with
        the ACG Multi-Tag Reader or similar card reader hardware.
 
 OPTIONS
        -h           --help
                  Show summary of options.
 
        -p        specify port to use
 
        --setupreader
                  setup the card reader
 
 FILES
        ~/.config/rfdump.ini
                  rfdump configuration file
 
 FURTHER DOCUMENTATION
        Further documentation can be found under /usr/share/doc/rfdump.
 
 AUTHOR
        This  manual page was written by Meike Reichle <meike@alphascorpii.net>
        for the Debian system (but may  be  used  by  others).   Permission  is
        granted to copy, distribute and/or modify this document under the terms
        of  the  GNU  General  Public License, Version 2 any later version pub-
        lished by the Free Software Foundation.
 
        On Debian systems, the complete text of the GNU General Public  License
        can be found in /usr/share/common-licenses/GPL.
 
                                                                      RFDUMP(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
