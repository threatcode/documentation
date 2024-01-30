---
Title: vpnc
Homepage: https://github.com/streambinder/vpnc
Repository: https://salsa.debian.org/debian/vpnc
Architectures: any
Version: 0.5.3+git20220927-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### vpnc
 
  vpnc is a VPN client compatible with cisco3000 VPN Concentrator (also
  known as Cisco's EasyVPN equipment). vpnc runs entirely in userspace
  and does not require kernel modules except for the tun driver to
  communicate with the network layer.
   
  It supports most of the features needed to establish connection to the
  VPN concentrator: MD5 and SHA1 hashes, 3DES and AES ciphers, PFS and
  various IKE DH group settings.
 
 **Installed size:** `231 KB`  
 **How to install:** `sudo apt install vpnc`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcrypt20 
 * libgnutls30 
 * perl
 * vpnc-scripts
 {{< /spoiler >}}
 
 ##### cisco-decrypt
 
 Decrypts an obfuscated Cisco vpn client pre-shared key
 
 ```
 root@kali:~# cisco-decrypt -h
 
 Usage: cisco-decrypt DEADBEEF...012345678 424242...7261
     Print decoded result to stdout
 
 ```
 
 - - -
 
 ##### pcf2vpnc
 
 Converts VPN-config files from pcf to vpnc-format
 
 ```
 root@kali:~# man pcf2vpnc
 PCF2VPNC(1)                          vpnc                          PCF2VPNC(1)
 
 NAME
        pcf2vpnc - converts VPN-config files from pcf to vpnc-format
 
 SYNOPSIS
        pcf2vpnc <pcf file> [vpnc file]
 
 DESCRIPTION
        This  script  accompanies vpnc. It attempts to convert *.pcf-configura-
        tion files often spread with proprietary (read Cisco) VPN-clients  into
        vpnc-configuration files, usually named *.conf.
 
        If  [vpnc file] is not specified, the result will be printed to STDOUT.
        If specified, it will be written to that file. Please make sure that it
        has appropriate permissions as it may contain sensitive data!
 
 AUTHOR
        pcf2vpnc was originally written by Stefan  Tomanek.  Updates  and  this
        man-page were made by Wolfram Sang (ninja(at)the-dreams.de).
 
        Permission  is  granted to copy, distribute and/or modify this document
        under the terms of the GNU General Public License, Version 2 any  later
        version published by the Free Software Foundation.
 
        On  Debian systems, the complete text of the GNU General Public License
        can be found in /usr/share/common-licenses/GPL.
 
 SEE ALSO
        vpnc(8) cisco-decrypt(8)
 
 pcf2vpnc                           June 2007                       PCF2VPNC(1)
 ```
 
 - - -
 
 ##### vpnc
 
 Client for Cisco VPN3000 Concentrator, IOS and PIX
 
 ```
 root@kali:~# vpnc --help
 Usage: vpnc [--version] [--print-config] [--help] [--long-help] [options] [config files]
 
 Options:
   --gateway <ip/hostname>
       IP/name of your IPSec gateway
   conf-variable: IPSec gateway<ip/hostname>
 
   --id <ASCII string>
       your group name
   conf-variable: IPSec ID<ASCII string>
 
   --secret <ASCII string>
       your group password (cleartext)
   conf-variable: IPSec secret<ASCII string>
 
   --username <ASCII string>
       your username
   conf-variable: Xauth username<ASCII string>
 
   --password <ASCII string>
       your password (cleartext)
   conf-variable: Xauth password<ASCII string>
 
 Use --long-help to see all options
 
 Report bugs to vpnc@unix-ag.uni-kl.de
 ```
 
 - - -
 
 ##### vpnc-connect
 
 Client for Cisco VPN3000 Concentrator, IOS and PIX
 
 ```
 root@kali:~# vpnc-connect --help
 Usage: vpnc-connect [--version] [--print-config] [--help] [--long-help] [options] [config files]
 
 Options:
   --gateway <ip/hostname>
       IP/name of your IPSec gateway
   conf-variable: IPSec gateway<ip/hostname>
 
   --id <ASCII string>
       your group name
   conf-variable: IPSec ID<ASCII string>
 
   --secret <ASCII string>
       your group password (cleartext)
   conf-variable: IPSec secret<ASCII string>
 
   --username <ASCII string>
       your username
   conf-variable: Xauth username<ASCII string>
 
   --password <ASCII string>
       your password (cleartext)
   conf-variable: Xauth password<ASCII string>
 
 Use --long-help to see all options
 
 Report bugs to vpnc@unix-ag.uni-kl.de
 ```
 
 - - -
 
 ##### vpnc-disconnect
 
 Client for Cisco VPN3000 Concentrator, IOS and PIX
 
 ```
 root@kali:~# vpnc-disconnect -h
 Usage: /usr/sbin/vpnc-disconnect
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
