---
Title: tftp-hpa
Homepage: http://git.kernel.org/cgit/network/tftp/tftp-hpa.git
Repository: https://salsa.debian.org/ron/tftp-hpa
Architectures: linux-any kfreebsd-any
Version: 5.2+20150808-1.4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tftp-hpa
 
  Trivial File Transfer Protocol (TFTP) is a file transfer protocol, mainly to
  serve boot images over the network to other machines (PXE).
   
  tftp-hpa is an enhanced version of the BSD TFTP client and server. It
  possesses a number of bugfixes and enhancements over the original.
   
  This package contains the client.
 
 **Installed size:** `59 KB`  
 **How to install:** `sudo apt install tftp-hpa`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### tftp
 
 IPv4 Trivial File Transfer Protocol client
 
 ```
 root@kali:~# tftp -h
 Usage: tftp [-4][-6][-v][-l][-m mode] [host [port]] [-c command]
 ```
 
 - - -
 
 ### tftp-hpa-dbg
 
  Trivial File Transfer Protocol (TFTP) is a file transfer protocol, mainly to
  serve boot images over the network to other machines (PXE).
   
  tftp-hpa is an enhanced version of the BSD TFTP client and server. It
  possesses a number of bugfixes and enhancements over the original.
   
  This package contains the debugging symbols for both the client and the server.
 
 **Installed size:** `113 KB`  
 **How to install:** `sudo apt install tftp-hpa-dbg`  
 
 {{< spoiler "Dependencies:" >}}
 * tftp-hpa 
 * tftpd-hpa 
 {{< /spoiler >}}
 
 
 - - -
 
 ### tftpd-hpa
 
  Trivial File Transfer Protocol (TFTP) is a file transfer protocol, mainly to
  serve boot images over the network to other machines (PXE).
   
  tftp-hpa is an enhanced version of the BSD TFTP client and server. It
  possesses a number of bugfixes and enhancements over the original.
   
  This package contains the server.
 
 **Installed size:** `114 KB`  
 **How to install:** `sudo apt install tftpd-hpa`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * debconf  | debconf-2.0
 * libc6 
 * libwrap0 
 {{< /spoiler >}}
 
 ##### in.tftpd
 
 Trivial File Transfer Protocol Server.
 
 ```
 root@kali:~# in.tftpd -h
 Usage: tftpd [options] [directory]
  [options] may be:
   -t, --tftpd-timeout <value>: number of second of inactivity before exiting
   -r, --retry-timeout <value>: time to wait a reply before retransmition
   -m, --maxthread <value>    : number of concurrent thread allowed
   -v, --verbose [value]      : increase or set the level of output messages
   --trace                    : log all sent and received packets
   --no-timeout               : disable 'timeout' from RFC2349
   --no-tsize                 : disable 'tsize' from RFC2349
   --no-blksize               : disable 'blksize' from RFC2348
   --no-windowsize            : disable 'windowsize' from RFC7440
   --no-multicast             : disable 'multicast' from RFC2090
   --logfile <file>           : logfile to log logs to ;-) (use - for stdout)
   --pidfile <file>           : write PID to this file
   --listen-local             : force listen on local network address
   --daemon                   : run atftpd standalone (no inetd)
   --no-fork                  : run as a daemon, don't fork
   --prevent-sas              : prevent Sorcerer's Apprentice Syndrome
   --user <user[.group]>      : default is nobody
   --group <group>            : default is nogroup
   --port <port>              : port on which atftp listen
   --bind-address <IP>        : local address atftpd listen to
   --mcast-ttl                : ttl to used for multicast
   --mcast-addr <address list>: list/range of IP address to use
   --mcast-port <port range>  : ports to use for multicast transfer
   --pcre <file>              : use this file for pattern replacement
   --pcre-test <file>         : just test pattern file, not starting server
   --mtftp <file>             : mtftp configuration file
   --mtftp-port <port>        : port mtftp will listen
   --no-source-port-checking  : violate RFC, see man page
   --mcast-switch-client      : switch client on first timeout, see man page
   -V, --version              : print version information
   -h, --help                 : print this help
 
  [directory] must be a world readable/writable directories.
  By default /tftpboot is assumed.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
