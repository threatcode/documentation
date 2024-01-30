---
Title: hostapd-mana
Homepage: https://github.com/sensepost/hostapd-mana
Repository: https://gitlab.com/kalilinux/packages/hostapd-mana
Architectures: any
Version: 2.6.5+git20200121-0kali5
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hostapd-mana
 
  This package contains a eatureful rogue access point first presented at Defcon
  22.
 
 **Installed size:** `1.27 MB`  
 **How to install:** `sudo apt install hostapd-mana`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnl-3-200 
 * libnl-genl-3-200 
 * libssl3 
 * openssl
 * ssl-cert
 {{< /spoiler >}}
 
 ##### hostapd-mana
 
 
 ```
 root@kali:~# hostapd-mana --help
 hostapd-mana: invalid option -- '-'
 hostapd-mana v2.6
 User space daemon for IEEE 802.11 AP management,
 IEEE 802.1X/WPA/WPA2/EAP/RADIUS Authenticator
 Copyright (c) 2002-2016, Jouni Malinen <j@w1.fi> and contributors
 --------------------------------------------------
 MANA https://github.com/sensepost/hostapd-mana
 By @singe (dominic@sensepost.com)
 Original MANA EAP by Ian (ian@sensepost.com)
 Original karma patches by Robin Wood - robin@digininja.org
 Original EAP patches by Brad Antoniewicz @brad_anton
 Sycophant by Michael Kruger @_cablethief
 usage: hostapd [-hdBKtv] [-P <PID file>] [-e <entropy file>] \
          [-g <global ctrl_iface>] [-G <group>]\
          [-i <comma-separated list of interface names>]\
          <configuration file(s)>
 
 options:
    -h   show this usage
    -d   show more debug messages (-dd for even more)
    -B   run daemon in the background
    -e   entropy file
    -g   global control interface path
    -G   group for control interfaces
    -P   PID file
    -K   include key data in debug messages
    -i   list of interface names to use
    -S   start all the interfaces synchronously
    -t   include timestamps in some debug messages
    -v   show hostapd version
 ```
 
 - - -
 
 ##### hostapd-mana_cli
 
 
 ```
 root@kali:~# hostapd-mana_cli -h
 hostapd_cli v2.6
 Copyright (c) 2004-2016, Jouni Malinen <j@w1.fi> and contributors
 
 usage: hostapd_cli [-p<path>] [-i<ifname>] [-hvB] [-a<path>] \
                    [-P<pid file>] [-G<ping interval>] [command..]
 
 Options:
    -h           help (show this usage text)
    -v           shown version information
    -p<path>     path to find control sockets (default: /var/run/hostapd-mana)
    -s<dir_path> dir path to open client sockets (default: /var/run/hostapd-mana)
    -a<file>     run in daemon mode executing the action file based on events
                 from hostapd
    -B           run a daemon in the background
    -i<ifname>   Interface to listen on (default: first interface found in the
                 socket path)
 
 commands:
   ping = pings hostapd
   mib = get MIB variables (dot1x, dot11, radius)
   sta <addr> = get MIB variables for one station
   all_sta = get MIB variables for all stations
   new_sta <addr> = add a new station
   deauthenticate <addr> = deauthenticate a station
   disassociate <addr> = disassociate a station
   signature <addr> = get taxonomy signature for a station
   sa_query <addr> = send SA Query to a station
   get_config = show current configuration
   help = show this usage help
   interface [ifname] = show interfaces/select interface
   level <debug level> = change debug level
   license = show full hostapd_cli license
   quit = exit hostapd_cli
   mana_change_ssid = change the default SSID for when mana is off
   mana_get_ssid = get the default SSID for when mana is off
   mana_get_state = get whether mana is enabled or not
   mana_disable = disable mana
   mana_enable = enable mana
   mana_loud_off = disable mana's loud mode
   mana_loud_on = enable mana's loud mode
   mana_loud_state = check mana's loud mode
   mana_macacl_off = disable MAC ACLs at management frame level
   mana_macacl_on = enable MAC ACLs at management frame level
   mana_macacl_state = check mana's MAC ACL mode
   mana_wpe_off = disable mana's wpe mode
   mana_wpe_on = enable mana's wpe mode
   mana_wpe_state = check mana's wpe mode
   mana_eapsuccess_off = disable mana's eapsuccess mode
   mana_eapsuccess_on = enable mana's eapsuccess mode
   mana_eapsuccess_state = check mana's eapsuccess mode
   mana_eaptls_off = disable mana's eaptls mode
   mana_eaptls_on = enable mana's eaptls mode
   mana_eaptls_state = check mana's eaptls mode
   sycophant_get_state = get whether sycophant is enabled or not
   sycophant_disable = disable sycophant
   sycophant_enable = enable sycophant
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
