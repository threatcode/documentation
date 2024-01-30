---
Title: google-nexus-tools
Homepage: https://github.com/corbindavenport/nexus-tools
Repository: https://gitlab.com/kalilinux/packages/google-nexus-tools
Architectures: any
Version: 2.3-0kali7
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### google-nexus-tools
 
  Nexus Tools is an installer for the Android debug/development command-line
  tools ADB (Android Device Bridge) and Fastboot for Mac OS X, Linux, and Google
  Chrome/Chromium OS.
 
 **Installed size:** `1.38 MB`  
 **How to install:** `sudo apt install google-nexus-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * lib32stdc++6
 {{< /spoiler >}}
 
 ##### nexus-adb
 
 
 ```
 root@kali:~# nexus-adb -h
 Android Debug Bridge version 1.0.31
 
  -a                            - directs adb to listen on all interfaces for a connection
  -d                            - directs command to the only connected USB device
                                  returns an error if more than one USB device is present.
  -e                            - directs command to the only running emulator.
                                  returns an error if more than one emulator is running.
  -s <specific device>          - directs command to the device or emulator with the given
                                  serial number or qualifier. Overrides ANDROID_SERIAL
                                  environment variable.
  -p <product name or path>     - simple product name like 'sooner', or
                                  a relative/absolute path to a product
                                  out directory like 'out/target/product/sooner'.
                                  If -p is not specified, the ANDROID_PRODUCT_OUT
                                  environment variable is used, which must
                                  be an absolute path.
  -H                            - Name of adb server host (default: localhost)
  -P                            - Port of adb server (default: 5037)
  devices [-l]                  - list all connected devices
                                  ('-l' will also list device qualifiers)
  connect <host>[:<port>]       - connect to a device via TCP/IP
                                  Port 5555 is used by default if no port number is specified.
  disconnect [<host>[:<port>]]  - disconnect from a TCP/IP device.
                                  Port 5555 is used by default if no port number is specified.
                                  Using this command with no additional arguments
                                  will disconnect from all connected TCP/IP devices.
 
 device commands:
   adb push <local> <remote>    - copy file/dir to device
   adb pull <remote> [<local>]  - copy file/dir from device
   adb sync [ <directory> ]     - copy host->device only if changed
                                  (-l means list but don't copy)
                                  (see 'adb help all')
   adb shell                    - run remote shell interactively
   adb shell <command>          - run remote shell command
   adb emu <command>            - run emulator console command
   adb logcat [ <filter-spec> ] - View device log
   adb forward --list           - list all forward socket connections.
                                  the format is a list of lines with the following format:
                                     <serial> " " <local> " " <remote> "\n"
   adb forward <local> <remote> - forward socket connections
                                  forward specs are one of: 
                                    tcp:<port>
                                    localabstract:<unix domain socket name>
                                    localreserved:<unix domain socket name>
                                    localfilesystem:<unix domain socket name>
                                    dev:<character device name>
                                    jdwp:<process pid> (remote only)
   adb forward --no-rebind <local> <remote>
                                - same as 'adb forward <local> <remote>' but fails
                                  if <local> is already forwarded
   adb forward --remove <local> - remove a specific forward socket connection
   adb forward --remove-all     - remove all forward socket connections
   adb jdwp                     - list PIDs of processes hosting a JDWP transport
   adb install [-l] [-r] [-s] [--algo <algorithm name> --key <hex-encoded key> --iv <hex-encoded iv>] <file>
                                - push this package file to the device and install it
                                  ('-l' means forward-lock the app)
                                  ('-r' means reinstall the app, keeping its data)
                                  ('-s' means install on SD card instead of internal storage)
                                  ('--algo', '--key', and '--iv' mean the file is encrypted already)
   adb uninstall [-k] <package> - remove this app package from the device
                                  ('-k' means keep the data and cache directories)
   adb bugreport                - return all information from the device
                                  that should be included in a bug report.
 
   adb backup [-f <file>] [-apk|-noapk] [-obb|-noobb] [-shared|-noshared] [-all] [-system|-nosystem] [<packages...>]
                                - write an archive of the device's data to <file>.
                                  If no -f option is supplied then the data is written
                                  to "backup.ab" in the current directory.
                                  (-apk|-noapk enable/disable backup of the .apks themselves
                                     in the archive; the default is noapk.)
                                  (-obb|-noobb enable/disable backup of any installed apk expansion
                                     (aka .obb) files associated with each application; the default
                                     is noobb.)
                                  (-shared|-noshared enable/disable backup of the device's
                                     shared storage / SD card contents; the default is noshared.)
                                  (-all means to back up all installed applications)
                                  (-system|-nosystem toggles whether -all automatically includes
                                     system applications; the default is to include system apps)
                                  (<packages...> is the list of applications to be backed up.  If
                                     the -all or -shared flags are passed, then the package
                                     list is optional.  Applications explicitly given on the
                                     command line will be included even if -nosystem would
                                     ordinarily cause them to be omitted.)
 
   adb restore <file>           - restore device contents from the <file> backup archive
 
   adb help                     - show this help message
   adb version                  - show version num
 
 scripting:
   adb wait-for-device          - block until device is online
   adb start-server             - ensure that there is a server running
   adb kill-server              - kill the server if it is running
   adb get-state                - prints: offline | bootloader | device
   adb get-serialno             - prints: <serial-number>
   adb get-devpath              - prints: <device-path>
   adb status-window            - continuously print device status for a specified device
   adb remount                  - remounts the /system partition on the device read-write
   adb reboot [bootloader|recovery] - reboots the device, optionally into the bootloader or recovery program
   adb reboot-bootloader        - reboots the device into the bootloader
   adb root                     - restarts the adbd daemon with root permissions
   adb usb                      - restarts the adbd daemon listening on USB
   adb tcpip <port>             - restarts the adbd daemon listening on TCP on the specified port
 networking:
   adb ppp <tty> [parameters]   - Run PPP over USB.
  Note: you should not automatically start a PPP connection.
  <tty> refers to the tty for PPP stream. Eg. dev:/dev/omap_csmi_tty1
  [parameters] - Eg. defaultroute debug dump local notty usepeerdns
 
 adb sync notes: adb sync [ <directory> ]
   <localdir> can be interpreted in several ways:
 
   - If <directory> is not specified, both /system and /data partitions will be updated.
 
   - If it is "system" or "data", only the corresponding partition
     is updated.
 
 environmental variables:
   ADB_TRACE                    - Print debug information. A comma separated list of the following values
                                  1 or all, adb, sockets, packets, rwx, usb, sync, sysdeps, transport, jdwp
   ANDROID_SERIAL               - The serial number to connect to. -s takes priority over this if given.
   ANDROID_LOG_TAGS             - When used with the logcat option, only these debug tags are printed.
 ```
 
 - - -
 
 ##### nexus-fastboot
 
 
 ```
 root@kali:~# nexus-fastboot -h
 usage: fastboot [ <option> ] <command>
 
 commands:
   update <filename>                        reflash device from update.zip
   flashall                                 flash boot + recovery + system
   flash <partition> [ <filename> ]         write a file to a flash partition
   erase <partition>                        erase a flash partition
   format <partition>                       format a flash partition 
   getvar <variable>                        display a bootloader variable
   boot <kernel> [ <ramdisk> ]              download and boot kernel
   flash:raw boot <kernel> [ <ramdisk> ]    create bootimage and flash it
   devices                                  list all connected devices
   continue                                 continue with autoboot
   reboot                                   reboot device normally
   reboot-bootloader                        reboot device into bootloader
   help                                     show this help message
 
 options:
   -w                                       erase userdata and cache (and format
                                            if supported by partition type)
   -u                                       do not first erase partition before
                                            formatting
   -s <specific device>                     specify device serial number
                                            or path to device port
   -l                                       with "devices", lists device paths
   -p <product>                             specify product name
   -c <cmdline>                             override kernel commandline
   -i <vendor id>                           specify a custom USB vendor id
   -b <base_addr>                           specify a custom kernel base address. default: 0x10000000
   -n <page size>                           specify the nand page size. default: 2048
   -S <size>[K|M|G]                         automatically sparse files greater than
                                            size.  0 to disable
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
