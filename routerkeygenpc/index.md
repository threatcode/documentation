---
Title: routerkeygenpc
Homepage: https://github.com/routerkeygen/routerkeygenPC
Repository: https://gitlab.com/kalilinux/packages/routerkeygenpc
Architectures: any
Version: 1.1.0+git20190721.c1f1665-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### routerkeygenpc
 
  This package generates default WPA/WEP keys for the several routers:
   * Thomson based routers ( this includes Thomson, SpeedTouch, Orange,
     Infinitum, BBox, DMax, BigPond, O2Wireless, Otenet, Cyta , TN_private,
     Blink )
   * DLink ( only some models )
   * Pirelli Discus
   * Eircom
   * Verizon FiOS ( only some routers supported)
   * Alice AGPF
   * FASTWEB Pirelli and Telsey
   * Huawei (some InfinitumXXXX)
   * Wlan_XXXX or Jazztel_XXXX
   * Wlan_XX ( only some are supported)
   * Ono ( P1XXXXXX0000X )
   * WlanXXXXXX, YacomXXXXXX and WifiXXXXXX
   * Sky V1 routers
   * Clubinternet.box v1 and v2 ( TECOM-AH4XXXX )
   * InfostradaWifi
   * CONN-X
   * Megared
   * EasyBox, Arcor and Vodafone
   * PBS (Austria)
   * MAXCOM
   * PTV
   * TeleTu/Tele2
   * Axtel, Axtel-xtremo
   * Intercable
   * OTE
   * Cabovisao Sagem
   * Alice in Germany
   * Speedport
 
 **Installed size:** `5.63 MB`  
 **How to install:** `sudo apt install routerkeygenpc`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libqt5core5a 
 * libqt5dbus5 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5script5 
 * libqt5widgets5 
 * libssl3 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### routerkeygen
 
 
 
 - - -
 
 ##### routerkeygen-cli
 
 
 ```
 root@kali:~# routerkeygen-cli -h
 Usage:  [-h] [-s network_name] [-m mac_address] [-k] [-q]
 
 Optional arguments:
   -h, --help                            Show this help message and exit
   -s network_name, --ssid network_name  SSID
   -m mac_address, --mac mac_address     MAC address
   -k, --kg                              Print keygen in form kgname:candidate
   -q, --quiet                           Print only calculated keys
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
