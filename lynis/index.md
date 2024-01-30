---
Title: lynis
Homepage: https://cisofy.com/lynis/
Repository: https://salsa.debian.org/debian/lynis
Architectures: all
Version: 3.0.9-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-vulnerability 
Icon: images/lynis-logo.svg
PackagesInfo: |
 ### lynis
 
  Lynis is an auditing tool for hardening GNU/Linux and Unix based systems.
  It scans the system configuration and creates an overview of system information
  and security issues usable by professional auditors.
  It can assist in automated audits.
   
  Lynis can be used in addition to other software, like security
  scanners, system benchmarking and fine-tuning tools.
 
 **Installed size:** `1.61 MB`  
 **How to install:** `sudo apt install lynis`  
 
 {{< spoiler "Dependencies:" >}}
 * e2fsprogs
 {{< /spoiler >}}
 
 ##### lynis
 
 System and security auditing tool
 
 ```
 root@kali:~# lynis -h
 
 [ Lynis 3.0.9 ]
 
 ################################################################################
   Lynis comes with ABSOLUTELY NO WARRANTY. This is free software, and you are
   welcome to redistribute it under the terms of the GNU General Public License.
   See the LICENSE file for details about using this software.
 
   2007-2021, CISOfy - https://cisofy.com/lynis/
   Enterprise support available (compliance, plugins, interface and tools)
 ################################################################################
 
 
 [+] Initializing program
 ------------------------------------
 
 
   Usage: lynis command [options]
 
 
   Command:
 
     audit
         audit system                  : Perform local security scan
         audit system remote <host>    : Remote security scan
         audit dockerfile <file>       : Analyze Dockerfile
 
     show
         show                          : Show all commands
         show version                  : Show Lynis version
         show help                     : Show help
 
     update
         update info                   : Show update details
 
 
   Options:
 
     Alternative system audit modes
     --forensics                       : Perform forensics on a running or mounted system
     --pentest                         : Non-privileged, show points of interest for pentesting
 
     Layout options
     --no-colors                       : Don't use colors in output
     --quiet (-q)                      : No output
     --reverse-colors                  : Optimize color display for light backgrounds
     --reverse-colours                 : Optimize colour display for light backgrounds
 
     Misc options
     --debug                           : Debug logging to screen
     --no-log                          : Don't create a log file
     --profile <profile>               : Scan the system with the given profile file
     --view-manpage (--man)            : View man page
     --verbose                         : Show more details on screen
     --version (-V)                    : Display version number and quit
     --wait                            : Wait between a set of tests
     --slow-warning <seconds>  : Threshold for slow test warning in seconds (default 10)
 
     Enterprise options
     --plugindir <path>                : Define path of available plugins
     --upload                          : Upload data to central node
 
     More options available. Run '/usr/sbin/lynis show options', or use the man page.
 
 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## lynis Usage Example

Scan the system in quiet mode (`-Q`) and output in cronjob format (`–cronjob`):

````
root@kali:~# lynis -Q --cronjob

[ Lynis 2.6.2 ]

################################################################################
  Lynis comes with ABSOLUTELY NO WARRANTY. This is free software, and you are
  welcome to redistribute it under the terms of the GNU General Public License.
  See the LICENSE file for details about using this software.

  2007-2018, CISOfy - https://cisofy.com/lynis/
  Enterprise support available (compliance, plugins, interface and tools)
################################################################################


[+] Initializing program
------------------------------------
- Detecting OS...  [ DONE ]
- Checking profiles... [ DONE ]

  ---------------------------------------------------
  Program version:           2.6.2
  Operating system:          Linux
  Operating system name:     Debian
  Operating system version:  kali-rolling
  Kernel version:            4.18.0
  Hardware platform:         x86_64
  Hostname:                  kali
  ---------------------------------------------------
  Profiles:                  /etc/lynis/default.prf
  Log file:                  /var/log/lynis.log
  Report file:               /var/log/lynis-report.dat
  Report version:            1.0
  Plugin directory:          /etc/lynis/plugins
  ---------------------------------------------------
  Auditor:                   [Not Specified]
  Language:                  en
  Test category:             all
  Test group:                all
  ---------------------------------------------------
[...]
```
