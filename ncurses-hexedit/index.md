---
Title: ncurses-hexedit
Homepage: http://www.rogoyski.com/adam/programs/hexedit/
Repository: https://salsa.debian.org/debian/ncurses-hexedit
Architectures: any
Version: 0.9.7+orig-7.2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ncurses-hexedit
 
  Hexedit is a file editor which allows editing and viewing a file in
  hexadecimal, along with its ASCII or EBCDIC text equivalent.  Standard
  editing features include insert, delete, search (text or byte searches),
  highlighted changes,  undo, two different viewing formats, and full
  screen text snapshots.  Allows editing of fixed disks as well.  Includes
  a binary/octal/decimal/hex converter.
 
 **Installed size:** `130 KB`  
 **How to install:** `sudo apt install ncurses-hexedit`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libncurses6 
 * libtinfo6 
 {{< /spoiler >}}
 
 ##### hexeditor
 
 Full screen curses Hex editor
 
 ```
 root@kali:~# hexeditor -h
 [N]Curses Hexedit 0.9.7 by Adam Rogoyski <apoc@laker.net>
 Copyright (C) 1998, 1999 Adam Rogoyski
 This is free software; see the source for copying conditions.
 There is NO warranty; not even for MERCHANTABILITY or FITNESS FOR A
 PARTICULAR PURPOSE.
 
 Usage: hexeditor [options] [file]
 Options:
   -h, --help              Print this message and exit.
   -8, --highbit           Print high order 8-bit text.
   -a, --alltext           Print all text characters.
   -b, --buffer            Buffer the entire file in memory.
                             Much faster and enables insert/delete.
   -d, --disk              Edit a fixed disk, i.e. /dev/hda (Read-only)
   -f, --force             Force editing of disk.
                             Needed to write to disks.
   -n, --nocolor           Force Gray scale, no colors.
   -q, --quiet             Quiet Mode, No annoying beeping
   -r, --readonly          Do no modifying of the file.
   -v, --version           Print the version number and exit.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
