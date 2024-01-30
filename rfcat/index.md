---
Title: rfcat
Homepage: https://github.com/atlas0fd00m/rfcat
Repository: https://gitlab.com/kalilinux/packages/rfcat
Architectures: any
Version: 1:2.0.1-0kali1
Metapackages: kali-linux-everything kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rfcat
 
  Rfcat is a sub GHz analysis tool. The goals of the project are to reduce the
  time for security researchers to create needed tools for analyzing unknown
  targets, to aid in reverse-engineering of hardware.
 
 **Installed size:** `443 KB`  
 **How to install:** `sudo apt install rfcat`  
 
 {{< spoiler "Dependencies:" >}}
 * ipython3
 * python3
 * python3-future
 * python3-ipython
 * python3-numpy
 * python3-pyside2.qtcore
 * python3-pyside2.qtgui
 * python3-pyside2.qtwidgets
 * python3-serial
 * python3-usb
 {{< /spoiler >}}
 
 ##### rfcat
 
 (unknown subject)
 
 ```
 root@kali:~# rfcat -h
 usage: rfcat [-h] [-r] [-i INDEX] [-s] [-f CENTFREQ] [-c INC] [-n SPECCHANS]
              [--bootloader] [--force] [-S]
 
 options:
   -h, --help            show this help message and exit
   -r, --research        Interactive Python and the "d" instance to talk to
                         your dongle. melikey longtime.
   -i INDEX, --index INDEX
   -s, --specan          start spectrum analyzer
   -f CENTFREQ, --centfreq CENTFREQ
   -c INC, --inc INC
   -n SPECCHANS, --specchans SPECCHANS
   --bootloader          trigger the bootloader (use in order to flash the
                         dongle)
   --force               use this to make sure you want to set bootloader mode
                         (you *must* flash after setting --bootloader)
   -S, --safemode        TROUBLESHOOTING ONLY, used with -r
 ```
 
 - - -
 
 ##### rfcat_bootloader
 
 
 ```
 root@kali:~# rfcat_bootloader -h
 
 CC Bootloader Download Utility
 
 Usage:  /usr/bin/rfcat_bootloader serial_port command
 
 Commands:
 
   download <hex_file>
 
     Download hex_file to the device.
     
   run
 
     Run the user code.
     
   reset
 
     The bootloader will not erase pages that have previously been written to
     before writing new data to that page. This allows for random access writes
     but prevents you from overwriting downloaded code unless the device is
     power cycled. This command will reset the bootloader's record of what
     pages have been written to, allowing you to overwrite without power 
     cycling.
     
   erase_all
 
     Erases the entire user flash area.
     
   erase <n>
 
     Erases page n of the flash memory (organised into 1024 byte pages). The
     bootloader occupies the first few pages and the rest are reserved for user
     code. Attempting to erase a bootloader page will have no effect. To
     determine which page the user code starts on please check the
     USER_CODE_BASE setting in main.h.
     
   read <start_addr> <len> [hex_file]
 
     Reads len bytes from flash memory starting from start_addr and optionally
     write to hex_file. start_addr and len should be specified in hexadecimal 
     (e.g. 0x1234).
 
   verify <hex_file>
 
     Verify hex_file matches device flash memory.
   
 ```
 
 - - -
 
 ##### rfcat_msfrelay
 
 
 ```
 root@kali:~# rfcat_msfrelay -h
 usage: rfcat_msfrelay [-h] [-i INDEX] [-u USER] [-p PASSWORD] [-P PORT]
                       [--noauth] [--localonly]
 
 options:
   -h, --help            show this help message and exit
   -i INDEX, --index INDEX
   -u USER, --user USER  HTTP Username
   -p PASSWORD, --password PASSWORD
                         HTTP Password
   -P PORT, --Port PORT
   --noauth              Do not require authentication
   --localonly           Listen on localhost only
 ```
 
 - - -
 
 ##### rfcat_server
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
