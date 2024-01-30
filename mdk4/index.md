---
Title: mdk4
Homepage: https://github.com/aircrack-ng/mdk4
Repository: https://salsa.debian.org/pkg-security-team/mdk4
Architectures: any
Version: 4.2-3
Metapackages: kali-linux-everything kali-tools-802-11 kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### mdk4
 
  This package contains a proof-of-concept tool to exploit common IEEE 802.11
  protocol weaknesses.
   
  MDK4 is a new version of MDK3. MDK4 is a Wi-Fi testing tool from E7mer of
  360PegasusTeam, ASPj of k2wrlz, it uses the osdep library from the aircrack-ng
  project to inject frames on several operating systems.
   
  IMPORTANT: It is your responsibility to make sure you have permission from the
  network owner before running MDK against it.
 
 **Installed size:** `232 KB`  
 **How to install:** `sudo apt install mdk4`  
 
 {{< spoiler "Dependencies:" >}}
 * aircrack-ng
 * libc6 
 * libnl-3-200 
 * libnl-genl-3-200 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### mdk4
 
 IEEE 802.11 PoC tool
 
 ```
 root@kali:~# mdk4 -h
 MDK4 4.2 - "Awesome! Supports Proof-of-concept of WiFi protocol implementation vulnerability testing"
 by E7mer, thanks to the author of MDK3 and aircrack-ng community.
 MDK4 is a proof-of-concept tool to exploit common IEEE 802.11 protocol weaknesses.
 IMPORTANT: It is your responsibility to make sure you have permission from the
 network owner before running MDK4 against it.
 
 This code is licenced under the GPLv3 or later
 
 MDK4 USAGE:
 mdk4 <interface> <attack_mode> [attack_options]
 mdk4 <interface in> <interface out> <attack_mode> [attack_options]
 
 Try mdk4 --fullhelp for all attack options
 Try mdk4 --help <attack_mode> for info about one attack only
 
 
 ###### This version supports IDS Evasion (Ghosting) ######
 # Just append  --ghost <period>,<max_rate>,<min_txpower> #
 # after your attack mode identifier to enable ghosting!  #
 # <period>      : How often (in ms) to switch rate/power #
 # <max_rate>    : Maximum Bitrate to use in MBit         #
 # <min_txpower> : Minimum TX power in dBm to use         #
 # NOTE: Does not fully work with every driver, YMMV...   #
 ##########################################################
 
 #### This version supports IDS Evasion  (Fragmenting) ####
 # Just append  --frag <min_frags>,<max_frags>,<percent>  #
 # after your attack mode identifier to fragment all      #
 # outgoing packets, possibly avoiding lots of IDS!       #
 # <min_frags> : Minimum fragments to split packets into  #
 # <max_frags> : Maximum amount of fragments to create    #
 # <percent>   : Percantage of packets to fragment        #
 # NOTE: May not fully work with every driver, YMMV...    #
 # HINT: Set max_frags to 0 to enable standard compliance #
 ##########################################################
 
 Loaded 10 attack modules
 
 ATTACK MODE b: Beacon Flooding
   Sends beacon frames to show fake APs at clients.
   This can sometimes crash network scanners and even drivers!
 ATTACK MODE a: Authentication Denial-Of-Service
   Sends authentication frames to all APs found in range.
   Too many clients can freeze or reset several APs.
 ATTACK MODE p: SSID Probing and Bruteforcing
   Probes APs and checks for answer, useful for checking if SSID has
   been correctly decloaked and if AP is in your sending range.
   Bruteforcing of hidden SSIDs with or without a wordlist is also available.
 ATTACK MODE d: Deauthentication and Disassociation
   Sends deauthentication and disassociation packets to stations
   based on data traffic to disconnect all clients from an AP.
 ATTACK MODE m: Michael Countermeasures Exploitation
   Sends random packets or re-injects duplicates on another QoS queue
   to provoke Michael Countermeasures on TKIP APs.
   AP will then shutdown for a whole minute, making this an effective DoS.
 ATTACK MODE e: EAPOL Start and Logoff Packet Injection
   Floods an AP with EAPOL Start frames to keep it busy with fake sessions
   and thus disables it to handle any legitimate clients.
   Or logs off clients by injecting fake EAPOL Logoff messages.
 ATTACK MODE s: Attacks for IEEE 802.11s mesh networks
   Various attacks on link management and routing in mesh networks.
   Flood neighbors and routes, create black holes and divert traffic!
 ATTACK MODE w: WIDS Confusion
   Confuse/Abuse Intrusion Detection and Prevention Systems by
   cross-connecting clients to multiple WDS nodes or fake rogue APs.
 ATTACK MODE f: Packet Fuzzer
   A simple packet fuzzer with multiple packet sources
   and a nice set of modifiers. Be careful!
 ATTACK MODE x: Proof-of-concept of WiFi protocol implementation vulnerability testing
   Proof-of-concept of WiFi protocol implementation vulnerability,
   to test whether the device has wifi vulnerabilities.
   It may cause the wifi connection to be disconnected or the target device to crash.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
