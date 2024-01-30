---
Title: wifi-honey
Homepage: https://www.digininja.org/projects/wifi_honey.php
Repository: https://gitlab.com/kalilinux/packages/wifi-honey
Architectures: all
Version: 1.0-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-802-11 kali-tools-sniffing-spoofing kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wifi-honey
 
  In the case of WPA/WPA2, by running airodump-ng along side
  this you also end up capturing the first two packets of
  the four way handshake and so can attempt to crack the key
  with either aircrack-ng or coWPAtty.
   
  What this script does is to automate the setup process, it
  creates five monitor mode interfaces, four are used as APs
  and the fifth is used for airodump-ng. To make things
  easier, rather than having five windows all this is done in
  a screen session which allows you to switch between screens
  to see what is going on. All sessions are labelled so you
  know which is which.
 
 **Installed size:** `16 KB`  
 **How to install:** `sudo apt install wifi-honey`  
 
 {{< spoiler "Dependencies:" >}}
 * aircrack-ng
 * screen
 {{< /spoiler >}}
 
 ##### wifi-honey
 
 
 ```
 root@kali:~# wifi-honey --help
 
 Found 2 processes that could cause trouble.
 Kill them using 'airmon-ng check kill' before putting
 the card in monitor mode, they will interfere by changing channels
 and sometimes putting the interface back in managed mode
 
     PID Name
     666 NetworkManager
  801920 dhclient
 
 Requested device "wlan0" does not exist.
 Run /usr/sbin/airmon-ng without any arguments to see available interfaces
 
 Found 2 processes that could cause trouble.
 Kill them using 'airmon-ng check kill' before putting
 the card in monitor mode, they will interfere by changing channels
 and sometimes putting the interface back in managed mode
 
     PID Name
     666 NetworkManager
  801920 dhclient
 
 Requested device "wlan0" does not exist.
 Run /usr/sbin/airmon-ng without any arguments to see available interfaces
 
 Found 2 processes that could cause trouble.
 Kill them using 'airmon-ng check kill' before putting
 the card in monitor mode, they will interfere by changing channels
 and sometimes putting the interface back in managed mode
 
     PID Name
     666 NetworkManager
  801920 dhclient
 
 Requested device "wlan0" does not exist.
 Run /usr/sbin/airmon-ng without any arguments to see available interfaces
 
 Found 2 processes that could cause trouble.
 Kill them using 'airmon-ng check kill' before putting
 the card in monitor mode, they will interfere by changing channels
 and sometimes putting the interface back in managed mode
 
     PID Name
     666 NetworkManager
  801920 dhclient
 
 Requested device "wlan0" does not exist.
 Run /usr/sbin/airmon-ng without any arguments to see available interfaces
 
 Found 2 processes that could cause trouble.
 Kill them using 'airmon-ng check kill' before putting
 the card in monitor mode, they will interfere by changing channels
 and sometimes putting the interface back in managed mode
 
     PID Name
     666 NetworkManager
  801920 dhclient
 
 Requested device "wlan0" does not exist.
 Run /usr/sbin/airmon-ng without any arguments to see available interfaces
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## wifi-honey Usage Example

Broadcast the given ESSID (`FreeWiFi`) on channel 6 (`6`) using the wireless interface (`wlan0`):

```
root@kali:~# wifi-honey FreeWiFi 6 wlan0
```
