---
Title: cisco-ocs
Homepage: http://hacklab.altervista.org/
Repository: https://gitlab.com/kalilinux/packages/cisco-ocs
Architectures: any
Version: 0.2-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cisco-ocs
 
  A mass Cisco scanning tool.
 
 **Installed size:** `25 KB`  
 **How to install:** `sudo apt install cisco-ocs`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### cisco-ocs
 
 
 ```
 root@kali:~# cisco-ocs -h
 ********************************* OCS v 0.2 **********************************
 ****                                                                      ****
 ****                           coded by OverIP                            ****
 ****                           overip@gmail.com                           ****
 ****                           under GPL License                          ****
 ****                                                                      ****
 ****             usage: ./ocs xxx.xxx.xxx.xxx yyy.yyy.yyy.yyy             ****
 ****                                                                      ****
 ****                   xxx.xxx.xxx.xxx = range start IP                   ****
 ****                    yyy.yyy.yyy.yyy = range end IP                    ****
 ****                                                                      ****
 ******************************************************************************
 use: cisco-ocs IP IP
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## cisco-ocs Usage Example

Attempt to exploit Cisco devices in the given IP range (`192.168.99.200 192.168.99.202`):

```
root@kali:~# cisco-ocs 192.168.99.200 192.168.99.202
********************************* OCS v 0.2 **********************************
****                                                                      ****
****                           coded by OverIP                            ****
****                           overip@gmail.com                           ****
****                           under GPL License                          ****
****                                                                      ****
****             usage: ./ocs xxx.xxx.xxx.xxx yyy.yyy.yyy.yyy             ****
****                                                                      ****
****                   xxx.xxx.xxx.xxx = range start IP                   ****
****                    yyy.yyy.yyy.yyy = range end IP                    ****
****                                                                      ****
******************************************************************************


-192.168.99.200
  |Logging... 192.168.99.200
  |Router not vulnerable.


-192.168.99.201
  |Logging... 192.168.99.201
  |Router not vulnerable.


-192.168.99.202
  |Logging... 192.168.99.202
  |Router not vulnerable.
```
