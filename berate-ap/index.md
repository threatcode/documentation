---
Title: berate-ap
Homepage: https://github.com/sensepost/berate_ap
Repository: https://gitlab.com/kalilinux/packages/berate-ap
Architectures: any
Version: 0.4.6+git20191120-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### berate-ap
 
  This package contains a script for orchestrating mana rogue Wi-Fi Access
  Points. It can also handle regular hostapd AP and create AP easily.
 
 **Installed size:** `101 KB`  
 **How to install:** `sudo apt install berate-ap`  
 
 {{< spoiler "Dependencies:" >}}
 * hostapd-mana
 * iproute2
 * iw
 * procps
 {{< /spoiler >}}
 
 ##### berate_ap
 
 
 ```
 root@kali:~# berate_ap -h
 Usage: berate_ap [options] <wifi-interface> [<interface-with-internet>] [<access-point-name> [<passphrase>]]
 
 Options:
   -h, --help              Show this help
   --version               Print version number
   -c <channel>            Channel number (default: 1)
   -w <WPA version>        Use 1 for WPA, use 2 for WPA2, 3 for WPA3, use 1+2 for WPA/2 (default), or 2+3 for WPA3/2 transition
   -n                      Disable Internet sharing (if you use this, don't pass
                           the <interface-with-internet> argument)
   -m <method>             Method for Internet sharing.
                           Use: 'nat' for NAT (default)
                                'bridge' for bridging
                                'none' for no Internet sharing (equivalent to -n)
   --psk                   Use 64 hex digits pre-shared-key instead of passphrase
   --hidden                Make the Access Point hidden (do not broadcast the SSID)
   --mac-filter            Enable MAC address filtering
   --mac-filter-accept     Location of MAC address filter list (defaults to /etc/hostapd/hostapd.accept)
   --redirect-to-localhost If -n is set, redirect every web request to localhost (useful for public information networks)
   --hostapd-debug <level> With level between 1 and 2, passes arguments -d or -dd to hostapd for debugging.
   --isolate-clients       Disable communication between clients
   --ieee80211n            Enable IEEE 802.11n (HT)
   --ieee80211ac           Enable IEEE 802.11ac (VHT)
   --ht_capab <HT>         HT capabilities (default: [HT40+])
   --vht_capab <VHT>       VHT capabilities
   --country <code>        Set two-letter country code for regularity (example: US)
   --freq-band <GHz>       Set frequency band. Valid inputs: 2.4, 5 (default: 2.4)
   --driver                Choose your WiFi adapter driver (default: nl80211)
   --ieee80211w <0-2>      Enable IEEE 802.11w Management Frame Protection (MFP). 0 disabled (default), 1 optional , 2 mandatory
   --no-virt               Do not create virtual interface
   --no-haveged            Do not run 'haveged' automatically when needed
   --fix-unmanaged         If NetworkManager shows your interface as unmanaged after you
                           close create_ap, then use this option to switch your interface
                           back to managed
   --mac <MAC>             Set MAC address
   --dhcp-dns <IP1[,IP2]>  Set DNS returned by DHCP
   --daemon                Run create_ap in the background
   --stop <id>             Send stop command to an already running create_ap. For an <id>
                           you can put the PID of create_ap or the WiFi interface. You can
                           get them with --list-running
   --list-running          Show the create_ap processes that are already running
   --list-clients <id>     List the clients connected to create_ap instance associated with <id>.
                           For an <id> you can put the PID of create_ap or the WiFi interface.
                           If virtual WiFi interface was created, then use that one.
                           You can get them with --list-running
   --mkconfig <conf_file>  Store configs in conf_file
   --config <conf_file>    Load configs from conf_file
 
 Enterprise Options:
   --eap                   Enable Enterprise (EAP) wireless settings
                           Default is to use built in RADIUS server
 
                           *Built in RADIUS server*
   --eap-user-file         Full path to EAP user file
                           Default will use Manas hostapd.eap_user
   --eap-cert-subj         Set or modify certificate subject
   --eap-cert-path         Full path to wireless certificates
                           Name of the certs at the location:
                               - hostapd.ca.pem
                               - hostapd.dh.pem
                               - hostapd.cert.pem
                               - hostapd.key.pem
                           You will be prompted to generate a cert if no path is provided
   --eap-key-passwd        If key requires a password
 
                           *Use external RADIUS server*
   --radius-server         Use an external RADIUS server rather than built in
                           Default port is 1812
                               --remote-radius <ip address>[:port]
   --radius-secret         Provide shared RADIUS secret
 
 Mana WPE Options:
   --mana-wpe              Enable WPE mode
                           Will intercept various EAP credentials
   --mana-credout <file>   Set location of output creds file
                           Default location is at /tmp/hostapd.credout
   --mana-eapsuccess       Always return an EAP success message
   --mana-eaptls           Accept any EAP-TLS client certificate
 
 Mana/Karma Options:
   --mana                  Enable Mana Attack
                           Will respond affirmative to all device access point probes
   --mana-loud             Enable Mana loud mode
                           Will respond with all seen access points to devices
   --mana-whitelist <list> Provide a list of SSIDs to respond to
   --mana-logging          Enable Device logging to file, taxonomy enabled by default
                           Default output location is at /tmp/hostapd.manaout
   --mana-manaout <file>   Set location of output mana logging file
 
 MANA Other Options:
   --mana-wpa              Enable MANA WPA handshake capture
                           Mana can capture handshakes for users attempting to connect which are then placed
                           into hashcats hccpx format. 
                           PLEASE NOTE: This attack currently does not work with mana enabled so the correct
                           ESSID will have to be specified
                           Default output location is at /tmp/hostapd.hccapx
   --mana-wpaout <file>    Set location of output for wpa-psk handshakes
   --colour                Colourise MANA output and credential capture so its easier to distinguish
   --vanilla               By default berate_ap will use hostapd_mana,
                           if you would like to use vanilla hostapd please use this flag
                           Using this flag will prevent evil mana operations
 
 wpa_sycophant Options:
   --wpa-sycophant         Enable the enable_sycophant flag in MANA
                           wpa_sycophant is a tool used to relay MSCHAP authentication attempts
                           between a rogue AP and a legitimate AP
                           This may be used to authenticate to a legitimate AP using someone elses login attempt
                           similar to a tool like Impackets ntlmrelayx.py in the wired world.
                           This option needs to be used in conjunction with https://github.com/sensepost/wpa_sycophant
 Non-Bridging Options:
   --no-dns                Disable dnsmasq DNS server
   --no-dnsmasq            Disable dnsmasq server completely
   -g <gateway>            IPv4 Gateway for the Access Point (default: 192.168.12.1)
   -d                      DNS server will take into account /etc/hosts
   -e <hosts_file>         DNS server will take into account additional hosts file
 
 Useful informations:
   * If you're not using the --no-virt option, then you can create an AP with the same
     interface you are getting your Internet connection.
   * You can pass your SSID and password through pipe or through arguments (see examples).
   * On bridge method if the <interface-with-internet> is not a bridge interface, then
     a bridge interface is created automatically.
 
 Examples:
   berate_ap wlan0 eth0 MyAccessPoint MyPassPhrase
   echo -e 'MyAccessPoint\nMyPassPhrase' | berate_ap wlan0 eth0
   berate_ap wlan0 eth0 MyAccessPoint
   echo 'MyAccessPoint' | berate_ap wlan0 eth0
   berate_ap wlan0 wlan0 MyAccessPoint MyPassPhrase
   berate_ap -n wlan0 MyAccessPoint MyPassPhrase
   berate_ap -m bridge wlan0 eth0 MyAccessPoint MyPassPhrase
   berate_ap -m bridge wlan0 br0 MyAccessPoint MyPassPhrase
   berate_ap --driver rtl871xdrv wlan0 eth0 MyAccessPoint MyPassPhrase
   berate_ap --daemon wlan0 eth0 MyAccessPoint MyPassPhrase
   berate_ap --stop wlan0
   berate_ap --eap --eap-cert-subj '/O=Internet Widgits Pty Ltd/ST=Some-State/C=AU' wlan0 eth0 MyAccessPoint
   berate_ap --eap --eap-user-file /etc/hostapd/hostapd.eap_user wlan0 eth0 MyAccessPoint
   berate_ap --trifecta wlan0 eth0 MyAccessPoint MyPassPhrase
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
