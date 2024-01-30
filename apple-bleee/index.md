---
Title: apple-bleee
Homepage: https://github.com/hexway/apple_bleee
Repository: https://gitlab.com/kalilinux/packages/apple-bleee
Architectures: all
Version: 0.1.5-0kali5
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### apple-bleee
 
  This package contains experimental scripts. They are PoCs that show what an
  attacker get from Apple devices if they sniff Bluetooth traffic.
  To use these scripts you will need a Bluetooth adapter for sending BLE
  messages and Wi-Fi card supporting active monitor mode with frame injection for
  communication using AWDL (AirDrop).
 
 **Installed size:** `23.54 MB`  
 **How to install:** `sudo apt install apple-bleee`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * python3
 * python3-bluez
 * python3-bs4
 * python3-ctypescrypto
 * python3-fleep
 * python3-libarchive-c
 * python3-netifaces
 * python3-pil
 * python3-prettytable
 * python3-pycryptodome
 * python3-requests
 {{< /spoiler >}}
 
 ##### apple-bleee
 
 
 ```
 root@kali:~# apple-bleee -h
 
 > apple-bleee ~ scripts to show what an attacker get from Apple devices
 
 /usr/share/apple-bleee
 |-- adv_airpods.py
 |-- adv_wifi.py
 |-- airdrop_leak.py
 |-- ble_read_state.py
 |-- hash2phone
 |-- npyscreen
 |-- opendrop2
 `-- utils
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
