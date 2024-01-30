---
Title: darkstat
Homepage: https://unix4lyfe.org/darkstat/
Repository: 
Architectures: any
Version: 3.0.719-1.1
Metapackages: kali-linux-everything kali-linux-large kali-tools-sniffing-spoofing 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### darkstat
 
  It is a packet sniffer which runs as a background process and serves its
  statistics to a web browser:
   - input and output IP traffic by machines, ports and protocols,
   - last minute, hourly, daily and monthly global input and output graphics.
   
  It is known to be smaller (in terms of memory footprint) and stabler than ntop.
 
 **Installed size:** `171 KB`  
 **How to install:** `sudo apt install darkstat`  
 
 {{< spoiler "Dependencies:" >}}
 * debconf  | debconf-2.0
 * libc6 
 * libpcap0.8 
 * lsb-base 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### darkstat
 
 Network statistics gatherer
 
 ```
 root@kali:~# darkstat --help
 darkstat 3.0.719 (using libpcap version 1.10.4 (with TPACKET_V3))
 
 usage: darkstat [ -i interface ]
                 [ -f filter ]
                 [ -r capfile ]
                 [ -p port ]
                 [ -b bindaddr ]
                 [ -l network/netmask ]
                 [ --base path ]
                 [ --local-only ]
                 [ --snaplen bytes ]
                 [ --pppoe ]
                 [ --syslog ]
                 [ --verbose ]
                 [ --no-daemon ]
                 [ --no-promisc ]
                 [ --no-dns ]
                 [ --no-macs ]
                 [ --no-lastseen ]
                 [ --chroot dir ]
                 [ --user username ]
                 [ --daylog filename ]
                 [ --import filename ]
                 [ --export filename ]
                 [ --pidfile filename ]
                 [ --hosts-max count ]
                 [ --hosts-keep count ]
                 [ --ports-max count ]
                 [ --ports-keep count ]
                 [ --highest-port port ]
                 [ --wait secs ]
                 [ --hexdump ]
                 [ --version ]
                 [ --help ]
 
 Please refer to the darkstat(8) manual page for further
 documentation and usage examples.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
