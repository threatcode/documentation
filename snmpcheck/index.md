---
Title: snmpcheck
Homepage: http://www.nothink.org/codes/snmpcheck/index.php
Repository: https://gitlab.com/kalilinux/packages/snmpcheck
Architectures: all
Version: 1.9-0kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### snmpcheck
 
  Like to snmpwalk, snmpcheck allows you to enumerate the SNMP
  devices and places the output in a very human readable
  friendly format. It could be useful for penetration testing
  or systems monitoring.
 
 **Installed size:** `46 KB`  
 **How to install:** `sudo apt install snmpcheck`  
 
 {{< spoiler "Dependencies:" >}}
 * libnet-snmp-perl
 * libnumber-bytes-human-perl
 * perl
 * ruby
 * ruby-snmp
 {{< /spoiler >}}
 
 ##### snmp-check
 
 SNMP device enumerator
 
 ```
 root@kali:~# snmp-check -h
 snmp-check v1.9 - SNMP enumerator
 Copyright (c) 2005-2015 by Matteo Cantoni (www.nothink.org)
 
  Usage: snmp-check [OPTIONS] <target IP address>
 
   -p --port        : SNMP port. Default port is 161;
   -c --community   : SNMP community. Default is public;
   -v --version     : SNMP version (1,2c). Default is 1;
 
   -w --write       : detect write access (separate action by enumeration);
 
   -d --disable_tcp : disable TCP connections enumeration!
   -t --timeout     : timeout in seconds. Default is 5;
   -r --retries     : request retries. Default is 1; 
   -i --info        : show script version;
   -h --help        : show help menu;
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## snmp-check Usage Example

Scan the target host (`192.168.1.2`) using the public SNMP community string (`-c public`):

```
root@kali:~# snmp-check 192.168.1.2 -c public
snmp-check v1.9 - SNMP enumerator
Copyright (c) 2005-2015 by Matteo Cantoni (www.nothink.org)

[+] Try to connect to 192.168.1.2:161 using SNMPv1 and community 'public'

[*] System information:

  Host IP address               : 192.168.1.2
  Hostname                      : ...retracted...
  Description                   : ...retracted...
  Contact                       : ...retracted...
  Location                      : ...retracted...
  Uptime snmp                   : -
  Uptime system                 : 3 days, 00:13:51.05
  System date                   : -

[*] Network information:

[...]

[*] Network interfaces:

[...]

[*] Network IP:

[...]

[*] Routing information:

[...]

[*] TCP connections and listening ports:

[...]

[*] Listening UDP ports:

[...]

root@kali:~#
```
