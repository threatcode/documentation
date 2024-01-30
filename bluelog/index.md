---
Title: bluelog
Homepage: http://www.digifail.com/software/bluelog.shtml
Repository: https://gitlab.com/kalilinux/packages/bluelog
Architectures: any
Version: 1.1.2-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-bluetooth kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bluelog
 
  Bluelog is a Bluetooth scanner designed to tell you how
  many discoverable devices there are in an area as quickly
  as possible. It is intended to be used as a site survey
  tool, identifying the number of possible Bluetooth targets
  there are in the surrounding environment.
 
 **Installed size:** `198 KB`  
 **How to install:** `sudo apt install bluelog`  
 
 {{< spoiler "Dependencies:" >}}
 * bluez
 * ieee-data
 * libbluetooth-dev
 * libbluetooth3 
 * libc6 
 {{< /spoiler >}}
 
 ##### bluelog
 
 Bluetooth Scanner and Logger
 
 ```
 root@kali:~# bluelog -h
 Bluelog (v1.1.2) by Tom Nardi "MS3FGX" (MS3FGX@gmail.com)
 ----------------------------------------------------------------
 Bluelog is a Bluetooth site survey tool, designed to tell you how
 many discoverable devices there are in an area as quickly as possible.
 As the name implies, its primary function is to log discovered devices
 to file rather than to be used interactively. Bluelog could run on a
 system unattended for long periods of time to collect data.
 
 Bluelog also includes a mode called "Bluelog Live" which creates a
 webpage of the results that you can serve up with your HTTP daemon of
 choice. See the "README.LIVE" file for details.
 
 For more information, see: www.digifail.com
 
 Basic Options:
 	-i <interface>     Sets scanning device, default is "hci0"
 	-o <filename>      Sets output filename, default is "devices.log"
 	-v                 Verbose, prints discovered devices to the terminal
 	-q                 Quiet, turns off nonessential terminal outout
 	-d                 Enables daemon mode, Bluelog will run in background
 	-k                 Kill an already running Bluelog process
 	-l                 Start "Bluelog Live", default is disabled
 
 Logging Options:
 	-n                 Write device names to log, default is disabled
 	-m                 Write device manufacturer to log, default is disabled
 	-c                 Write device class to log, default is disabled
 	-f                 Use "friendly" device class, default is disabled
 	-t                 Write timestamps to log, default is disabled
 	-x                 Obfuscate discovered MACs, default is disabled
 	-e                 Encode discovered MACs with CRC32, default disabled
 	-b                 Enable BlueProPro log format, see README
 
 Advanced Options:
 	-r <retries>       Name resolution retries, default is 3
 	-a <minutes>       Amnesia, Bluelog will forget device after given time
 	-w <seconds>       Scanning window in seconds, see README
 	-s                 Syslog only mode, no log file. Default is disabled
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## bluelog Usage Example

```
root@kali:~# bluelog
Bluelog (v1.1.2) by MS3FGX
---------------------------
Autodetecting device...OK
Opening output file: bluelog-2014-05-15-1651.log...OK
Writing PID file: /tmp/bluelog.pid...OK
Scan started at [05/15/14 16:51:46] on 00:19:0E:0E:EA:4B.
Hit Ctrl+C to end scan.
```
