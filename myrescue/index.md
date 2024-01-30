---
Title: myrescue
Homepage: http://myrescue.sf.net
Repository: https://salsa.debian.org/pkg-security-team/myrescue
Architectures: any
Version: 0.9.8-3
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-recover kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### myrescue
 
  myrescue is a program to rescue the still-readable data from a damaged
  harddisk, CD-ROM, DVD, flash drives, etc. It is similar in purpose to
  dd_rescue (or ddrescue), but it tries to quickly get out of damaged
  areas to first handle the not yet damaged part of the disk and return
  later.
   
  This package is useful to recover data from any media and for forensics
  investigations.
 
 **Installed size:** `83 KB`  
 **How to install:** `sudo apt install myrescue`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### myrescue
 
 Harddisc Rescue
 
 ```
 root@kali:~# myrescue --help
 myrescue: invalid option -- '-'
 myrescue [<options>] <input-file> <output-file>
 options:
 -b <block-size>   block size in bytes, default: 4096
 -B <bitmap-file>  bitmap-file, default: <output-file>.bitmap
 -A                abort on error
 -S                skip errors (exponential-step)
 -f <number>       skip blocks with <number> or more failures
 -r <retry-count>  try up to <retry-count> reads per block, default: 1
 -s <start-block>  start block number, default: 0
 -e <end-block>    end block number (excl.), default: size of <input-file>
 -G <range>        only read <range> blocks around good ones
 -F <range>        skip <range> blocks around failed ones
 -J <number>       randomly jump after reading a few sectors
 -T                make -A, -S and -F avoid blocks that took long to read
 -R                reverse copy direction
 -U <dev-file>     USB device reset after read error
                   (something like /dev/bus/usb/XXX/XXX !)
 -h, -?            usage information
 ```
 
 - - -
 
 ##### myrescue-bitmap2ppm
 
 Visualisation of the block bitmap for myrescue
 
 ```
 root@kali:~# myrescue-bitmap2ppm -h
 usage: bitmap2ppm <bitmap-file> <width> <rows> <width> ...
 ```
 
 - - -
 
 ##### myrescue-stat
 
 Block bitmap statistics for myrescue
 
 ```
 root@kali:~# man myrescue-stat
 myrescue-stat(2)              System Calls Manual             myrescue-stat(2)
 
 NAME
        myrescue-stat - Block bitmap statistics for myrescue
 
 SYNOPSIS
        myrescue-stat bitmap-file
 
 DESCRIPTION
        myrescue-stat reads a block bitmap from myrescue(1) and prints the num-
        ber and percentage of blocks for the different conditions.
 
        Possible conditions are:
 
        0 = Block has not yet been handled.
 
        1 = Block was successfully copied.
 
        2 = Block was successfully copied, but took a long time to read.
               (This usually indicates that the block is almost dead.)
 
        Negative values = Attempts to read the block have so far failed.
               The absolute value indicate the number of failed read attempts.
 
 AUTHORS
        Kristof Koehler <kristofk@users.sourceforge.net>
 
 SEE ALSO
        myrescue(1)
 
        http://myrescue.sourceforge.net/
 
 myrescue 0.9.6                   February 2018                myrescue-stat(2)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
