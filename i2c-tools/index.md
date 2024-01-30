---
Title: i2c-tools
Homepage: https://www.kernel.org/pub/software/utils/i2c-tools/
Repository: 
Architectures: linux-any
Version: 4.3-4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### i2c-tools
 
  This package contains a heterogeneous set of I2C tools for Linux: a bus
  probing tool, a chip dumper, register-level access helpers, EEPROM
  decoding scripts, and more.
 
 **Installed size:** `317 KB`  
 **How to install:** `sudo apt install i2c-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * libi2c0 
 * perl
 * udev
 {{< /spoiler >}}
 
 ##### ddcmon
 
 
 
 - - -
 
 ##### decode-dimms
 
 Decode the information found in memory module SPD EEPROMs
 
 ```
 root@kali:~# decode-dimms -h
 Usage: /usr/bin/decode-dimms [-c] [-f [-b]] [-x|-X file [files..]]
        /usr/bin/decode-dimms -h
 
   -f, --format            Print nice html output
   -b, --bodyonly          Don't print html header
                           (useful for postprocessing the output)
       --side-by-side      Display all DIMMs side-by-side if possible
       --merge-cells       Merge neighbour cells with identical values
                           (side-by-side output only, default)
       --no-merge-cells    Don't merge neighbour cells with identical values
                           (side-by-side output only)
   -c, --checksum          Decode completely even if checksum fails
   -x,                     Read data from hexdump files
   -X,                     Same as -x except treat multibyte hex
                           data as little endian
   -h, --help              Display this usage summary
 
 Hexdumps can be the output from hexdump, hexdump -C, i2cdump, eeprog and
 likely many other progams producing hex dumps of one kind or another.  Note
 that the default output of "hexdump" will be byte-swapped on little-endian
 systems and you must use -X instead of -x, otherwise the dump will not be
 parsed correctly.  It is better to use "hexdump -C", which is not ambiguous.
 ```
 
 - - -
 
 ##### decode-edid
 
 
 
 - - -
 
 ##### decode-vaio
 
 Decode the information found in the Sony Vaio laptop identification EEPROMs
 
 ```
 root@kali:~# decode-vaio -h
 # Sony Vaio EEPROM Decoder version 1.7 by Jean Delvare
 
 Vaio EEPROM not found.  Please make sure that the at24 or eeprom module is loaded.
 
 ```
 
 - - -
 
 ##### i2c-stub-from-dump
 
 Feed i2c-stub with dump files
 
 ```
 root@kali:~# i2c-stub-from-dump -h
 Usage: i2c-stub-from-dump <addr>[,<addr>,...] <dump file> [<dump file> ...]
 ```
 
 - - -
 
 ##### i2cdetect
 
 Detect I2C chips
 
 ```
 root@kali:~# i2cdetect -h
 Error: Unsupported option "-h"!
 Usage: i2cdetect [-y] [-a] [-q|-r] I2CBUS [FIRST LAST]
        i2cdetect -F I2CBUS
        i2cdetect -l
   I2CBUS is an integer or an I2C bus name
   If provided, FIRST and LAST limit the probing range.
 ```
 
 - - -
 
 ##### i2cdump
 
 Examine I2C registers
 
 ```
 root@kali:~# i2cdump -h
 Error: Unsupported option "-h"!
 Usage: i2cdump [-f] [-y] [-r first-last] [-a] I2CBUS ADDRESS [MODE [BANK [BANKREG]]]
   I2CBUS is an integer or an I2C bus name
   ADDRESS is an integer (0x08 - 0x77, or 0x00 - 0x7f if -a is given)
   MODE is one of:
     b (byte, default)
     w (word)
     W (word on even register addresses)
     s (SMBus block, deprecated)
     i (I2C block)
     c (consecutive byte)
     Append p for SMBus PEC
 ```
 
 - - -
 
 ##### i2cget
 
 Read from I2C/SMBus chip registers
 
 ```
 root@kali:~# i2cget -h
 Error: Unsupported option "-h"!
 Usage: i2cget [-f] [-y] [-a] I2CBUS CHIP-ADDRESS [DATA-ADDRESS [MODE [LENGTH]]]
   I2CBUS is an integer or an I2C bus name
   ADDRESS is an integer (0x08 - 0x77, or 0x00 - 0x7f if -a is given)
   MODE is one of:
     b (read byte data, default)
     w (read word data)
     c (write byte/read byte)
     s (read SMBus block data)
     i (read I2C block data)
     Append p for SMBus PEC
   LENGTH is the I2C block data length (between 1 and 32, default 32)
 ```
 
 - - -
 
 ##### i2cset
 
 Set I2C registers
 
 ```
 root@kali:~# i2cset -h
 Error: Unsupported option "-h"!
 Usage: i2cset [-f] [-y] [-m MASK] [-r] [-a] I2CBUS CHIP-ADDRESS DATA-ADDRESS [VALUE] ... [MODE]
   I2CBUS is an integer or an I2C bus name
   ADDRESS is an integer (0x08 - 0x77, or 0x00 - 0x7f if -a is given)
   MODE is one of:
     c (byte, no value)
     b (byte data, default)
     w (word data)
     i (I2C block data)
     s (SMBus block data)
     Append p for SMBus PEC
 ```
 
 - - -
 
 ##### i2ctransfer
 
 Send user-defined I2C messages in one transfer
 
 ```
 root@kali:~# i2ctransfer -h
 Error: Unsupported option "-h"!
 Usage: i2ctransfer [-f] [-y] [-v] [-V] [-a] I2CBUS DESC [DATA] [DESC [DATA]]...
   I2CBUS is an integer or an I2C bus name
   DESC describes the transfer in the form: {r|w}LENGTH[@address]
     1) read/write-flag 2) LENGTH (range 0-65535, or '?')
     3) I2C address (use last one if omitted)
   DATA are LENGTH bytes for a write message. They can be shortened by a suffix:
     = (keep value constant until LENGTH)
     + (increase value by 1 until LENGTH)
     - (decrease value by 1 until LENGTH)
     p (use pseudo random generator until LENGTH with value as seed)
 
 Example (bus 0, read 8 byte at offset 0x64 from EEPROM at 0x50):
   # i2ctransfer 0 w1@0x50 0x64 r8
 Example (same EEPROM, at offset 0x42 write 0xff 0xfe ... 0xf0):
   # i2ctransfer 0 w17@0x50 0x42 0xff-
 ```
 
 - - -
 
 ### libi2c-dev
 
  I2C devices are usually controlled by a kernel driver.  Using this
  library it is also possible to access all devices on an adapter
  from userspace and without the knowledge of Linux kernel internals.
   
  This package contains what you need for compiling sources that
  use this library in your own code.
 
 **Installed size:** `33 KB`  
 **How to install:** `sudo apt install libi2c-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libi2c0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libi2c0
 
  I2C devices are usually controlled by a kernel driver.  Using this
  library it is also possible to access all devices on an adapter
  from userspace and without the knowledge of Linux kernel internals.
   
  This package contains what you need to run programs that use this
  library.
 
 **Installed size:** `35 KB`  
 **How to install:** `sudo apt install libi2c0`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python3-smbus
 
  This Python 3 module allows SMBus access through the I2C /dev interface on
  Linux hosts.  The host kernel must have I2C support, I2C device interface
  support, and a bus adapter driver.
 
 **Installed size:** `46 KB`  
 **How to install:** `sudo apt install python3-smbus`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libi2c0 
 * python3 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
