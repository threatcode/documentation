---
Title: miredo
Homepage: http://www.remlab.net/miredo/
Repository: https://salsa.debian.org/debian/miredo
Architectures: any
Version: 1.2.6-7.1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation 
Icon: images/miredo-logo.svg
PackagesInfo: |
 ### miredo
 
  The Teredo IPv6 tunneling protocol encapsulates IPv6 packets into UDP/IPv4
  datagrams, to allow hosts behind NAT devices to access the IPv6 Internet.
   
  Miredo is a Teredo client (as per RFC 4380): it can provide IPv6
  connectivity to a dual-stack IPv6/IPv4 host even if it is located behind a
  NAT. It can also operate as a Teredo relay which forwards IPv6 packets
  between the IPv6 Internet and remote Teredo clients.
 
 **Installed size:** `389 KB`  
 **How to install:** `sudo apt install miredo`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * init-system-helpers 
 * iproute2
 * libc6 
 * libcap2 
 * libjudydebian1
 * lsb-base
 * udev | makedev
 {{< /spoiler >}}
 
 ##### miredo
 
 Teredo IPv6 tunneling for Unix
 
 ```
 root@kali:~# miredo -h
 Usage: miredo [OPTIONS] [SERVER_NAME]
 Creates a Teredo tunneling interface for encapsulation of IPv6 over UDP.
 
   -c, --config     specify an configuration file
   -f, --foreground run in the foreground
   -h, --help       display this help and exit
   -p, --pidfile    override the location of the PID file
   -u, --user       override the user to set UID to
   -V, --version    display program version and exit
 ```
 
 - - -
 
 ##### miredo-checkconf
 
 Miredo configuration file syntax checking tool
 
 ```
 root@kali:~# miredo-checkconf -h
 Usage: miredo-checkconf [CONF_FILE]
 ```
 
 - - -
 
 ##### teredo-mire
 
 Stateless Teredo IPv6 responder
 
 ```
 root@kali:~# teredo-mire -h
 Usage: teredo-mire
 ```
 
 - - -
 
 ### miredo-server
 
  The Teredo IPv6 tunneling protocol encapsulates IPv6 packets into UDP/IPv4
  datagrams, to allow hosts behind NAT devices to access the IPv6 Internet.
   
  Miredo-server provides a Teredo server. Teredo servers help Teredo clients
  determine their NAT configuration, maintain their NAT binding, and perform
  hole punching when transmitting IPv6 packets to other Teredo clients and/or
  Teredo relays.
 
 **Installed size:** `231 KB`  
 **How to install:** `sudo apt install miredo-server`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * init-system-helpers 
 * libc6 
 * libcap2 
 * lsb-base
 {{< /spoiler >}}
 
 ##### miredo-server
 
 Teredo server for Unix
 
 ```
 root@kali:~# miredo-server -h
 Usage: miredo-server [OPTIONS] [SERVER_NAME]
 Creates a Teredo tunneling interface for encapsulation of IPv6 over UDP.
 
   -c, --config     specify an configuration file
   -f, --foreground run in the foreground
   -h, --help       display this help and exit
   -p, --pidfile    override the location of the PID file
   -u, --user       override the user to set UID to
   -V, --version    display program version and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
