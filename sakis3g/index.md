---
Title: sakis3g
Homepage: http://www.sakis3g.org
Repository: https://gitlab.com/kalilinux/packages/sakis3g
Architectures: any
Version: 0.2.0e+git20150717-0kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sakis3g
 
  Sakis3G is a tweaked shell script which is supposed to work
  out-of-the-box for establishing a 3G connection with any
  combination of modem or operator. It automagically setups
  your USB or Bluetooth™ modem, and may even detect operator
  settings. You should try it when anything else fails.
 
 **Installed size:** `537 KB`  
 **How to install:** `sudo apt install sakis3g`  
 
 {{< spoiler "Dependencies:" >}}
 * bzip2
 * libusb-1.0-0
 {{< /spoiler >}}
 
 ##### sakis3g
 
 
 ```
 root@kali:~# sakis3g --help
 Sakis 3G All-in-one script - Version 0.2.0e
 (c) Sakis Dimopoulos 2009, 2010 under GNU GPL v2
 
 
 Usage:
       sakis3g [actors] [switches] [variables]
 
 Sakis3G is a shell script which is supposed to work out-of-the-box for 
 establishing a 3G connection with any combination of modem or operator. 
 
 NOTE: This script requires root priviledges to properly work. If not executed 
 from root, it will try to acquire them.
 
 Common actors are:
 connect       - Attempts to establish 3G connection.
 disconnect    - Stops all active PPP connections.
 toggle        - Attempts to establish 3G connection. If already connected, it 
 disconnects instead.
 reconnect     - Attempts to establish 3G connection. If already connected, it 
 first disconnects and then attempts.
 start         - Same as connect. Provided for use as init.d script.
 stop          - Same as disconnect. Provided for use as init.d script.
 reload        - Same as reconnect. Provided for use as init.d script.
 force-reload  - Same as reload. Provided for use as init.d script.
 restart       - Same as reload. Provided for use as init.d script.
 desktop       - Creates desktop shortcut for this script.
 status        - Prints connection status and exits. Exit code is 0 if 
 connected, or 6 if not connected.
 help          - Prints this screen and exits.
 man           - Displays man page.
 
 NOTE: For more information, you should consult man page or official Sakis3G 
 wiki, available at:
   http://wiki.sakis3g.org/
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## sakis3g Usage Example

```
root@kali:~# sakis3g --interactive "connect"
```
