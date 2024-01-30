---
Title: sslh
Homepage: http://www.rutschle.net/tech/sslh/README.html
Repository: https://salsa.debian.org/debian/sslh.git
Architectures: any
Version: 1.22c-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-post-exploitation kali-tools-web 
Icon: images/sslh-logo.svg
PackagesInfo: |
 ### sslh
 
  sslh lets one accept HTTPS, SSH, OpenVPN, tinc and XMPP connections on the
  same port. This makes it possible to connect to any of these servers on
  port 443 (e.g. from inside a corporate firewall, which almost never block
  port 443) while still serving HTTPS on that port.
 
 **Installed size:** `321 KB`  
 **How to install:** `sudo apt install sslh`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * debconf 
 * init-system-helpers 
 * libc6 
 * libcap2 
 * libconfig9
 * libpcre2-8-0 
 * libwrap0 
 * update-inetd
 {{< /spoiler >}}
 
 ##### sslh
 
 Protocol demultiplexer
 
 ```
 root@kali:~# sslh -h
 sslhcfg: invalid option "-h"
  [-Vfin] [-F <file>] [-v <n>] [--transparent] [-t <n>] [-u <str>] [-P <file>] [-C <path>] [--syslog-facility=<str>] [--on-timeout=<str>] [--prefix=<str>] [-p <host:port>]... [--ssh=<host:port>]... [--tls=<host:port>]... [--openvpn=<host:port>]... [--tinc=<host:port>]... [--xmpp=<host:port>]... [--http=<host:port>]... [--adb=<host:port>]... [--socks5=<host:port>]... [--syslog=<host:port>]... [--anyprot=<host:port>]...
   -F, --config=<file>      	Specify configuration file
   -v, --verbose=<n>        	
   -V, --version            	Print version information and exit
   -f, --foreground         	Run in foreground instead of as a daemon
   -i, --inetd              	Run in inetd mode: use stdin/stdout instead of network listen
   -n, --numeric            	Print IP addresses and ports as numbers
   --transparent            	Set up as a transparent proxy
   -t, --timeout=<n>        	Set up timeout before connecting to default target
   -u, --user=<str>         	Username to change to after set-up
   -P, --pidfile=<file>     	Path to file to store PID of current instance
   -C, --chroot=<path>      	Root to change to after set-up
   --syslog-facility=<str>  	Facility to syslog to
   --on-timeout=<str>       	Target to connect to when timing out
   --prefix=<str>           	Reserved for testing
   -p, --listen=<host:port> 	Listen on host:port
   --ssh=<host:port>        	Set up ssh target
   --tls=<host:port>        	Set up TLS/SSL target
   --openvpn=<host:port>    	Set up OpenVPN target
   --tinc=<host:port>       	Set up tinc target
   --xmpp=<host:port>       	Set up XMPP target
   --http=<host:port>       	Set up HTTP (plain) target
   --adb=<host:port>        	Set up ADB (Android Debug) target
   --socks5=<host:port>     	Set up socks5 target
   --syslog=<host:port>     	Set up syslog target
   --anyprot=<host:port>    	Set up default target
 ```
 
 - - -
 
 ##### sslh-select
 
 Protocol demultiplexer
 
 ```
 root@kali:~# sslh-select -h
 sslhcfg: invalid option "-h"
  [-Vfin] [-F <file>] [-v <n>] [--transparent] [-t <n>] [-u <str>] [-P <file>] [-C <path>] [--syslog-facility=<str>] [--on-timeout=<str>] [--prefix=<str>] [-p <host:port>]... [--ssh=<host:port>]... [--tls=<host:port>]... [--openvpn=<host:port>]... [--tinc=<host:port>]... [--xmpp=<host:port>]... [--http=<host:port>]... [--adb=<host:port>]... [--socks5=<host:port>]... [--syslog=<host:port>]... [--anyprot=<host:port>]...
   -F, --config=<file>      	Specify configuration file
   -v, --verbose=<n>        	
   -V, --version            	Print version information and exit
   -f, --foreground         	Run in foreground instead of as a daemon
   -i, --inetd              	Run in inetd mode: use stdin/stdout instead of network listen
   -n, --numeric            	Print IP addresses and ports as numbers
   --transparent            	Set up as a transparent proxy
   -t, --timeout=<n>        	Set up timeout before connecting to default target
   -u, --user=<str>         	Username to change to after set-up
   -P, --pidfile=<file>     	Path to file to store PID of current instance
   -C, --chroot=<path>      	Root to change to after set-up
   --syslog-facility=<str>  	Facility to syslog to
   --on-timeout=<str>       	Target to connect to when timing out
   --prefix=<str>           	Reserved for testing
   -p, --listen=<host:port> 	Listen on host:port
   --ssh=<host:port>        	Set up ssh target
   --tls=<host:port>        	Set up TLS/SSL target
   --openvpn=<host:port>    	Set up OpenVPN target
   --tinc=<host:port>       	Set up tinc target
   --xmpp=<host:port>       	Set up XMPP target
   --http=<host:port>       	Set up HTTP (plain) target
   --adb=<host:port>        	Set up ADB (Android Debug) target
   --socks5=<host:port>     	Set up socks5 target
   --syslog=<host:port>     	Set up syslog target
   --anyprot=<host:port>    	Set up default target
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
