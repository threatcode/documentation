---
Title: vlan
Homepage: 
Repository: https://salsa.debian.org/debian/vlan
Architectures: all
Version: 2.0.5
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### vlan
 
  This package contains integration scripts for configuring vlan
  interfaces via ifupdown (/etc/network/interfaces).
  For further details see vlan-interfaces(5) man page in this package.
   
  Please note that these integration scripts only supports a limited
  set of interface naming schemes, which means you might be better
  off with writing your own ifupdown hooks using ip(route2)
  directly in /etc/network/interfaces rather than using this package.
   
  It currently also ships a wrapper script for backwards compatibility
  called vconfig, that replaces the old deprecated vconfig program
  with translations to ip(route2) commands.
  This compatibility shim might be dropped in future releases, please
  use ip(route2) commands directly.
   
  Your kernel needs vlan support for this to work, see "modinfo 8021q".
 
 **Installed size:** `41 KB`  
 **How to install:** `sudo apt install vlan`  
 
 {{< spoiler "Dependencies:" >}}
 * iproute2
 {{< /spoiler >}}
 
 ##### vconfig
 
 VLAN (802.1q) configuration program.
 
 ```
 root@kali:~# vconfig -h
 
 Usage: add             [interface-name] [vlan_id]
        rem             [vlan-name]
        set_flag        [interface-name] [flag-num]       [0 | 1]
        set_egress_map  [vlan-name]      [skb_priority]   [vlan_qos]
        set_ingress_map [vlan-name]      [skb_priority]   [vlan_qos]
        set_name_type   [name-type]
 
 * The [interface-name] is the name of the ethernet card that hosts
   the VLAN you are talking about.
 * The vlan_id is the identifier (0-4095) of the VLAN you are operating on.
 * skb_priority is the priority in the socket buffer (sk_buff).
 * vlan_qos is the 3 bit priority in the VLAN header
 * name-type:  VLAN_PLUS_VID (vlan0005), VLAN_PLUS_VID_NO_PAD (vlan5),
               DEV_PLUS_VID (eth0.0005), DEV_PLUS_VID_NO_PAD (eth0.5)
 * FLAGS:  1 REORDER_HDR  When this is set, the VLAN device will move the
             ethernet header around to make it look exactly like a real
             ethernet device.  This may help programs such as DHCPd which
             read the raw ethernet packet and make assumptions about the
             location of bytes.  If you don't need it, don't turn it on, because
             there will be at least a small performance degradation.  Default
             is OFF.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
