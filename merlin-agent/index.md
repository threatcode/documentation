---
Title: merlin-agent
Homepage: https://github.com/Ne0nd0g/merlin-agent
Repository: https://gitlab.com/kalilinux/packages/merlin-agent
Architectures: any
Version: 1.6.5-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### merlin-agent
 
  This package contains the Agent code for Merlin post-exploitation command and
  control framework.
 
 **Installed size:** `9.07 MB`  
 **How to install:** `sudo apt install merlin-agent`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### merlin-agent
 
 
 ```
 root@kali:~# merlin-agent -h
   -debug
     	Enable debug output
   -headers string
     	A new line separated (e.g., \n) list of additional HTTP headers to use
   -host string
     	HTTP Host header
   -ja3 string
     	JA3 signature string (not the MD5 hash). Overrides -proto & -parrot flags
   -killdate string
     	The date, as a Unix EPOCH timestamp, that the agent will quit running (default "0")
   -maxretry string
     	The maximum amount of failed checkins before the agent will quit running (default "7")
   -padding string
     	The maximum amount of data that will be randomly selected and appended to every message (default "4096")
   -parrot string
     	parrot or mimic a specific browser from github.com/refraction-networking/utls (e.g., HelloChrome_Auto
   -proto string
     	Protocol for the agent to connect with [https (HTTP/1.1), http (HTTP/1.1 Clear-Text), h2 (HTTP/2), h2c (HTTP/2 Clear-Text), http3 (QUIC or HTTP/3.0)] (default "h2")
   -proxy string
     	Hardcoded proxy to use for http/1.1 traffic only that will override host configuration
   -psk string
     	Pre-Shared Key used to encrypt initial communications (default "merlin")
   -skew string
     	Amount of skew, or variance, between agent checkins (default "3000")
   -sleep string
     	Time for agent to sleep (default "30s")
   -url string
     	Full URL for agent to connect to (default "https://127.0.0.1:443")
   -useragent string
     	The HTTP User-Agent header string that the Agent will use while sending traffic (default "Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/40.0.2214.85 Safari/537.36")
   -v	Enable verbose output
   -version
     	Print the agent version and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
