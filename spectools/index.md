---
Title: spectools
Homepage: 
Repository: 
Architectures: any
Version: 201601r1-2
Metapackages: kali-linux-everything kali-linux-large kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### spectools
 
  Spectrum-Tools is a set of utilities for using the Wi-Spy USB spectrum
  analyzer tools from Metageek LLC.  They include userspace drivers for
  the hardware (implemented via libusb), a graphing UI built on GTK/Cairo,
  network servers for remote devices, and simple utilities for developing
  additional tools.
 
 **Installed size:** `214 KB`  
 **How to install:** `sudo apt install spectools`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libncurses6 
 * libtinfo6 
 * libusb-0.1-4 
 {{< /spoiler >}}
 
 ##### spectool_curses
 
 Utility for developing other tools using the Wi-Spy
 
 ```
 root@kali:~# spectool_curses -h
 spectool_curses [ options ]
  -n / --net  tcp://host:port  Connect to network server
  -l / --list                  List detected devices
  -r / --range #               Use device range #
  -d / --device #              Use device #
 ```
 
 - - -
 
 ##### spectool_net
 
 Network server for the spectool_gtk program
 
 ```
 root@kali:~# spectool_net -h
 spectool_net [-b <secs>] [-p <port>] [-a <bind address>]
  --broadcast/-b  <secs>	    Send broadcast announce
  --port/-p <port>           Use alternate port
  --bindaddr/-a <address>    Bind to specific address
  -l / --list				  List devices and ranges only
  -r / --range [device:]range  Configure a device for a specific range
 ```
 
 - - -
 
 ##### spectool_raw
 
 Utility for developing other tools using the Wi-Spy
 
 ```
 root@kali:~# spectool_raw -h
 spectool_raw [ options ]
  -n / --net  tcp://host:port  Connect to network server instead of
  -b / --broadcast             Listen for (and connect to) broadcast servers
  -l / --list				  List devices and ranges only
  -r / --range [device:]range  Configure a device for a specific range
                               local USB devices
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
