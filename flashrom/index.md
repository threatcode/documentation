---
Title: flashrom
Homepage: http://www.flashrom.org
Repository: https://salsa.debian.org/myczko-guest/flashrom
Architectures: any
Version: 1.3.0-2.1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-hardware 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### flashrom
 
  flashrom is a tool for identifying, reading, writing, verifying and erasing
  flash chips. It's often used to flash BIOS/EFI/coreboot/firmware/optionROM
  images in-system using a supported mainboard, but it also supports flashing of
  network cards (NICs), SATA controller cards, and other external devices which
  can program flash chips.
   
  It supports a wide range of DIP32, PLCC32, DIP8, SO8/SOIC8, TSOP32/40/48,
  and BGA chips, which use various protocols such as LPC, FWH, parallel
  flash, or SPI.
   
  The tool can be used to flash BIOS/firmware images for example -- be it
  proprietary BIOS images or coreboot (previously known as LinuxBIOS) images.
   
  It can also be used to read the current existing BIOS/firmware from a
  flash chip.
   
  Currently supported programmers include:
   
    * internal (for in-system flashing in the mainboard)
    * dummy (virtual programmer for testing flashrom)
    * nic3com (for flash ROMs on 3COM network cards)
    * nicrealtek (for flash ROMs on Realtek and SMC 1211 network cards)
    * nicnatsemi (for flash ROMs on National Semiconductor DP838* network cards)
    * nicintel (for parallel flash ROMs on Intel 10/100Mbit network cards)
    * gfxnvidia (for flash ROMs on NVIDIA graphics cards)
    * drkaiser (for flash ROMs on Dr. Kaiser PC-Waechter PCI cards)
    * satasii (for flash ROMs on Silicon Image SATA/IDE controllers)
    * satamv (for flash ROMs on Marvell SATA controllers)
    * atahpt (for flash ROMs on Highpoint ATA/RAID controllers)
    * atavia (for flash ROMs on VIA VT6421A SATA controllers)
    * atapromise (for flash ROMs on Promise PDC2026x ATA/RAID controllers)
    * it8212 (for flash ROMs on ITE IT8212F ATA/RAID controller)
    * ft2232_spi (for SPI flash ROMs attached to an FT2232/FT4232H/FT232H family
      based USB SPI programmer), including the DLP Design DLP-USB1232H,
      FTDI FT2232H Mini-Module, FTDI FT4232H Mini-Module, openbiosprog-spi,
      Amontec JTAGkey/JTAGkey-tiny/JTAGkey-2, Dangerous Prototypes Bus Blaster,
      Olimex ARM-USB-TINY/-H, Olimex ARM-USB-OCD/-H, TIAO/DIYGADGET USB
      Multi-Protocol Adapter (TUMPA), TUMPA Lite, GOEPEL PicoTAP,
      Google Servo v1/v2, and FIC OpenMoko Neo1973 Debug board.
    * serprog (for flash ROMs attached to a programmer speaking serprog),
      including AVR flasher by Urja Rannikko, AVR flasher by eightdot,
      Arduino Mega flasher by fritz, InSystemFlasher by Juhana Helovuo,
      and atmegaXXu2-flasher by Stefan Tauner.
    * buspirate_spi (for SPI flash ROMs attached to a Bus Pirate)
    * dediprog (for SPI flash ROMs attached to a Dediprog SF100)
    * rayer_spi (for SPI flash ROMs attached to a RayeR parport based programmer)
    * pony_spi (for SPI flash ROMs attached to a SI-Prog serial port
      bitbanging adapter)
    * nicintel_spi (for SPI flash ROMs on Intel Gigabit network cards)
    * ogp_spi (for SPI flash ROMs on Open Graphics Project graphics card)
    * linux_spi (for SPI flash ROMs accessible via /dev/spidevX.Y on Linux)
    * usbblaster_spi (for SPI flash ROMs attached to an Altera USB-Blaster)
    * nicintel_eeprom (for SPI EEPROMs on Intel Gigabit network cards)
    * mstarddc_spi (for SPI flash ROMs accessible through DDC in MSTAR-equipped
      displays)
    * pickit2_spi (for SPI flash ROMs accessible via Microchip PICkit2)
    * ch341a_spi (for SPI flash ROMs attached to WCH CH341A)
 
 **Installed size:** `1.08 MB`  
 **How to install:** `sudo apt install flashrom`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libftdi1-2 
 * libjaylink0 
 * libpci3 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 ##### flashrom
 
 Detect, read, write, verify and erase flash chips
 
 ```
 root@kali:~# flashrom -h
 flashrom unknown on Linux 6.5.0-kali3-amd64 (x86_64)
 flashrom is free software, get the source code at https://flashrom.org
 
 Using clock_gettime for delay loops (clk_id: 1, resolution: 1ns).
 Usage: flashrom [-h|-R|-L|
 	-p <programmername>[:<parameters>] [-c <chipname>]
 		(--flash-name|--flash-size|
 		 [-E|-x|(-r|-w|-v) <file>]
 		 [(-l <layoutfile>|--ifd| --fmap|--fmap-file <file>) [-i <region>[:<file>]]...]
 		 [-n] [-N] [-f])]
 	[-V[V[V]]] [-o <logfile>]
 
  -h | --help                        print this help text
  -R | --version                     print version (release)
  -r | --read <file>                 read flash and save to <file>
  -w | --write (<file>|-)            write <file> or the content provided
                                     on the standard input to flash
  -v | --verify (<file>|-)           verify flash against <file>
                                     or the content provided on the standard input
  -E | --erase                       erase flash memory
  -V | --verbose                     more verbose output
  -c | --chip <chipname>             probe only for specified flash chip
  -f | --force                       force specific operations (see man page)
  -n | --noverify                    don't auto-verify
  -N | --noverify-all                verify included regions only (cf. -i)
  -x | --extract                     extract regions to files
  -l | --layout <layoutfile>         read ROM layout from <layoutfile>
       --wp-disable                  disable write protection
       --wp-enable                   enable write protection
       --wp-list                     list supported write protection ranges
       --wp-status                   show write protection status
       --wp-range=<start>,<len>      set write protection range (use --wp-range=0,0
                                     to unprotect the entire flash)
       --wp-region <region>          set write protection region
       --flash-name                  read out the detected flash name
       --flash-size                  read out the detected flash size
       --fmap                        read ROM layout from fmap embedded in ROM
       --fmap-file <fmapfile>        read ROM layout from fmap in <fmapfile>
       --ifd                         read layout from an Intel Firmware Descriptor
  -i | --include <region>[:<file>]   only read/write image <region> from layout
                                     (optionally with data from <file>)
       --image <region>[:<file>]     deprecated, please use --include
  -o | --output <logfile>            log output to <logfile>
       --flash-contents <ref-file>   assume flash contents to be <ref-file>
  -L | --list-supported              print supported devices
  -p | --programmer <name>[:<param>] specify the programmer device. One of
     internal, dummy, nic3com, nicrealtek, gfxnvidia, raiden_debug_spi, drkaiser,
     satasii, atavia, it8212, ft2232_spi, serprog, buspirate_spi, dediprog,
     developerbox, rayer_spi, pony_spi, nicintel, nicintel_spi, nicintel_eeprom,
     ogp_spi, satamv, linux_mtd, linux_spi, usbblaster_spi, pickit2_spi,
     ch341a_spi, digilent_spi, jlink_spi, stlinkv3_spi, dirtyjtag_spi.
 
 You can specify one of -h, -R, -L, -E, -r, -w, -v or no operation.
 If no operation is specified, flashrom will only probe for flash chips.
 ```
 
 - - -
 
 ### libflashrom-dev
 
  flashrom is a tool for identifying, reading, writing, verifying and erasing
  flash chips. It's often used to flash BIOS/EFI/coreboot/firmware/optionROM
  images in-system using a supported mainboard, but it also supports flashing of
  network cards (NICs), SATA controller cards, and other external devices which
  can program flash chips.
   
  It supports a wide range of DIP32, PLCC32, DIP8, SO8/SOIC8, TSOP32/40/48,
  and BGA chips, which use various protocols such as LPC, FWH, parallel
  flash, or SPI.
   
  The tool can be used to flash BIOS/firmware images for example -- be it
  proprietary BIOS images or coreboot (previously known as LinuxBIOS) images.
   
  It can also be used to read the current existing BIOS/firmware from a
  flash chip.
   
  This package provides flashrom header development files.
 
 **Installed size:** `43 KB`  
 **How to install:** `sudo apt install libflashrom-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libflashrom1 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libflashrom1
 
  flashrom is a tool for identifying, reading, writing, verifying and erasing
  flash chips. It's often used to flash BIOS/EFI/coreboot/firmware/optionROM
  images in-system using a supported mainboard, but it also supports flashing of
  network cards (NICs), SATA controller cards, and other external devices which
  can program flash chips.
   
  It supports a wide range of DIP32, PLCC32, DIP8, SO8/SOIC8, TSOP32/40/48,
  and BGA chips, which use various protocols such as LPC, FWH, parallel
  flash, or SPI.
   
  The tool can be used to flash BIOS/firmware images for example -- be it
  proprietary BIOS images or coreboot (previously known as LinuxBIOS) images.
   
  It can also be used to read the current existing BIOS/firmware from a
  flash chip.
   
  This package provides flashrom library development files.
 
 **Installed size:** `1.02 MB`  
 **How to install:** `sudo apt install libflashrom1`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libftdi1-2 
 * libjaylink0 
 * libpci3 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
