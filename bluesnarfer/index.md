---
Title: bluesnarfer
Homepage: http://www.alighieri.org/
Repository: https://gitlab.com/kalilinux/packages/bluesnarfer
Architectures: any
Version: 0.1-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-bluetooth kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bluesnarfer
 
  A bluetooth bluesnarfing Utility
 
 **Installed size:** `30 KB`  
 **How to install:** `sudo apt install bluesnarfer`  
 
 {{< spoiler "Dependencies:" >}}
 * bluez
 * libbluetooth3 
 * libc6 
 {{< /spoiler >}}
 
 ##### bluesnarfer
 
 
 ```
 root@kali:~# bluesnarfer --help
 bluesnarfer: invalid option -- '-'
 bluesnarfer, version 0.1 -
 usage: bluesnarfer [options] [ATCMD] -b bt_addr
 
 ATCMD     : valid AT+CMD (GSM EXTENSION)
 
 TYPE      : valid phonebook type ..
 example   : "DC" (dialed call list)
             "SM" (SIM phonebook)
             "RC" (recevied call list)
             "XX" much more
 
 -b bdaddr : bluetooth device address
 -C chan   : bluetooth rfcomm channel
 
 -c ATCMD  : custom action
 -r N-M    : read phonebook entry N to M 
 -w N-M    : delete phonebook entry N to M
 -f name   : search "name" in phonebook address
 -s TYPE   : select phonebook memory storage
 -l        : list aviable phonebook memory storage
 -i        : device info
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}


bluesnarfer Usage Example

Scan the remote device address (`-b 20:C9:D0:43:4B:D8`) and get the device info (`-i`):

```
root@kali:~# bluesnarfer -b 20:C9:D0:43:4B:D8 -i
device name: ares
```
