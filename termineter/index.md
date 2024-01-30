---
Title: termineter
Homepage: https://github.com/securestate/termineter
Repository: https://salsa.debian.org/pkg-security-team/termineter
Architectures: all
Version: 1.0.4-2
Metapackages: kali-linux-everything kali-linux-large kali-tools-exploitation 
Icon: images/termineter-logo.svg
PackagesInfo: |
 ### termineter
 
  This package contains a Python framework which provides a platform for the
  security testing of smart meters.  It implements the C1218 and C1219 protocols
  for communication over an optical interface.  Currently supported are Meters
  using C1219-2007 with 7-bit character sets.  This is the most common
  configuration found in North America.  Termineter communicates with Smart
  Meters via a connection using an ANSI type-2 optical probe with a serial
  interface.
 
 **Installed size:** `339 KB`  
 **How to install:** `sudo apt install termineter`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-crcelk
 * python3-pluginbase
 * python3-pyasn1
 * python3-serial
 * python3-smoke-zephyr
 * python3-tabulate
 * python3-termcolor
 {{< /spoiler >}}
 
 ##### termineter
 
 
 ```
 root@kali:~# termineter -h
 usage: termineter [-h] [-v] [-L {DEBUG,INFO,WARNING,ERROR,CRITICAL}]
                   [-r RESOURCE_FILE]
 
 Termineter: Python Smart Meter Testing Framework
 
 options:
   -h, --help            show this help message and exit
   -v, --version         show program's version number and exit
   -L {DEBUG,INFO,WARNING,ERROR,CRITICAL}, --log {DEBUG,INFO,WARNING,ERROR,CRITICAL}
                         set the logging level
   -r RESOURCE_FILE, --rc-file RESOURCE_FILE
                         execute a resource file
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/154407.js" id="asciicast-154407" async></script>

## termineter Usage Example

```
root@kali:~# termineter

   ______              _          __
  /_  __/__ ______ _  (_)__  ___ / /____ ____
   / / / -_) __/  ' \/ / _ \/ -_) __/ -_) __/
  /_/  \__/_/ /_/_/_/_/_//_/\__/\__/\__/_/

  <[ termineter                     v1.0.4
  <[ model:                         T-1000
  <[ loaded modules:                    17

termineter > show modules

Modules
=======

  Name                    Description
  ----------------------  ------------------------------------------------
  brute_force_login       Brute Force Credentials
  diff_tables             Check C12.19 Tables For Differences
  dump_tables             Write Readable C12.19 Tables To A CSV File
  enum_tables             Enumerate Readable C12.19 Tables From The Device
  enum_user_ids           Enumerate Valid User IDs From The Device
  get_identification      Read And Parse The Identification Information
  get_info                Get Basic Meter Information By Reading Tables
  get_local_display_info  Get Information From The Local Display Tables
  get_log_info            Get Information About The Meter's Logs
  get_modem_info          Get Information About The Integrated Modem
  get_security_info       Get Information About The Meter's Access Control
  read_table              Read Data From A C12.19 Table
  remote_reset            Initiate A Reset Procedure
  run_procedure           Initiate A Custom Procedure
  set_meter_id            Set The Meter's I.D.
  set_meter_mode          Change the Meter's Operating Mode
  write_table             Write Data To A C12.19 Table

termineter >
```
