---
Title: mdk3
Homepage: https://aspj.aircrack-ng.org/index.html#mdk3
Repository: https://salsa.debian.org/pkg-security-team/mdk3
Architectures: linux-any
Version: 6.0-8
Metapackages: kali-linux-everything kali-linux-large kali-linux-nethunter kali-tools-802-11 kali-tools-wireless 
Icon: images/mdk3-logo.svg
PackagesInfo: |
 ### mdk3
 
  MDK is a proof-of-concept tool to exploit common
  IEEE 802.11 (Wi-Fi) protocol weaknesses.
  Features:
    * Bruteforce MAC Filters.
    * Bruteforce hidden SSIDs (some small SSID wordlists included).
    * Probe networks to check if they can hear you.
    * Intelligent Authentication-DoS to freeze APs (with success checks).
    * FakeAP - Beacon Flooding with channel hopping (can crash NetStumbler and
      some buggy drivers)
    * Disconnect everything (aka AMOK-MODE) with Deauthentication and
      Disassociation packets.
    * WPA TKIP Denial-of-Service.
    * WDS Confusion - Shuts down large scale multi-AP installations.
 
 **Installed size:** `172 KB`  
 **How to install:** `sudo apt install mdk3`  
 
 {{< spoiler "Dependencies:" >}}
 * aircrack-ng
 * libc6 
 {{< /spoiler >}}
 
 ##### mdk3
 
 Wireless attack tool for IEEE 802.11 networks
 
 ```
 root@kali:~# mdk3 --help
 
 MDK 3.0 v6 - "Yeah, well, whatever"
 by ASPj of k2wrlz, using the osdep library from aircrack-ng
 And with lots of help from the great aircrack-ng community:
 Antragon, moongray, Ace, Zero_Chaos, Hirte, thefkboss, ducttape,
 telek0miker, Le_Vert, sorbo, Andy Green, bahathir and Dawid Gajownik
 THANK YOU!
 
 MDK is a proof-of-concept tool to exploit common IEEE 802.11 protocol weaknesses.
 IMPORTANT: It is your responsibility to make sure you have permission from the
 network owner before running MDK against it.
 
 This code is licenced under the GPLv2
 
 MDK USAGE:
 mdk3 <interface> <test_mode> [test_options]
 
 Try mdk3 --fullhelp for all test options
 Try mdk3 --help <test_mode> for info about one test only
 
 TEST MODES:
 b   - Beacon Flood Mode
       Sends beacon frames to show fake APs at clients.
       This can sometimes crash network scanners and even drivers!
 a   - Authentication DoS mode
       Sends authentication frames to all APs found in range.
       Too much clients freeze or reset some APs.
 p   - Basic probing and ESSID Bruteforce mode
       Probes AP and check for answer, useful for checking if SSID has
       been correctly decloaked or if AP is in your adaptors sending range
       SSID Bruteforcing is also possible with this test mode.
 d   - Deauthentication / Disassociation Amok Mode
       Kicks everybody found from AP
 m   - Michael shutdown exploitation (TKIP)
       Cancels all traffic continuously
 x   - 802.1X tests
 w   - WIDS/WIPS Confusion
       Confuse/Abuse Intrusion Detection and Prevention Systems
 f   - MAC filter bruteforce mode
       This test uses a list of known client MAC Addresses and tries to
       authenticate them to the given AP while dynamically changing
       its response timeout for best performance. It currently works only
       on APs who deny an open authentication request properly
 g   - WPA Downgrade test
       deauthenticates Stations and APs sending WPA encrypted packets.
       With this test you can check if the sysadmin will try setting his
       network to WEP or disable encryption.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## mdk3 Usage Example

Use the wireless interface (`wlan0`) to run the Authentication DoS mode test (`a`):

```
root@kali:~# mdk3 wlan0 a

Trying to get a new target AP...
AP 9C:D3:6D:B8:FF:56 is responding!
Connecting Client: 00:00:00:00:00:00 to target AP: 9C:D3:6D:B8:FF:56
Connecting Client: 00:00:00:00:00:00 to target AP: 9C:D3:6D:B8:FF:56
AP 9C:D3:6D:B8:FF:56 seems to be INVULNERABLE!
Device is still responding with   500 clients connected!
Trying to get a new target AP...
AP E0:3F:49:6A:57:78 is responding!
Connecting Client: 00:00:00:00:00:00 to target AP: E0:3F:49:6A:57:78
AP E0:3F:49:6A:57:78 seems to be INVULNERABLE!
```
