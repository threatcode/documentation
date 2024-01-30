---
Title: udptunnel
Homepage: http://www1.cs.columbia.edu/~lennox/udptunnel/
Repository: https://salsa.debian.org/debian/udptunnel
Architectures: any
Version: 1.1-10
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation 
Icon: images/udptunnel-logo.svg
PackagesInfo: |
 ### udptunnel
 
  UDPTunnel is a small program which can tunnel UDP packets bi-directionally
  over a TCP connection. Its primary purpose (and original motivation) is to
  allow multi-media conferences to traverse a firewall which allows only
  outgoing TCP connections. UDPTunnel also can be used for security tests in
  networks.
 
 **Installed size:** `36 KB`  
 **How to install:** `sudo apt install udptunnel`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnsl2 
 {{< /spoiler >}}
 
 ##### udptunnel
 
 Tunnel UDP packets over a TCP connection
 
 ```
 root@kali:~# udptunnel --help
 udptunnel: invalid option -- '-'
 Usage: udptunnel -s TCP-port [-r] [-v] UDP-addr/UDP-port[/ttl]
     or udptunnel -c TCP-addr[/TCP-port] [-r] [-v] UDP-addr/UDP-port[/ttl]
      -s: Server mode.  Wait for TCP connections on the port.
      -c: Client mode.  Connect to the given address.
      -r: RTP mode.  Connect/listen on ports N and N+1 for both UDP and TCP.
          Port numbers must be even.
      -v: Verbose mode.  Specify -v multiple times for increased verbosity.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
