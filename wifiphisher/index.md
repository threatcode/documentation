---
Title: wifiphisher
Homepage: https://github.com/sophron/wifiphisher
Repository: https://gitlab.com/kalilinux/packages/wifiphisher
Architectures: all
Version: 1.4+git20220707-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wifiphisher
 
  This package contains a security tool that mounts automated phishing attacks
  against Wi-Fi networks in order to obtain secret passphrases or other
  credentials. It is a social engineering attack that unlike other methods it
  does not include any brute forcing. It is an easy way for obtaining credentials
  from captive portals and third party login pages or WPA/WPA2 secret
  passphrases.
 
 **Installed size:** `7.91 MB`  
 **How to install:** `sudo apt install wifiphisher`  
 
 {{< spoiler "Dependencies:" >}}
 * cowpatty
 * dnsmasq-base
 * hostapd
 * iptables
 * net-tools
 * python3
 * python3-pbkdf2
 * python3-pyric 
 * python3-roguehostapd
 * python3-scapy
 * python3-tornado
 {{< /spoiler >}}
 
 ##### wifiphisher
 
 
 ```
 root@kali:~# wifiphisher -h
 usage: wifiphisher [-h] [-i INTERFACE] [-eI EXTENSIONSINTERFACE]
                    [-aI APINTERFACE] [-iI INTERNETINTERFACE]
                    [-pI PROTECTINTERFACE [PROTECTINTERFACE ...]]
                    [-mI MITMINTERFACE] [-iAM MAC_AP_INTERFACE]
                    [-iEM MAC_EXTENSIONS_INTERFACE] [-iNM] [-kN] [-nE] [-nD]
                    [-dC DEAUTH_CHANNELS [DEAUTH_CHANNELS ...]] [-e ESSID]
                    [-dE DEAUTH_ESSID] [-p PHISHINGSCENARIO] [-pK PRESHAREDKEY]
                    [-hC HANDSHAKE_CAPTURE] [-qS] [-lC] [-lE LURE10_EXPLOIT]
                    [--logging] [-dK] [-lP LOGPATH] [-cP CREDENTIAL_LOG_PATH]
                    [--payload-path PAYLOAD_PATH] [-cM] [-wP]
                    [-wAI WPSPBC_ASSOC_INTERFACE] [-kB] [-fH]
                    [-pPD PHISHING_PAGES_DIRECTORY]
                    [--dnsmasq-conf DNSMASQ_CONF] [-pE PHISHING_ESSID]
 
 options:
   -h, --help            show this help message and exit
   -i INTERFACE, --interface INTERFACE
                         Manually choose an interface that supports both AP and
                         monitor modes for spawning the rogue AP as well as
                         mounting additional Wi-Fi attacks from Extensions
                         (i.e. deauth). Example: -i wlan1
   -eI EXTENSIONSINTERFACE, --extensionsinterface EXTENSIONSINTERFACE
                         Manually choose an interface that supports monitor
                         mode for deauthenticating the victims. Example: -eI
                         wlan1
   -aI APINTERFACE, --apinterface APINTERFACE
                         Manually choose an interface that supports AP mode for
                         spawning the rogue AP. Example: -aI wlan0
   -iI INTERNETINTERFACE, --internetinterface INTERNETINTERFACE
                         Choose an interface that is connected on the
                         InternetExample: -iI ppp0
   -pI PROTECTINTERFACE [PROTECTINTERFACE ...], --protectinterface PROTECTINTERFACE [PROTECTINTERFACE ...]
                         Specify the interface(s) that will have their
                         connection protected (i.e. NetworkManager will be
                         prevented from controlling them). Example: -pI wlan1
                         wlan2
   -mI MITMINTERFACE, --mitminterface MITMINTERFACE
                         Choose an interface that is connected on the Internet
                         in order to perform a MITM attack. All other
                         interfaces will be protected.Example: -mI wlan1
   -iAM MAC_AP_INTERFACE, --mac-ap-interface MAC_AP_INTERFACE
                         Specify the MAC address of the AP interface
   -iEM MAC_EXTENSIONS_INTERFACE, --mac-extensions-interface MAC_EXTENSIONS_INTERFACE
                         Specify the MAC address of the extensions interface
   -iNM, --no-mac-randomization
                         Do not change any MAC address
   -kN, --keepnetworkmanager
                         Do not kill NetworkManager
   -nE, --noextensions   Do not load any extensions.
   -nD, --nodeauth       Skip the deauthentication phase.
   -dC DEAUTH_CHANNELS [DEAUTH_CHANNELS ...], --deauth-channels DEAUTH_CHANNELS [DEAUTH_CHANNELS ...]
                         Channels to deauth. Example: --deauth-channels 1,3,7
   -e ESSID, --essid ESSID
                         Enter the ESSID of the rogue Access Point. This option
                         will skip Access Point selection phase. Example:
                         --essid 'Free WiFi'
   -dE DEAUTH_ESSID, --deauth-essid DEAUTH_ESSID
                         Deauth all the BSSIDs in the WLAN with that ESSID.
   -p PHISHINGSCENARIO, --phishingscenario PHISHINGSCENARIO
                         Choose the phishing scenario to run.This option will
                         skip the scenario selection phase. Example: -p
                         firmware_upgrade
   -pK PRESHAREDKEY, --presharedkey PRESHAREDKEY
                         Add WPA/WPA2 protection on the rogue Access Point.
                         Example: -pK s3cr3tp4ssw0rd
   -hC HANDSHAKE_CAPTURE, --handshake-capture HANDSHAKE_CAPTURE
                         Capture of the WPA/WPA2 handshakes for verifying
                         passphrase. Requires cowpatty. Example : -hC
                         capture.pcap
   -qS, --quitonsuccess  Stop the script after successfully retrieving one pair
                         of credentials
   -lC, --lure10-capture
                         Capture the BSSIDs of the APs that are discovered
                         during AP selection phase. This option is part of
                         Lure10 attack.
   -lE LURE10_EXPLOIT, --lure10-exploit LURE10_EXPLOIT
                         Fool the Windows Location Service of nearby Windows
                         users to believe it is within an area that was
                         previously captured with --lure10-capture. Part of the
                         Lure10 attack.
   --logging             Log activity to file
   -dK, --disable-karma  Disables KARMA attack
   -lP LOGPATH, --logpath LOGPATH
                         Determine the full path of the logfile.
   -cP CREDENTIAL_LOG_PATH, --credential-log-path CREDENTIAL_LOG_PATH
                         Determine the full path of the file that will store
                         any captured credentials
   --payload-path PAYLOAD_PATH
                         Payload path for scenarios serving a payload
   -cM, --channel-monitor
                         Monitor if target access point changes the channel.
   -wP, --wps-pbc        Monitor if the button on a WPS-PBC Registrar is
                         pressed.
   -wAI WPSPBC_ASSOC_INTERFACE, --wpspbc-assoc-interface WPSPBC_ASSOC_INTERFACE
                         The WLAN interface used for associating to the WPS
                         AccessPoint.
   -kB, --known-beacons  Broadcast a number of beacon frames advertising
                         popular WLANs
   -fH, --force-hostapd  Force the usage of hostapd installed in the system
   -pPD PHISHING_PAGES_DIRECTORY, --phishing-pages-directory PHISHING_PAGES_DIRECTORY
                         Search for phishing pages in this location
   --dnsmasq-conf DNSMASQ_CONF
                         Determine the full path of a custom dnmasq.conf file
   -pE PHISHING_ESSID, --phishing-essid PHISHING_ESSID
                         Determine the ESSID you want to use for the phishing
                         page
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/104286.js" id="asciicast-104286" async></script>

## wifiphisher Usage Examples

Do not perform jamming (`-nJ`), create a wireless access point (`-e “Free Wi-Fi”`) and present a fake firmware upgrade to clients (`-T firmware-upgrade`). When a client connects, they a presented with a webpage to enter the PSK of their network:

```
root@kali:~# wifiphisher -nJ -e "Free Wi-Fi" -T firmware-upgrade
[*] Starting Wifiphisher 1.1GIT at 2017-02-22 13:52
[+] Selecting wlan0 interface for creating the rogue Access Point
[*] Cleared leases, started DHCP, set up iptables
[+] Selecting Firmware Upgrade Page template
[*] Starting the fake access point...

Jamming devices:



DHCP Leases:
1487839973 c0:cc:f8:06:53:93 10.0.0.93 Victims-iPhone 11:c0:cc:38:66:a3:b3


HTTP requests:
[*] GET 10.0.0.93
[*] GET 10.0.0.93
[*] GET 10.0.0.93
[*] POST 10.0.0.93 wfphshr-wpa-password=s3cr3tp4s5
[*] GET 10.0.0.93
[*] GET 10.0.0.93
[*] GET 10.0.0.93
```
