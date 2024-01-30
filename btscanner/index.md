---
Title: btscanner
Homepage: https://salsa.debian.org/pkg-security-team/btscanner
Repository: https://salsa.debian.org/pkg-security-team/btscanner
Architectures: any
Version: 2.1-9
Metapackages: kali-linux-everything kali-linux-large kali-tools-bluetooth kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### btscanner
 
  btscanner is a tool designed specifically to extract as much information
  as possible from a Bluetooth device without the requirement to pair. A
  detailed information screen extracts HCI and SDP information, and
  maintains an open connection to monitor the RSSI and link quality.
  btscanner is based on the BlueZ Bluetooth stack, which is included with
  recent Linux kernels, and the BlueZ toolset. btscanner also contains a
  complete listing of the IEEE OUI numbers and class lookup tables. Using
  the information gathered from these sources it is possible to make
  educated guesses as to the host device type.
 
 **Installed size:** `106 KB`  
 **How to install:** `sudo apt install btscanner`  
 
 {{< spoiler "Dependencies:" >}}
 * ieee-data
 * libbluetooth3 
 * libc6 
 * libncurses6 
 * libtinfo6 
 * libxml2 
 * perl
 {{< /spoiler >}}
 
 ##### btscanner
 
 Ncurses-based scanner for Bluetooth devices
 
 ```
 root@kali:~# btscanner -h
 Usage: btscanner [options]
 options
 	--help	Display help
 	--cfg=<file>	Use <file> as the config file
 	--no-reset	Do not reset the Bluetooth adapter before scanning
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
