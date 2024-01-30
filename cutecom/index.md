---
Title: cutecom
Homepage: https://gitlab.com/cutecom/cutecom
Repository: 
Architectures: any
Version: 0.51.0-1
Metapackages: kali-linux-everything kali-tools-hardware 
Icon: images/cutecom-logo.svg
PackagesInfo: |
 ### cutecom
 
  Cutecom is a graphical serial terminal, like minicom.
  It is aimed mainly at hardware developers or other people who need a
  terminal to talk to their devices. It features lineoriented interface
  instead of character-oriented, xmodem, ymodem, zmodem support
  (requires the lrzsz package) and hexadecimal input and output among
  other things.
  It is written using the Qt library originally by Trolltech (www.trolltech.com).
 
 **Installed size:** `755 KB`  
 **How to install:** `sudo apt install cutecom`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5serialport5 
 * libqt5widgets5 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### cutecom
 
 Graphical serial terminal.
 
 ```
 root@kali:~# man cutecom
 CUTECOM(1)                  General Commands Manual                 CUTECOM(1)
 
 NAME
        cutecom - graphical serial terminal.
 
 SYNOPSIS
        cutecom
 
 DESCRIPTION
        CuteCom  is  a  graphical  serial  terminal, like minicom.  It is aimed
        mainly at hardware developers or other people who need  a  terminal  to
        talk  to their devices. It features a lineoriented interface instead of
        character-oriented, xmodem, ymodem, zmodem support (requires the  lrzsz
        package) and hexadecimal input and output among other things.
 
 OPTIONS
        -h, --help
               prints a short help message
 
        -s, --session <session_name>
               opens  a  previously defined session. A new Session with default
               connection parameters is created when a session with  this  name
               can not be found in the config file
 
 FILES
        ~/.config/CuteCom/CuteCom5.conf
               Personal  CuteCom configuration file (with sessions stored there
               also).
 
 SEE ALSO
        minicom(1), sz(1).
 
 AUTHOR
        CuteCom was originally written by Alexander Neundorf <neundorf@kde.org>
        and is now maintained by Meinhard Ritscher <cyc1ingsir@gmail.com>.
 
        This manual page was written by Roman I Khimov  <roman@khimov.ru>,  for
        the Debian project (but may be used by others).
 
                               September 30, 2016                    CUTECOM(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
