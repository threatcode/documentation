---
Title: macchanger
Homepage: https://github.com/alobbs/macchanger
Repository: 
Architectures: linux-any
Version: 1.7.0-5.4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-802-11 kali-tools-sniffing-spoofing kali-tools-wireless 
Icon: images/macchanger-logo.svg
PackagesInfo: |
 ### macchanger
 
  GNU MAC Changer is an utility that makes the maniputation of MAC addresses of
  network interfaces easier.  MAC addresses are unique identifiers on networks,
  they only need to be unique, they can be changed on most network hardware.
  MAC addresses have started to be abused by unscrupulous marketing firms,
  government agencies, and others to provide an easy way to track a computer
  across multiple networks.  By changing the MAC address regularly, this kind
  of tracking can be thwarted, or at least made a lot more difficult.
   
  Features:
   
    * set specific MAC address of a network interface
    * set the MAC randomly
    * set a MAC of another vendor
    * set another MAC of the same vendor
    * set a MAC of the same kind (eg: wireless card)
    * display a vendor MAC list (today, 6200 items) to choose from
 
 **Installed size:** `637 KB`  
 **How to install:** `sudo apt install macchanger`  
 
 {{< spoiler "Dependencies:" >}}
 * debconf  | debconf-2.0
 * dpkg  | install-info
 * libc6 
 {{< /spoiler >}}
 
 ##### macchanger
 
 MAC Changer
 
 ```
 root@kali:~# macchanger -h
 GNU MAC Changer
 Usage: macchanger [options] device
 
   -h,  --help                   Print this help
   -V,  --version                Print version and exit
   -s,  --show                   Print the MAC address and exit
   -e,  --ending                 Don't change the vendor bytes
   -a,  --another                Set random vendor MAC of the same kind
   -A                            Set random vendor MAC of any kind
   -p,  --permanent              Reset to original, permanent hardware MAC
   -r,  --random                 Set fully random MAC
   -l,  --list[=keyword]         Print known vendors
   -b,  --bia                    Pretend to be a burned-in-address
   -m,  --mac=XX:XX:XX:XX:XX:XX
        --mac XX:XX:XX:XX:XX:XX  Set the MAC XX:XX:XX:XX:XX:XX
 
 Report bugs to https://github.com/alobbs/macchanger/issues
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
