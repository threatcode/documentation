---
Title: bettercap
Homepage: https://www.bettercap.org
Repository: https://gitlab.com/kalilinux/packages/bettercap
Architectures: any
Version: 2.32.0+git20230725-0kali2
Metapackages: kali-linux-everything kali-linux-nethunter kali-tools-sniffing-spoofing 
Icon: images/bettercap-logo.svg
PackagesInfo: |
 ### bettercap
 
  This package contains a Swiss Army knife for 802.11, BLE and Ethernet networks
  reconnaissance and attacks.
 
 **Installed size:** `24.29 MB`  
 **How to install:** `sudo apt install bettercap`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnetfilter-queue1 
 * libpcap0.8 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 ##### bettercap
 
 
 ```
 root@kali:~# bettercap -h
 Usage of bettercap:
   -autostart string
     	Comma separated list of modules to auto start. (default "events.stream")
   -caplet string
     	Read commands from this file and execute them in the interactive session.
   -caplets-path string
     	Specify an alternative base path for caplets.
   -cpu-profile file
     	Write cpu profile file.
   -debug
     	Print debug messages.
   -env-file string
     	Load environment variables from this file if found, set to empty to disable environment persistence.
   -eval string
     	Run one or more commands separated by ; in the interactive session, used to set variables via command line.
   -gateway-override string
     	Use the provided IP address instead of the default gateway. If not specified or invalid, the default gateway will be used.
   -iface string
     	Network interface to bind to, if empty the default interface will be auto selected.
   -mem-profile file
     	Write memory profile to file.
   -no-colors
     	Disable output color effects.
   -no-history
     	Disable interactive session history file.
   -pcap-buf-size int
     	PCAP buffer size, leave to 0 for the default value. (default -1)
   -script string
     	Load a session script.
   -silent
     	Suppress all logs which are not errors.
   -version
     	Print the version and exit.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## bettercap Usage Example

Scan the system in quiet mode (`-Q`) and output in cronjob format (`–cronjob`):

```
root@kali:~# bettercap
bettercap v2.11 (type 'help' for a list of commands)

172.16.10.0/24 > 172.16.10.212  » [12:34:15] [endpoint.new] endpoint 172.16.10.254 detected as 00:50:56:01:33:70 (VMware, Inc.).
172.16.10.0/24 > 172.16.10.212  » help

           help MODULE : List available commands or show module specific help if no module name is provided.
                active : Show information about active modules.
                  quit : Close the session and exit.
         sleep SECONDS : Sleep for the given amount of seconds.
              get NAME : Get the value of variable NAME, use * alone for all, or NAME* as a wildcard.
        set NAME VALUE : Set the VALUE of variable NAME.
  read VARIABLE PROMPT : Show a PROMPT to ask the user for input that will be saved inside VARIABLE.
                 clear : Clear the screen.
        include CAPLET : Load and run this caplet in the current session.
             ! COMMAND : Execute a shell command and print its output.
        alias MAC NAME : Assign an alias to a given endpoint given its MAC address.

Modules

      any.proxy > not running
       api.rest > not running
      arp.spoof > not running
      ble.recon > not running
        caplets > not running
    dhcp6.spoof > not running
      dns.spoof > not running
  events.stream > running
            gps > not running
     http.proxy > not running
    http.server > not running
    https.proxy > not running
    mac.changer > not running
   mysql.server > not running
      net.probe > not running
      net.recon > running
      net.sniff > not running
   packet.proxy > not running
       syn.scan > not running
      tcp.proxy > not running
         ticker > not running
         update > not running
           wifi > not running
            wol > not running

172.16.10.0/24 > 172.16.10.212  » net.show

+-----------------+--------------------+----------+-------------------------+---------+---------+------------+
|       IP        |        MAC         |  Name    |         Vendor          | Sent    | Recvd  | Last Seen  |
+-----------------+--------------------+----------+-------------------------+---------+---------+------------+
| 172.16.10.212   | 00:b0:52:af:4a:50  | eth0     | Atheros Communications  | 0 B     | 0 B     | 12:34:15   |
| 172.16.10.2     | 00:50:56:13:37:0a  | gateway  | VMware, Inc.            | 49 kB   | 20 kB   | 12:34:15   |
|                 |                    |          |                         |         |         |            |
| 172.16.10.254   | 00:50:56:01:33:70  |          | VMware, Inc.            | 2.4 kB  | 2.4 kB  | 12:35:15   |
+-----------------+--------------------+----------+-------------------------+---------+---------+------------+

↑ 0 B / ↓ 3.2 MB / 11354 pkts / 0 errs
```
