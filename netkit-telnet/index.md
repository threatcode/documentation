---
archived: "true"
Title: netkit-telnet
Homepage: http://www.hcs.harvard.edu/~dholland/computers/netkit.html
Repository: https://salsa.debian.org/debian/netkit-telnet
Architectures: any
Version: 0.17-45
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### telnet
 
  The telnet command is used for interactive communication with another host
  using the TELNET protocol.
   
  For the purpose of remote login, the present client executable should be
  depreciated in favour of an ssh-client, or in some cases with variants like
  telnet-ssl or Kerberized TELNET clients.  The most important reason is that
  this implementation exchanges user name and password in clear text.
   
  On the other hand, the present program does satisfy common use cases of
  network diagnostics, like protocol testing of SMTP services, so it can
  become handy enough.
 
 **Installed size:** `166 KB`  
 **How to install:** `sudo apt install telnet`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libstdc++6 
 * netbase
 {{< /spoiler >}}
 
 ##### telnet.netkit
 
 User interface to the TELNET protocol
 
 ```
 root@kali:~# telnet.netkit -h
 telnet.netkit: invalid option -- 'h'
 Usage: telnet.netkit [-4] [-6] [-8] [-E] [-L] [-a] [-d] [-e char] [-l user]
 	[-n tracefile] [ -b addr ] [-r] [host-name [port]]
 ```
 
 - - -
 
 ### telnetd
 
  The in.telnetd program is a server which supports the DARPA telnet interactive
  communication protocol.
   
  This legacy server should in general be abandoned in favour of a contemporary
  ssh-server, as this implementation only is able to process password and user
  name in clear text.  Other variants, like telnetd-ssl and a selection of
  Kerberized TELNET servers, are able to improve on this by providing secure
  forms of authentication and encryption.
 
 **Installed size:** `115 KB`  
 **How to install:** `sudo apt install telnetd`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * openbsd-inetd | inet-superserver
 * passwd
 {{< /spoiler >}}
 
 ##### in.telnetd
 
 DARPA telnet protocol server
 
 ```
 root@kali:~# in.telnetd --help
 in.telnetd: invalid option -- '-'
 Usage: telnetd [-debug port] [-D (options|report|exercise|netdata|ptydata)]
 	 [-h] [-L login_program] [-n]
 ```
 
 - - -
 
 ##### in.telnetd
 
 DARPA telnet protocol server
 
 ```
 root@kali:~# in.telnetd --help
 in.telnetd: invalid option -- '-'
 Usage: telnetd [-debug port] [-D (options|report|exercise|netdata|ptydata)]
 	 [-h] [-L login_program] [-n]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
