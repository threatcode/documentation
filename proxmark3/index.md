---
Title: proxmark3
Homepage: https://github.com/RfidResearchGroup/proxmark3
Repository: https://gitlab.com/kalilinux/packages/proxmark3
Architectures: any all
Version: 4.16191-0kali1
Metapackages: kali-linux-everything kali-tools-rfid kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### proxmark3
 
  This package contains the client and tools for the Proxmark3. It is
  dedicated to bringing the most out of the new features for Proxmark3 RDV4.0
  new hardware and design but it will also support older hardware revisions.
 
 **Installed size:** `4.03 MB`  
 **How to install:** `sudo apt install proxmark3`  
 
 {{< spoiler "Dependencies:" >}}
 * libbluetooth3 
 * libbz2-1.0
 * libc6 
 * libgcc-s1 
 * libjansson4 
 * liblua5.2-0 
 * libpython3.11 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5widgets5 
 * libreadline8 
 * libssl3 
 * libstdc++6 
 * libwhereami0 
 * proxmark3-common 
 * proxmark3-firmwares 
 {{< /spoiler >}}
 
 ##### proxmark3
 
 
 ```
 root@kali:~# proxmark3 -h
 
 syntax: proxmark3 [-h|-t|-m|--fulltext]
         proxmark3 [[-p] <port>] [-b] [-w] [-f] [-c <command>]|[-l <lua_script_file>]|[-y <python_script_file>]|[-s <cmd_script_file>] [-i] [-d <0|1|2>]
         proxmark3 [-p] <port> --flash [--unlock-bootloader] [--image <imagefile>]+ [-w] [-f] [-d <0|1|2>]
 
 Common options:
       -h/--help                           this help
       -v/--version                        print client version
       -p/--port                           serial port to connect to
       -w/--wait                           20sec waiting the serial port to appear in the OS
       -f/--flush                          output will be flushed after every print
       -d/--debug <0|1|2>                  set debugmode
 
 Options in client mode:
       -t/--text                           dump all interactive command list at once
       --fulltext                          dump all interactive command's help at once
       -m/--markdown                       dump all interactive command list at once in markdown syntax
       -b/--baud                           serial port speed (only needed for physical UART, not for USB-CDC or BT)
       -c/--command <command>              execute one Proxmark3 command (or several separated by ';').
       -l/--lua <lua_script_file>          execute Lua script.
       -y/--py <python_script_file>        execute Python script.
       -s/--script-file <cmd_script_file>  script file with one Proxmark3 command per line
       -i/--interactive                    enter interactive mode after executing the script or the command
       --incognito                         do not use history, prefs file nor log files
 
 Options in flasher mode:
       --flash                             flash Proxmark3, requires at least one --image
       --reboot-bootloader                 reboot Proxmark3 into bootloader mode
       --unlock-bootloader                 Enable flashing of bootloader area *DANGEROUS* (need --flash)
       --force                             Enable flashing even if firmware seems to not match client version
       --image <imagefile>                 image to flash. Can be specified several times.
 
 Examples:
 
   to run Proxmark3 client:
 
       proxmark3 /dev/ttyACM0                       -- runs the pm3 client
       proxmark3 /dev/ttyACM0 -f                    -- flush output every time
       proxmark3 /dev/ttyACM0 -w                    -- wait for serial port
       proxmark3                                    -- runs the pm3 client in OFFLINE mode
 
   to execute different commands from terminal:
 
       proxmark3 /dev/ttyACM0 -c "hf mf chk --1k"   -- execute cmd and quit client
       proxmark3 /dev/ttyACM0 -l hf_read            -- execute Lua script `hf_read` and quit client
       proxmark3 /dev/ttyACM0 -s mycmds.txt         -- execute each pm3 cmd in file and quit client
 
   to flash fullimage and bootloader:
 
       proxmark3 /dev/ttyACM0 --flash --unlock-bootloader --image bootrom.elf --image fullimage.elf
 
 Note (Linux):
 if the flasher gets stuck in 'Waiting for Proxmark3 to reappear on <DEVICE>',
 you need to blacklist Proxmark3 for modem-manager - see documentation for more details:
 * https://github.com/RfidResearchGroup/proxmark3/blob/master/doc/md/Installation_Instructions/ModemManager-Must-Be-Discarded.md
 
 More info on flashing procedure from the official Proxmark3 wiki:
 * https://github.com/Proxmark/proxmark3/wiki/Gentoo%20Linux
 * https://github.com/Proxmark/proxmark3/wiki/Ubuntu%20Linux
 * https://github.com/Proxmark/proxmark3/wiki/OSX
 
 ```
 
 - - -
 
 ### proxmark3-common
 
  This package contains scripts for the Proxmark3. It is
  dedicated to bringing the most out of the new features for Proxmark3 RDV4.0
  new hardware and design but it will also support older hardware revisions.
 
 **Installed size:** `38.53 MB`  
 **How to install:** `sudo apt install proxmark3-common`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### pm3
 
 
 ```
 root@kali:~# pm3 -h
 
 Quick helper script for proxmark3 client when working with a Proxmark3 device
 
 Description:
     The usage is the same as for the proxmark3 client, with the following differences:
      * the correct port name will be automatically guessed;
      * the script will wait for a Proxmark to be connected (same as option -w of the client).
     You can also specify a first option -n N to access the Nth Proxmark3 connected.
     To see a list of available ports, use --list.
 
 Usage:
     pm3 [-n <N>] [<any other proxmark3 client option>]
     pm3 [--list] [-h|--help] [-hh|--helpclient]
     pm3 [-o|--offline]
 
 
 Arguments:
     -h/--help        this help
     -hh/--helpclient proxmark3 client help (the script will forward these options)
     --list           list all detected com ports
     -n <N>           connect device referred to the N:th number on the --list output
     -o/--offline     shortcut to use directly the proxmark3 client without guessing ports
 
 Samples:
     ./pm3                       -- Auto detect/ select com port in the following order BT, USB/CDC, BT DONGLE
     ./pm3 -p /dev/ttyACM0       -- connect to port /dev/ttyACM0
     ./pm3 -n 2                  -- use second item from the --list output
     ./pm3 -c 'lf search' -i     -- run command and stay in client once completed
 
 
 ```
 
 - - -
 
 ##### pm3-flash
 
 
 ```
 root@kali:~# pm3-flash -h
 Quick helper script for flashing a Proxmark device via USB
 
 Description:
     The usage is similar to the old proxmark3-flasher binary, except that the correct port name will be automatically guessed.
     You can also specify a first option -n N to access the Nth Proxmark3 connected on USB.
     If this doesn't work, you'll have to use manually the proxmark3 client, see "/usr/bin/proxmark3 -h".
     To see a list of available ports, use --list.
 
 Usage:
     pm3-flash [-n <N>] [-b] image.elf [image.elf...]
     pm3-flash --list
 
 Options:
     -b         Enable flashing of bootloader area (DANGEROUS)
 
 Example:
      pm3-flash -b bootrom.elf fullimage.elf
 ```
 
 - - -
 
 ##### pm3-flash-all
 
 
 ```
 root@kali:~# pm3-flash-all -h
 Quick helper script for flashing a Proxmark device via USB
 
 Description:
     The correct port name will be automatically guessed and the stock bootloader and firmware image will be flashed.
     You can also specify a first option -n N to access the Nth Proxmark3 connected on USB.
     If this doesn't work, you'll have to use manually the proxmark3 client, see "/usr/bin/proxmark3 -h".
     To see a list of available ports, use --list.
 
 Usage:
     pm3-flash-all [-n <N>]
     pm3-flash-all --list
 ```
 
 - - -
 
 ##### pm3-flash-bootrom
 
 
 ```
 root@kali:~# pm3-flash-bootrom -h
 Quick helper script for flashing a Proxmark device via USB
 
 Description:
     The correct port name will be automatically guessed and the stock bootloader will be flashed.
     You can also specify a first option -n N to access the Nth Proxmark3 connected on USB.
     If this doesn't work, you'll have to use manually the proxmark3 client, see "/usr/bin/proxmark3 -h".
     To see a list of available ports, use --list.
 
 Usage:
     pm3-flash-bootrom [-n <N>]
     pm3-flash-bootrom --list
 ```
 
 - - -
 
 ##### pm3-flash-fullimage
 
 
 ```
 root@kali:~# pm3-flash-fullimage -h
 Quick helper script for flashing a Proxmark device via USB
 
 Description:
     The correct port name will be automatically guessed and the stock firmware image will be flashed.
     You can also specify a first option -n N to access the Nth Proxmark3 connected on USB.
     If this doesn't work, you'll have to use manually the proxmark3 client, see "/usr/bin/proxmark3 -h".
     To see a list of available ports, use --list.
 
 Usage:
     pm3-flash-fullimage [-n <N>]
     pm3-flash-fullimage --list
 ```
 
 - - -
 
 ### proxmark3-doc
 
  This package contains the documentation files for the Proxmark3 package. It is
  dedicated to bringing the most out of the new features for Proxmark3 RDV4.0
  new hardware and design but it will also support older hardware revisions.
 
 **Installed size:** `280 KB`  
 **How to install:** `sudo apt install proxmark3-doc`  
 
 
 - - -
 
 ### proxmark3-firmwares
 
  This package contains several firmwares for the Proxmark3. It is
  dedicated to bringing the most out of the new features for Proxmark3 RDV4.0
  new hardware and design but it will also support older hardware revisions.
 
 **Installed size:** `28.22 MB`  
 **How to install:** `sudo apt install proxmark3-firmwares`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
