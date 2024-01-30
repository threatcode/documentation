---
archived: "true"
Title: usbutils
Homepage: https://github.com/gregkh/usbutils
Repository: 
Architectures: linux-any
Version: 1:014-1
Metapackages: kali-linux-arm kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-802-11 kali-tools-exploitation kali-tools-sniffing-spoofing kali-tools-social-engineering kali-tools-top10 kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### usbutils
 
  This package contains the lsusb utility for inspecting the devices
  connected to the USB bus. It shows a graphical representation of the
  devices that are currently plugged in, showing the topology of the
  USB bus. It also displays information on each individual device on
  the bus.
 
 **Installed size:** `325 KB`  
 **How to install:** `sudo apt install usbutils`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libudev1 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 ##### lsusb
 
 List USB devices
 
 ```
 root@kali:~# lsusb -h
 Usage: lsusb [options]...
 List USB devices
   -v, --verbose
       Increase verbosity (show descriptors)
   -s [[bus]:][devnum]
       Show only devices with specified device and/or
       bus numbers (in decimal)
   -d vendor:[product]
       Show only devices with the specified vendor and
       product ID numbers (in hexadecimal)
   -D device
       Selects which device lsusb will examine
   -t, --tree
       Dump the physical USB device hierarchy as a tree
   -V, --version
       Show version of program
   -h, --help
       Show usage and help
 ```
 
 - - -
 
 ##### usb-devices
 
 Print USB device details
 
 ```
 root@kali:~# usb-devices -h
 
 T:  Bus=01 Lev=00 Prnt=00 Port=00 Cnt=00 Dev#=  1 Spd=12  MxCh=12
 D:  Ver= 1.10 Cls=09(hub  ) Sub=00 Prot=00 MxPS=64 #Cfgs=  1
 P:  Vendor=1d6b ProdID=0001 Rev=06.00
 S:  Manufacturer=Linux 6.0.0-kali3-amd64 ohci_hcd
 S:  Product=OHCI PCI host controller
 S:  SerialNumber=0000:00:06.0
 C:  #Ifs= 1 Cfg#= 1 Atr=e0 MxPwr=0mA
 I:  If#= 0 Alt= 0 #EPs= 1 Cls=09(hub  ) Sub=00 Prot=00 Driver=hub
 E:  Ad=81(I) Atr=03(Int.) MxPS=   2 Ivl=255ms
 
 T:  Bus=01 Lev=01 Prnt=01 Port=00 Cnt=01 Dev#=  2 Spd=12  MxCh= 0
 D:  Ver= 1.10 Cls=00(>ifc ) Sub=00 Prot=00 MxPS= 8 #Cfgs=  1
 P:  Vendor=80ee ProdID=0021 Rev=01.00
 S:  Manufacturer=VirtualBox
 S:  Product=USB Tablet
 C:  #Ifs= 1 Cfg#= 1 Atr=80 MxPwr=100mA
 I:  If#= 0 Alt= 0 #EPs= 1 Cls=03(HID  ) Sub=00 Prot=00 Driver=usbhid
 E:  Ad=81(I) Atr=03(Int.) MxPS=   8 Ivl=10ms
 ```
 
 - - -
 
 ##### usbhid-dump
 
 Dump USB HID device report descriptors and streams
 
 ```
 root@kali:~# usbhid-dump -h
 Usage: usbhid-dump [OPTION]...
 Dump USB device HID report descriptor(s) and/or stream(s).
 
 Options:
   -h, --help                       output this help message and exit
   -v, --version                    output version information and exit
 
   -s, -a, --address=bus[:dev]      limit interfaces by bus number
                                    (1-255) and device address (1-255),
                                    decimal; zeroes match any
   -d, -m, --model=vid[:pid]        limit interfaces by vendor and
                                    product IDs (0001-ffff), hexadecimal;
                                    zeroes match any
   -i, --interface=NUMBER           limit interfaces by number (0-254),
                                    decimal; 255 matches any
 
   -e, --entity=STRING              what to dump: either "descriptor",
                                    "stream" or "all"; value can be
                                    abbreviated
 
   -t, --stream-timeout=NUMBER      stream interrupt transfer timeout, ms;
                                    zero means infinity
   -p, --stream-paused              start with the stream dump output
                                    paused
   -f, --stream-feedback            enable stream dumping feedback: for
                                    every transfer dumped a dot is
                                    printed to stderr
 
 Default options: --stream-timeout=60000 --entity=descriptor
 
 Signals:
   USR1/USR2                        pause/resume the stream dump output
 
 ```
 
 - - -
 
 ##### usbreset
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
