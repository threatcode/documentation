---
Title: hak5-wifi-coconut
Homepage: https://hak5.org
Repository: https://gitlab.com/kalilinux/packages/hak5-wifi-coconut
Architectures: any
Version: 1.1.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hak5-wifi-coconut
 
  Userspace drive for USB Wi-Fi NICs and the Hak5 Wi-Fi Coconut
 
 **Installed size:** `176 KB`  
 **How to install:** `sudo apt install hak5-wifi-coconut`  
 
 {{< spoiler "Dependencies:" >}}
 * firmware-misc-nonfree
 * libc6 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 ##### wifi_coconut
 
 
 ```
 root@kali:~# wifi_coconut -h
 Wi-Fi Coconut
 Usage: wifi_coconut [options]
 By default, the wifi_coconut tool opens in interactive mode.
 Universal options:
  --disable-leds        Go fully dark; don't enable any LEDs
  --invert-leds         Normally a Wi-Fi Coconut enables all the LEDs
                        and blinks during traffic; Invert only lights
                        when there is traffic.
  --disable-blinking    Disable blinking the LEDs on traffic
 Non-interactive modes:
  --no-display          Don't display channel UI while logging
  --wait                Wait for a coconut to be found
  --pcap=[fname]        Log packets to a pcap file.  If file is '-',
                        a pcap file will be echoed to stdout so that it can
                        be piped to other tools. --wait-for-coconut    Wait for a coconut to be connected and identified
  --list-coconuts       List Wi-Fi Coconut devices and exit
  --coconut-device=X    If you have multiple Wi-Fi Coconuts, specify
                        which one to use
  --enable-partial      Enable a Wi-Fi Coconut even if not all the
                        radios have been identified.
  --plain-dot11         Log plain 802.11 packets instead of radiotap
                        formatted packets with signal and channel
  --quiet               Disable most output
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
