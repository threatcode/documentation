---
Title: openocd
Homepage: http://openocd.sourceforge.net/
Repository: https://salsa.debian.org/electronics-team/openocd
Architectures: any
Version: 0.12.0-1
Metapackages: kali-linux-everything kali-tools-hardware 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### openocd
 
  OpenOCD aims to provide debugging, in-system programming and boundary-scan
  testing for embedded target devices.
   
  The debugger uses an IEEE 1149-1 compliant JTAG TAP bus master to access
  on-chip debug functionality available on ARM based microcontrollers or
  system-on-chip solutions. For MIPS systems the EJTAG interface is supported.
  Additionally there is support for eSi-RISC, Intel, OpenRISC, RISC-V and ARC
  controllers.
   
  User interaction is realized through a telnet command line interface,
  a gdb (the GNU debugger) remote protocol server, and a simplified RPC
  connection that can be used to interface with OpenOCD's Jim Tcl engine.
   
  OpenOCD supports many different types of JTAG interfaces/programmers.
 
 **Installed size:** `8.79 MB`  
 **How to install:** `sudo apt install openocd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcapstone4 
 * libftdi1-2 
 * libgpiod2 
 * libhidapi-hidraw0 
 * libjaylink0 
 * libjim0.82 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 ##### openocd
 
 A free and open on-chip debugging, in-system programming and boundary-scan testing tool for ARM and MIPS systems
 
 ```
 root@kali:~# openocd -h
 Open On-Chip Debugger 0.12.0
 Licensed under GNU GPL v2
 For bug reports, read
 	http://openocd.org/doc/doxygen/bugs.html
 Open On-Chip Debugger
 Licensed under GNU GPL v2
 --help       | -h	display this help
 --version    | -v	display OpenOCD version
 --file       | -f	use configuration file <name>
 --search     | -s	dir to search for config files and scripts
 --debug      | -d	set debug level to 3
              | -d<n>	set debug level to <level>
 --log_output | -l	redirect log output to file <name>
 --command    | -c	run <command>
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
