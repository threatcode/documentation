---
Title: atftp
Homepage: https://sourceforge.net/projects/atftp
Repository: https://salsa.debian.org/debian/atftp
Architectures: any
Version: 0.8.0-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### atftp
 
  Interactive client for the Trivial File Transfer Protocol (TFTP). Its
  usage is mainly for testing and debugging the atftp server. A TFTP client
  is usually implemented in UEFI/BIOS and bootstrap programs like pxelinux when
  booting from LAN. The atftp client also supports non-interactive invocation
  for easy use in scripts.
 
 **Installed size:** `96 KB`  
 **How to install:** `sudo apt install atftp`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libreadline8 
 {{< /spoiler >}}
 
 ##### atftp
 
 TFTP client (RFC1350).
 
 ```
 root@kali:~# atftp -h
 Usage: tftp [options] [host] [port]
  [options] may be:
   -g, --get                : get file
       --mget               : get file using mtftp
   -p, --put                : put file
   -l, --local-file <file>  : local file name
   -r, --remote-file <file> : remote file name
   -P, --password <password>: specify password (Linksys extension)
   --tftp-timeout <value>   : delay before retransmission, client side
   --option <"name value">  : set option name to value
   --mtftp <"name value">   : set mtftp variable to value
   --no-source-port-checking: violate RFC, see man page
   --prevent-sas            : prevent Sorcerer's Apprentice Syndrome
   --verbose                : set verbose mode on
   --trace                  : set trace mode on
   -V, --version            : print version information
   -h, --help               : print this help
 
  [host] is the tftp server name
  [port] is the port to use
 
 ```
 
 - - -
 
 ### atftpd
 
  Multi-threaded TFTP server implementing all options (option extension and
  multicast) as specified in RFC1350, RFC2090, RFC2347, RFC2348, RFC2349 and
  RFC7440. Atftpd also supports the multicast protocol known as mtftp, defined
  in the PXE specification. The server is socket activated by default but
  supports being started from inetd(8) as well as in daemon mode using init
  scripts.
 
 **Installed size:** `181 KB`  
 **How to install:** `sudo apt install atftpd`  
 
 {{< spoiler "Dependencies:" >}}
 * debconf  | debconf-2.0
 * init-system-helpers 
 * libc6 
 * libpcre2-8-0 
 * libwrap0 
 {{< /spoiler >}}
 
 ##### atftpd
 
 Trivial File Transfer Protocol Server.
 
 ```
 root@kali:~# atftpd -h
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
