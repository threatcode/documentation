---
Title: spooftooph
Homepage: http://www.hackfromacave.com/projects/spooftooph.html
Repository: https://gitlab.com/kalilinux/packages/spooftooph
Architectures: any
Version: 0.5.2-1kali4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-bluetooth kali-tools-wireless 
Icon: images/spooftooph-logo.svg
PackagesInfo: |
 ### spooftooph
 
  Spooftooph is designed to automate spoofing or cloning
  Bluetooth device Name, Class, and Address. Cloning this
  information effectively allows Bluetooth device to hide in
  plain site. Bluetooth scanning software will only list one
  of the devices if more than one device in range shares the
  same device information when the devices are in Discoverable
  Mode (specificaly the same Address).
 
 **Installed size:** `74 KB`  
 **How to install:** `sudo apt install spooftooph`  
 
 {{< spoiler "Dependencies:" >}}
 * bluez
 * libbluetooth3 
 * libc6 
 * libncurses6 
 * libtinfo6 
 {{< /spoiler >}}
 
 ##### spooftooph
 
 
 ```
 root@kali:~# spooftooph -h
 
 spooftooph v0.5.2 by JP Dunning (.ronin) 
 <www.hackfromacave.com>
 (c) 2009-2012 Shadow Cave LLC.
 
 NAME
 	spooftooph
 
 SYNOPSIS
 	spooftooph -i dev [-mstu] [-nac]|[-R]|[-r file] [-w file]
 
 DESCRIPTION
 	-a <address>	: Specify new BD_ADDR
 	-b <num_lines>	: Number of Bluetooth profiles to display per page
 	-B 		: Disable banner for smaller screens (like phones)
 	-c <class>	: Specify new CLASS
 	-h		: Help
 	-i <dev>	: Specify interface
 	-m		: Specify multiple interfaces during selection
 	-n <name>	: Specify new NAME
 	-r <file>	: Read in CSV logfile
 	-R		: Assign random NAME, CLASS, and ADDR
 	-s		: Scan for devices in local area
 	-t <time>	: Time interval to clone device in range
 	-u		: USB delay.  Interactive delay for reinitializing interface
 	-w <file>	: Write to CSV logfile
 			  (Useful in Virtualized environment when USB must be passed through.)
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## spooftooph Usage Example

Use the Bluetooth interface (`-i hci1`) to spoof itself as the given address (`-a 00803789EE76`):

```
root@kali:~# spooftooph -i hci1 -a 00803789EE76
Manufacturer:   Broadcom Corporation (15)
Device address: 00:19:0E:0E:EA:4B
```
