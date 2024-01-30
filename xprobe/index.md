---
archived: "true"
Title: xprobe
Homepage: 
Repository: https://salsa.debian.org/pkg-security-team/xprobe
Architectures: any
Version: 0.3-5
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### xprobe
 
  Xprobe2 allows you to determine what operating system is running on a
  remote host. It sends several packets to a host and analyses the
  returned answers.
   
  Xprobe2's functionality is comparable to the OS fingerprinting feature
  in nmap (written by a different Fyodor):
   - Outputs its level of confidence about the OS on the remote host.
   - Remains usable even if intermediate systems (routers, firewalls) make
     slight modifications to the packets.
   - Can list the type of intermediate device (e.g. "Linux IP masquerading").
   - Modular architecture allows new fingerprinting tests and new OS
     signatures to be added.
 
 **Installed size:** `982 KB`  
 **How to install:** `sudo apt install xprobe`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libpcap0.8 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### xprobe2
 
 A Remote active operating system fingerprinting tool.
 
 ```
 root@kali:~# xprobe2 --help
 xprobe2: invalid option -- '-'
 usage: xprobe2 [options] target
 Options:
           -v                       Be verbose
           -r                       Show route to target(traceroute)
           -p <proto:portnum:state> Specify portnumber, protocol and state.
                                    Example: tcp:23:open, UDP:53:CLOSED
           -c <configfile>          Specify config file to use.
           -h                       Print this help.
           -o <fname>               Use logfile to log everything.
           -t <time_sec>            Set initial receive timeout or roundtrip time.
           -s <send_delay>          Set packsending delay (milseconds).
           -d <debuglv>             Specify debugging level.
           -D <modnum>              Disable module number <modnum>.
           -M <modnum>              Enable module number <modnum>.
           -L                       Display modules.
           -m <numofmatches>        Specify number of matches to print.
           -T <portspec>            Enable TCP portscan for specified port(s).
                                    Example: -T21-23,53,110
           -U <portspec>            Enable UDP portscan for specified port(s).
           -f                       force fixed round-trip time (-t opt).
           -F                       Generate signature (use -o to save to a file).
           -X                       Generate XML output and save it to logfile specified with -o.
           -B                       Options forces TCP handshake module to try to guess open TCP port
           -A                       Perform analysis of sample packets gathered during portscan in
                                    order to detect suspicious traffic (i.e. transparent proxies,
                                    firewalls/NIDSs resetting connections). Use with -T.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
