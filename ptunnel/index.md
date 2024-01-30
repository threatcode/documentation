---
Title: ptunnel
Homepage: http://www.mit.edu/afs.new/sipb/user/golem/tmp/ptunnel-0.61.orig/web/
Repository: https://salsa.debian.org/alteholz/ptunnel
Architectures: any
Version: 0.72-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-post-exploitation 
Icon: images/ptunnel-logo.svg
PackagesInfo: |
 ### ptunnel
 
  ptunnel is an application that allows you to reliably tunnel TCP
  connections to a remote host using ICMP echo request and reply
  packets, commonly known as ping requests and replies. It acts as
  a proxy and can handle sockets and secured identification.
   
  Those features can be very handy when working in a closed networking
  environment with firewalls and proxies.
 
 **Installed size:** `123 KB`  
 **How to install:** `sudo apt install ptunnel`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 * libselinux1 
 * lsb-base 
 {{< /spoiler >}}
 
 ##### ptunnel
 
 Tunnel TCP connections over ICMP echo request/reply packets.
 
 ```
 root@kali:~# ptunnel -h
 ptunnel v 0.72.
 Usage:   ptunnel -p <addr> -lp <port> -da <dest_addr> -dp <dest_port> [-m max_tunnels] [-v verbosity] [-f logfile]
          ptunnel [-m max_threads] [-v verbosity] [-c <device>]
      -p: Set address of peer running packet forwarder. This causes
          ptunnel to operate in forwarding mode - the absence of this
          option causes ptunnel to operate in proxy mode.
     -lp: Set TCP listening port (only used when operating in forward mode)
     -da: Set remote proxy destination address if client
          Restrict to only this destination address if server
     -dp: Set remote proxy destionation port if client
          Restrict to only this destination port if server
      -m: Set maximum number of concurrent tunnels
      -v: Verbosity level (-1 to 4, where -1 is no output, and 4 is all output)
      -c: Enable libpcap on the given device.
      -f: Specify a file to log to, rather than printing to standard out.
      -s: Client only. Enables continuous output of statistics (packet loss, etc.)
 -daemon: Run in background, the PID will be written in the file supplied as argument
 -syslog: Output debug to syslog instead of standard out.
    -udp: Toggle use of UDP instead of ICMP. Proxy will listen on port 53 (must be root).
 
 Security features:  [-x password] [-u] [-setuid user] [-setgid group] [-chroot dir]
      -x: Set password (must be same on client and proxy)
      -u: Run proxy in unprivileged mode. This causes the proxy to forward
          packets using standard echo requests, instead of crafting custom echo replies.
          Unprivileged mode will only work on some systems, and is in general less reliable
          than running in privileged mode.
          Please consider combining the following three options instead:
 -setuid: When started in privileged mode, drop down to user's rights as soon as possible
 -setgid: When started in privileged mode, drop down to group's rights as soon as possible
 -chroot: When started in privileged mode, restrict file access to the specified directory
 -setcon: Set SELinux context when all there is left to do are network I/O operations
          To combine with -chroot you will have to `mount --bind /proc /chrootdir/proc`
 
 Starting the proxy (needs to run as root):
  [root #] ptunnel
 Starting a client (also needs root):
  [root #] ptunnel -p proxy.pingtunnel.com -lp 8000 -da login.domain.com -dp 22 -c eth0
 And then using the tunnel to ssh to login.domain.com:
  [user $] ssh -p 8000 localhost
 And that's it. Enjoy your tunnel!
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
