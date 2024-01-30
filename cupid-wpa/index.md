---
Title: cupid-wpa
Homepage: https://github.com/lgrangeia/cupid/
Repository: https://gitlab.com/kalilinux/packages/cupid-wpa
Architectures: linux-any kfreebsd-any
Version: 1:2.1-0.1kali7
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cupid-hostapd
 
  cupid-hostapd provide a binary of the same name that has been patched
  to exploit the heartbleed vulnerability over EAP TLS tunneled protocols
  (EAP-PEAP, EAP-TLS, EAP-TTLS) in use in wireless networks.
   
  With cupid-hostapd you can setup a fake wireless network to exploit
  the vulnerability of terminals that try to connect to it.
   
  Please see presentation slides for a simple introduction to cupid:
  http://www.slideshare.net/lgrangeia
 
 **Installed size:** `740 KB`  
 **How to install:** `sudo apt install cupid-hostapd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnl-3-200 
 * libnl-genl-3-200 
 * libunsafessl1.0.2
 {{< /spoiler >}}
 
 ##### cupid-hostapd
 
 IEEE 802.11 AP, IEEE 802.1X/WPA/WPA2/EAP/RADIUS Authenticator
 
 ```
 root@kali:~# cupid-hostapd --help
 cupid-hostapd: invalid option -- '-'
 hostapd v2.1
 User space daemon for IEEE 802.11 AP management,
 IEEE 802.1X/WPA/WPA2/EAP/RADIUS Authenticator
 Copyright (c) 2002-2014, Jouni Malinen <j@w1.fi> and contributors
 
 usage: hostapd [-hdBKtv] [-P <PID file>] [-e <entropy file>] \
          [-g <global ctrl_iface>] [-G <group>] \
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
    -t   include timestamps in some debug messages
    -v   show hostapd version
 ```
 
 - - -
 
 ##### cupid-hostapd_cli
 
 Hostapd command-line interface
 
 ```
 root@kali:~# cupid-hostapd_cli -h
 hostapd_cli v2.1
 Copyright (c) 2004-2014, Jouni Malinen <j@w1.fi> and contributors
 
 usage: hostapd_cli [-p<path>] [-i<ifname>] [-hvB] [-a<path>] \
                    [-G<ping interval>] [command..]
 
 Options:
    -h           help (show this usage text)
    -v           shown version information
    -p<path>     path to find control sockets (default: /var/run/hostapd)
    -a<file>     run in daemon mode executing the action file based on events
                 from hostapd
    -B           run a daemon in the background
    -i<ifname>   Interface to listen on (default: first interface found in the
                 socket path)
 
 Commands:
    mib                  get MIB variables (dot1x, dot11, radius)
    sta <addr>           get MIB variables for one station
    all_sta              get MIB variables for all stations
    new_sta <addr>       add a new station
    deauthenticate <addr>  deauthenticate a station
    disassociate <addr>  disassociate a station
    get_config           show current configuration
    help                 show this usage help
    interface [ifname]   show interfaces/select interface
    level <debug level>  change debug level
    license              show full hostapd_cli license
    quit                 exit hostapd_cli
 ```
 
 - - -
 
 ### cupid-wpasupplicant
 
  cupid-wpasupplicant provides a binary of the same name that has been patched
  to exploit the heartbleed vulnerability over EAP TLS tunneled protocols
  (EAP-PEAP, EAP-TLS, EAP-TTLS) in use in wireless networks.
   
  With cupid-wpasupplicant you can try to exploit the vulnerability on
  wireless access points.
   
  Please see presentation slides for a simple introduction to cupid:
  http://www.slideshare.net/lgrangeia
 
 **Installed size:** `2.16 MB`  
 **How to install:** `sudo apt install cupid-wpasupplicant`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * libdbus-1-3 
 * libnl-3-200 
 * libnl-genl-3-200 
 * libpcsclite1 
 * libreadline8 
 * libunsafessl1.0.2
 {{< /spoiler >}}
 
 ##### cupid-wpa_cli
 
 WPA command line client
 
 ```
 root@kali:~# cupid-wpa_cli -h
 wpa_cli [-p<path to ctrl sockets>] [-i<ifname>] [-hvB] [-a<action file>] \
         [-P<pid file>] [-g<global ctrl>] [-G<ping interval>]  [command..]
   -h = help (show this usage text)
   -v = shown version information
   -a = run in daemon mode executing the action file based on events from
        wpa_supplicant
   -B = run a daemon in the background
   default path: /var/run/wpa_supplicant
   default interface: first interface found in socket path
 commands:
   status [verbose] = get current WPA/EAPOL/EAP status
   ifname = get current interface name
   ping = pings wpa_supplicant
   relog = re-open log-file (allow rolling logs)
   note <text> = add a note to wpa_supplicant debug log
   mib = get MIB variables (dot1x, dot11)
   help [command] = show usage help
   interface [ifname] = show interfaces/select interface
   level <debug level> = change debug level
   license = show full wpa_cli license
   quit = exit wpa_cli
   set = set variables (shows list of variables when run without arguments)
   get <name> = get information
   logon = IEEE 802.1X EAPOL state machine logon
   logoff = IEEE 802.1X EAPOL state machine logoff
   pmksa = show PMKSA cache
   reassociate = force reassociation
   preauthenticate <BSSID> = force preauthentication
   identity <network id> <identity> = configure identity for an SSID
   password <network id> <password> = configure password for an SSID
   new_password <network id> <password> = change password for an SSID
   pin <network id> <pin> = configure pin for an SSID
   otp <network id> <password> = configure one-time-password for an SSID
   passphrase <network id> <passphrase> = configure private key passphrase
     for an SSID
   sim <network id> <pin> = report SIM operation result
   bssid <network id> <BSSID> = set preferred BSSID for an SSID
   blacklist <BSSID> = add a BSSID to the blacklist
   blacklist clear = clear the blacklist
   blacklist = display the blacklist
   log_level <level> [<timestamp>] = update the log level/timestamp
   log_level = display the current log level and log options
   list_networks = list configured networks
   select_network <network id> = select a network (disable others)
   enable_network <network id> = enable a network
   disable_network <network id> = disable a network
   add_network = add a network
   remove_network <network id> = remove a network
   set_network <network id> <variable> <value> = set network variables (shows
     list of variables when run without arguments)
   get_network <network id> <variable> = get network variables
   list_creds = list configured credentials
   add_cred = add a credential
   remove_cred <cred id> = remove a credential
   set_cred <cred id> <variable> <value> = set credential variables
   save_config = save the current configuration
   disconnect = disconnect and wait for reassociate/reconnect command before
     connecting
   reconnect = like reassociate, but only takes effect if already disconnected
   scan = request new BSS scan
   scan_results = get latest scan results
   bss <<idx> | <bssid>> = get detailed scan result info
   get_capability <eap/pairwise/group/key_mgmt/proto/auth_alg/channels/freq/modes> = get capabilies
   reconfigure = force wpa_supplicant to re-read its configuration file
   terminate = terminate wpa_supplicant
   interface_add <ifname> <confname> <driver> <ctrl_interface> <driver_param>
     <bridge_name> = adds new interface, all parameters but <ifname>
     are optional
   interface_remove <ifname> = removes the interface
   interface_list = list available interfaces
   ap_scan <value> = set ap_scan parameter
   scan_interval <value> = set scan_interval parameter (in seconds)
   bss_expire_age <value> = set BSS expiration age parameter
   bss_expire_count <value> = set BSS expiration scan count parameter
   bss_flush <value> = set BSS flush age (0 by default)
   stkstart <addr> = request STK negotiation with <addr>
   ft_ds <addr> = request over-the-DS FT with <addr>
   wps_pbc [BSSID] = start Wi-Fi Protected Setup: Push Button Configuration
   wps_pin <BSSID> [PIN] = start WPS PIN method (returns PIN, if not hardcoded)
   wps_check_pin <PIN> = verify PIN checksum
   wps_cancel Cancels the pending WPS operation
   wps_nfc [BSSID] = start Wi-Fi Protected Setup: NFC
   wps_nfc_config_token <WPS|NDEF> = build configuration token
   wps_nfc_token <WPS|NDEF> = create password token
   wps_nfc_tag_read <hexdump of payload> = report read NFC tag with WPS data
   nfc_get_handover_req <NDEF> <WPS> = create NFC handover request
   nfc_get_handover_sel <NDEF> <WPS> = create NFC handover select
   nfc_rx_handover_req <hexdump of payload> = report received NFC handover request
   nfc_rx_handover_sel <hexdump of payload> = report received NFC handover select
   nfc_report_handover <role> <type> <hexdump of req> <hexdump of sel> = report completed NFC handover
   wps_reg <BSSID> <AP PIN> = start WPS Registrar to configure an AP
   wps_ap_pin [params..] = enable/disable AP PIN
   wps_er_start [IP address] = start Wi-Fi Protected Setup External Registrar
   wps_er_stop = stop Wi-Fi Protected Setup External Registrar
   wps_er_pin <UUID> <PIN> = add an Enrollee PIN to External Registrar
   wps_er_pbc <UUID> = accept an Enrollee PBC using External Registrar
   wps_er_learn <UUID> <PIN> = learn AP configuration
   wps_er_set_config <UUID> <network id> = set AP configuration for enrolling
   wps_er_config <UUID> <PIN> <SSID> <auth> <encr> <key> = configure AP
   wps_er_nfc_config_token <WPS/NDEF> <UUID> = build NFC configuration token
   ibss_rsn <addr> = request RSN authentication with <addr> in IBSS
   sta <addr> = get information about an associated station (AP)
   all_sta = get information about all associated stations (AP)
   deauthenticate <addr> = deauthenticate a station
   disassociate <addr> = disassociate a station
   chan_switch <cs_count> <freq> [sec_channel_offset=] [center_freq1=] [center_freq2=] [bandwidth=] [blocktx] [ht|vht] = CSA parameters
   suspend = notification of suspend/hibernate
   resume = notification of resume/thaw
   drop_sa = drop SA without deauth/disassoc (test command)
   roam <addr> = roam to the specified BSS
   p2p_find [timeout] [type=*] = find P2P Devices for up-to timeout seconds
   p2p_stop_find = stop P2P Devices search
   p2p_connect <addr> <"pbc"|PIN> [ht40] = connect to a P2P Device
   p2p_listen [timeout] = listen for P2P Devices for up-to timeout seconds
   p2p_group_remove <ifname> = remove P2P group interface (terminate group if GO)
   p2p_group_add [ht40] = add a new P2P group (local end as GO)
   p2p_prov_disc <addr> <method> = request provisioning discovery
   p2p_get_passphrase = get the passphrase for a group (GO only)
   p2p_serv_disc_req <addr> <TLVs> = schedule service discovery request
   p2p_serv_disc_cancel_req <id> = cancel pending service discovery request
   p2p_serv_disc_resp <freq> <addr> <dialog token> <TLVs> = service discovery response
   p2p_service_update = indicate change in local services
   p2p_serv_disc_external <external> = set external processing of service discovery
   p2p_service_flush = remove all stored service entries
   p2p_service_add <bonjour|upnp> <query|version> <response|service> = add a local service
   p2p_service_del <bonjour|upnp> <query|version> [|service] = remove a local service
   p2p_reject <addr> = reject connection attempts from a specific peer
   p2p_invite <cmd> [peer=addr] = invite peer
   p2p_peers [discovered] = list known (optionally, only fully discovered) P2P peers
   p2p_peer <address> = show information about known P2P peer
   p2p_set <field> <value> = set a P2P parameter
   p2p_flush = flush P2P state
   p2p_cancel = cancel P2P group formation
   p2p_unauthorize <address> = unauthorize a peer
   p2p_presence_req [<duration> <interval>] [<duration> <interval>] = request GO presence
   p2p_ext_listen [<period> <interval>] = set extended listen timing
   p2p_remove_client <address|iface=address> = remove a peer from all groups
   wfd_subelem_set <subelem> [contents] = set Wi-Fi Display subelement
   wfd_subelem_get <subelem> = get Wi-Fi Display subelement
   fetch_anqp = fetch ANQP information for all APs
   stop_fetch_anqp = stop fetch_anqp operation
   interworking_select [auto] = perform Interworking network selection
   interworking_connect <BSSID> = connect using Interworking credentials
   anqp_get <addr> <info id>[,<info id>]... = request ANQP information
   gas_request <addr> <AdvProtoID> [QueryReq] = GAS request
   gas_response_get <addr> <dialog token> [start,len] = Fetch last GAS response
   hs20_anqp_get <addr> <subtype>[,<subtype>]... = request HS 2.0 ANQP information
   nai_home_realm_list <addr> <home realm> = get HS20 nai home realm list
   sta_autoconnect <0/1> = disable/enable automatic reconnection
   tdls_discover <addr> = request TDLS discovery with <addr>
   tdls_setup <addr> = request TDLS setup with <addr>
   tdls_teardown <addr> = tear down TDLS with <addr>
   signal_poll = get signal parameters
   pktcnt_poll = get TX/RX packet counters
   reauthenticate = trigger IEEE 802.1X/EAPOL reauthentication
   autoscan [params] = Set or unset (if none) autoscan parameters
   wnm_sleep <enter/exit> [interval=#] = enter/exit WNM-Sleep mode
   wnm_bss_query <query reason> = Send BSS Transition Management Query
   raw <params..> = Sent unprocessed command
   flush = flush wpa_supplicant state
   radio_work = radio_work <show/add/done>
 ```
 
 - - -
 
 ##### cupid-wpa_passphrase
 
 Generate a WPA PSK from an ASCII passphrase for a SSID
 
 ```
 root@kali:~# man cupid-wpa_passphrase
 WPA_PASSPHRASE(8)                                            WPA_PASSPHRASE(8)
 
 NAME
        wpa_passphrase - Generate a WPA PSK from an ASCII passphrase for a SSID
 
 SYNOPSIS
        wpa_passphrase [ ssid ] [ passphrase ]
 
 OVERVIEW
        wpa_passphrase  pre-computes  PSK  entries  for  network  configuration
        blocks of a wpa_supplicant.conf file. An ASCII passphrase and SSID  are
        used to generate a 256-bit PSK.
 
 OPTIONS
        ssid   The SSID whose passphrase should be derived.
 
        passphrase
               The  passphrase  to  use.  If  not included on the command line,
               passphrase will be read from standard input.
 
 SEE ALSO
        wpa_supplicant.conf(5) wpa_supplicant(8)
 
 LEGAL
        wpa_supplicant is copyright (c) 2003-2014, Jouni Malinen <j@w1.fi>  and
        contributors.  All Rights Reserved.
 
        This program is licensed under the BSD license (the one with advertise-
        ment clause removed).
 
                                 10 October 2023              WPA_PASSPHRASE(8)
 ```
 
 - - -
 
 ##### cupid-wpa_supplicant
 
 Wi-Fi Protected Access client and IEEE 802.1X supplicant
 
 ```
 root@kali:~# cupid-wpa_supplicant -h
 wpa_supplicant v2.1
 Copyright (c) 2003-2014, Jouni Malinen <j@w1.fi> and contributors
 
 This software may be distributed under the terms of the BSD license.
 See README for more details.
 
 This product includes software developed by the OpenSSL Project
 for use in the OpenSSL Toolkit (http://www.openssl.org/)
 
 usage:
   wpa_supplicant [-BddhKLqqstuvW] [-P<pid file>] [-g<global ctrl>] \
         [-G<group>] \
         -i<ifname> -c<config file> [-C<ctrl>] [-D<driver>] [-p<driver_param>] \
         [-b<br_ifname>] [-e<entropy file>] [-f<debug file>] \
         [-o<override driver>] [-O<override ctrl>] \
         [-N -i<ifname> -c<conf> [-C<ctrl>] [-D<driver>] \
         [-p<driver_param>] [-b<br_ifname>] [-I<config file>] ...]
 
 drivers:
   nl80211 = Linux nl80211/cfg80211
   wext = Linux wireless extensions (generic)
   wired = Wired Ethernet driver
   none = no driver (RADIUS server/WPS ER)
 options:
   -b = optional bridge interface name
   -B = run daemon in the background
   -c = Configuration file
   -C = ctrl_interface parameter (only used if -c is not)
   -i = interface name
   -I = additional configuration file
   -d = increase debugging verbosity (-dd even more)
   -D = driver name (can be multiple drivers: nl80211,wext)
   -e = entropy file
   -f = log output to debug file instead of stdout
   -g = global ctrl_interface
   -G = global ctrl_interface group
   -K = include keys (passwords, etc.) in debug output
   -s = log output to syslog instead of stdout
   -T = record to Linux tracing in addition to logging
        (records all messages regardless of debug verbosity)
   -t = include timestamp in debug messages
   -h = show this help text
   -L = show license (BSD)
   -o = override driver parameter for new interfaces
   -O = override ctrl_interface parameter for new interfaces
   -p = driver parameters
   -P = PID file
   -q = decrease debugging verbosity (-qq even less)
   -u = enable DBus control interface
   -v = show version
   -W = wait for a control interface monitor before starting
   -N = start describing new interface
 example:
   wpa_supplicant -Dnl80211 -iwlan0 -c/etc/wpa_supplicant.conf
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
