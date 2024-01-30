---
Title: eaphammer
Homepage: https://github.com/s0lst1c3/eaphammer
Repository: https://gitlab.com/kalilinux/packages/eaphammer
Architectures: any
Version: 1.14.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### eaphammer
 
  This package contains a toolkit for performing targeted evil twin attacks
  against WPA2-Enterprise networks. It is designed to be used in full scope
  wireless assessments and red team engagements. As such, focus is placed on
  providing an easy-to-use interface that can be leveraged to execute powerful
  wireless attacks with minimal manual configuration. To illustrate just how
  fast this tool is, the Quick Start section provides an example of how to
  execute a credential stealing evil twin attack against a WPA/2-EAP network in
  just commands.
 
 **Installed size:** `11.37 MB`  
 **How to install:** `sudo apt install eaphammer`  
 
 {{< spoiler "Dependencies:" >}}
 * apache2
 * asleap
 * dnsmasq
 * hcxdumptool
 * hcxtools
 * iptables
 * libc6 
 * libnl-3-200 
 * libnl-genl-3-200 
 * python3
 * python3-bs4
 * python3-distutils
 * python3-flask-cors
 * python3-flask-socketio
 * python3-gevent
 * python3-jinja2
 * python3-lxml
 * python3-openssl
 * python3-pem
 * python3-pyquery
 * python3-pywebcopy
 * python3-scapy
 * python3-tqdm
 * responder
 * seclists
 {{< /spoiler >}}
 
 ##### eaphammer
 
 
 ```
 root@kali:~# eaphammer -h
 
                      .__                                         
   ____ _____  ______ |  |__ _____    _____   _____   ___________ 
 _/ __ \\__  \ \____ \|  |  \\__  \  /     \ /     \_/ __ \_  __ \
 \  ___/ / __ \|  |_> >   Y  \/ __ \|  Y Y  \  Y Y  \  ___/|  | \/
  \___  >____  /   __/|___|  (____  /__|_|  /__|_|  /\___  >__|   
      \/     \/|__|        \/     \/      \/      \/     \/       
 
 
                         Now with more fast travel than a next-gen Bethesda game. >:D
 
                              Version:  1.14.0
                             Codename:  Final Frontier
                               Author:  @s0lst1c3
                              Contact:  gabriel<<at>>transmitengage.com
 
     
 usage: eaphammer [-h] [--cert-wizard [{create,import,interactive,list,dh}] |
                  --list-templates | --create-template | --delete-template |
                  --bootstrap | --creds | --pmkid | --eap-spray |
                  --hostile-portal | --captive-portal-server-only |
                  --captive-portal] [--debug] [--lhost LHOST] [-i INTERFACE]
                  [-e ESSID] [-b BSSID] [-c CHANNEL] [--hw-mode HW_MODE]
                  [--cloaking {none,full,zeroes}]
                  [--auth {open,wpa-psk,wpa-eap,owe,owe-transition,owe-psk}]
                  [--pmf {disable,enable,require}] [--karma]
                  [--essid-stripping {\r,\n,\t,\x20}]
                  [--mac-whitelist MAC_WHITELIST]
                  [--mac-blacklist MAC_BLACKLIST]
                  [--ssid-whitelist SSID_WHITELIST]
                  [--ssid-blacklist SSID_BLACKLIST] [--loud] [--known-beacons]
                  [--known-ssids-file KNOWN_SSIDS_FILE]
                  [--known-ssids KNOWN_SSIDS [KNOWN_SSIDS ...]]
                  [--channel-width MGhz] [--wpa-passphrase WPA_PASSPHRASE]
                  [--capture-wpa-handshakes {yes,no}]
                  [--psk-capture-file PSK_CAPTURE_FILE]
                  [--auth-alg {shared,open,both}] [--wpa-version {1,2}]
                  [--transition-bssid OWE_TRANSITION_BSSID]
                  [--transition-ssid OWE_TRANSITION_SSID] [--autocrack]
                  [--negotiate {balanced,speed,weakest,gtc-downgrade,manual}]
                  [--remote-cracking-rig server:port] [--wordlist WORDLIST]
                  [--name NAME] [--description DESCRIPTION] [--author AUTHOR]
                  [--add-download-form] [--dl-form-message DL_FORM_MESSAGE]
                  [--lport LPORT] [--payload PAYLOAD]
                  [--portal-template PORTAL_USER_TEMPLATE] [--pivot]
                  [-I iface_n [iface_n ...]] [--user-list USER_LIST]
                  [--password PASSWORD]
 
 options:
   -h, --help            show this help message and exit
   --debug               Enable debug output.
 
 Modes:
   --cert-wizard [{create,import,interactive,list,dh}]
                         Use this flag to run in Cert Wizard mode. Use "--cert-
                         wizard create" to create a new certificate. Use "--
                         cert-wizard interactive" or simply "--cert-wizard" to
                         run Cert Wizard in interactive mode. Use "--cert-
                         wizard import" to import a set of certificates into
                         eaphammer's static configuration. Use "--cert-wizard
                         list" to list all previously imported certs, as well
                         as the active cert configuration. Use "--cert-wizard
                         dh" to manually regenerate eaphammer's dh parameters.
   --list-templates      List available templates for the captive portal
   --create-template     Create a template by cloaning a login page
   --delete-template     Delete a captive portal template.
   --bootstrap           Shorthand for "--cert-wizard create --self-signed"
   --creds, --brad       Harvest EAP creds using evil twin attack
   --pmkid               Perform clientless attack against PSK network using
                         ZerBea's hcxtools.
   --eap-spray           Check for password reuse by spraying a single password
                         across a series of usernames against target ESSID.
   --hostile-portal      Force clients to connect to hostile portal
   --captive-portal-server-only
                         Run the captive portal server as astandalone service.
   --captive-portal      Force clients to connect to a captive portal
 
 Access Point:
   --lhost LHOST         Your AP's IP address
   -i INTERFACE, --interface INTERFACE
                         The phy interface on which to create the AP
   -e ESSID, --essid ESSID
                         Specify access point ESSID
   -b BSSID, --bssid BSSID
                         Specify access point BSSID
   -c CHANNEL, --channel CHANNEL
                         Specify access point channel (default: 1).
   --hw-mode HW_MODE     Specify access point hardware mode (defaults: g for
                         2.4GHz channels, a for 5GHz channels).
   --cloaking {none,full,zeroes}
                         Send empty SSID in beacons and ignore probe request
                         frames that do not specify full SSID (i.e. require
                         stations to know SSID). Choices: [1. none - do not use
                         SSID cloaking. ] [2. full - Send empty string in
                         beacon and ignore probe requests for broadcast SSID ]
                         [3. zeroes - Replace all characters in SSID with ASCII
                         0 and ignore probe requests for broadcast SSID.]
   --auth {open,wpa-psk,wpa-eap,owe,owe-transition,owe-psk}
                         Specify authentication mechanism (hostile and captive
                         portal default: open )(creds default: wpa-eap).
   --pmf {disable,enable,require}
                         Enable, disaable, or require the use of Protected
                         Management Frames (PMF) (802.11w) (default: disable)
                         (OWE default: require).
   --karma, --mana       Enable karma.
   --essid-stripping {\r,\n,\t,\x20}
                         Enable ESSID Stripping adding \r.
   --mac-whitelist MAC_WHITELIST
                         Enable MAC address whitelisting and specify path to
                         whitelist file.
   --mac-blacklist MAC_BLACKLIST
                         Enable MAC address blacklisting and specify path to
                         blacklist file.
   --ssid-whitelist SSID_WHITELIST
                         Enable MAC address whitelisting and specify path to
                         whitelist file.
   --ssid-blacklist SSID_BLACKLIST
                         Enable MAC address blacklisting and specify path to
                         blacklist file.
 
 Karma Options:
   --loud, --singe       Enable loud karma mode.
   --known-beacons       Enable persistent known beacons attack.
   --known-ssids-file KNOWN_SSIDS_FILE
                         Specify the wordlist to use with the --known-beacons
                         features.
   --known-ssids KNOWN_SSIDS [KNOWN_SSIDS ...]
                         Specify known ssids via the CLI
 
 802.11n Options:
   Used when --hw-mode is set to "n"
 
   --channel-width MGhz  Set the channel width in MGHz (single 20 MGHz spatial
                         stream or two 20 MGHz spatial streams totalling 40
                         MGHz). (default: 20)
 
 WPA-PSK Options:
   Only applicable if --auth wpa-psk is used
 
   --wpa-passphrase WPA_PASSPHRASE
                         Set WPA Passphrase for AP.
 
 WPA Options:
   Only applicable if --auth wpa-psk or wpa-eap are used
 
   --capture-wpa-handshakes {yes,no}
                         Capture 4-way WPA handshakes (wpa-psk default: yes)
                         (wpa-eap and sae defaults: no)
   --psk-capture-file PSK_CAPTURE_FILE
                         Path to which to write WPA handshakefiles (default:
                         automatically generated from nonce and current
                         timestamp)
   --auth-alg {shared,open,both}
                         Authentication type (open or shared key). (default:
                         shared)
   --wpa-version {1,2}   Set WPA version. (default: 2)
 
 OWE Transition Mode Options:
   Only applicable if --auth owe-transition is used
 
   --transition-bssid OWE_TRANSITION_BSSID
                         Set BSSID for OPEN AP
   --transition-ssid OWE_TRANSITION_SSID
                         Set SSID for OPEN AP
 
 EAP Options:
   Only applicable if --auth wpa-eap is used
 
   --autocrack           Enable autocrack 'n add.
   --negotiate {balanced,speed,weakest,gtc-downgrade,manual}
                         Specify EAP negotiation approach.
   --wordlist WORDLIST   Specify the wordlist to use with the autocrack
                         feature.
 
 Autocrack Options:
   Only applicable if --auth wpa-eap --autocrack is used
 
   --remote-cracking-rig server:port
                         Use remote cracking rig for autocrack feature.
 
 Create / Delete Template Options:
   Only applicable if --create-template or --delete-template is used.
 
   --name NAME           Specify name of resulting portal template module
   --description DESCRIPTION
                         Specify description of resulting portal template
                         module
   --author AUTHOR       Specify author of resulting portal template module
   --add-download-form   Add a download form to your captive portal.
   --dl-form-message DL_FORM_MESSAGE
                         Specify download form text.
 
 Captive Portal Options:
   Only applicable if --captive-portal is used
 
   --lport LPORT         Port on which to run captive portal.
   --payload PAYLOAD     Specify payload name (defaults to payload.msi test
                         file)
   --portal-template PORTAL_USER_TEMPLATE
                         Specify template directory
 
 Hostile Portal Options:
   Only applicable if --hostile-portal is used
 
   --pivot               Runs responder without SMB server enabled.
 
 EAP Spray:
   -I iface_n [iface_n ...], --interface-pool iface_n [iface_n ...]
                         List of interfaces available for password spray
                         attack.
   --user-list USER_LIST
                         Like a wordlist, except contains usernames instead of
                         passwords. Each username should be placed on a
                         separate line.
   --password PASSWORD   Specify password to be sprayed across list of users.
 
 [!] Use -h or --help to display a list of basic options.
 [!] Use -hh or --advanced-help to display full list of extended options.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
