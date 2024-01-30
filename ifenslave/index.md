---
Title: ifenslave
Homepage: 
Repository: https://salsa.debian.org/debian/ifenslave
Architectures: all
Version: 2.13
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ifenslave
 
  This is a tool to attach and detach slave network interfaces to a bonding
  device. A bonding device will act like a normal Ethernet network device to
  the kernel, but will send out the packets via the slave devices using a simple
  round-robin scheduler. This allows for simple load-balancing, identical to
  "channel bonding" or "trunking" techniques used in switches.
   
  The kernel must have support for bonding devices for ifenslave to be useful.
 
 **Installed size:** `45 KB`  
 **How to install:** `sudo apt install ifenslave`  
 
 {{< spoiler "Dependencies:" >}}
 * ifupdown
 * iproute2
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
