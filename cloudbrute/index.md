---
Title: cloudbrute
Homepage: https://github.com/0xsha/cloudbrute
Repository: https://gitlab.com/kalilinux/packages/cloudbrute
Architectures: any
Version: 1.0.7-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cloudbrute
 
  This package contains a tool to find a company (target) infrastructure, files,
  and apps on the top cloud providers (Amazon, Google, Microsoft, DigitalOcean,
  Alibaba, Vultr, Linode).
   
  The outcome is useful for bug bounty hunters, red teamers, and
  penetration testers alike. The complete writeup is available here
  (https://0xsha.io/posts/introducing-cloudbrute-wild-hunt-on-the-clouds)
  Features
   * Cloud detection (IPINFO API and Source Code)
   * Supports all major providers• Black-Box (unauthenticated)
   * Fast (concurrent)
   * Modular and easily customizable
   * Cross Platform (windows, Linux, mac)
   * User-Agent Randomization
   * Proxy Randomization (HTTP, Socks5)
   
  Supported Cloud Providers
   * Microsoft: - Storage - Apps
   * Amazon: - Storage - Apps
   * Google: - Storage - Apps
   * DigitalOcean: - storage
   * Vultr: - Storage
   * Linode: - Storage
   * Alibaba: - Storage
 
 **Installed size:** `6.15 MB`  
 **How to install:** `sudo apt install cloudbrute`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### cloudbrute
 
 
 ```
 root@kali:~# cloudbrute -h
 usage: CloudBrute [-h|--help] -d|--domain "<value>" -k|--keyword "<value>"
                   -w|--wordlist "<value>" [-c|--cloud "<value>"] [-t|--threads
                   <integer>] [-T|--timeout <integer>] [-p|--proxy "<value>"]
                   [-a|--randomagent "<value>"] [-D|--debug] [-q|--quite]
                   [-m|--mode "<value>"] [-o|--output "<value>"]
                   [-C|--configFolder "<value>"]
 
                   Awesome Cloud Enumerator
 
 Arguments:
 
   -h  --help          Print help information
   -d  --domain        domain
   -k  --keyword       keyword used to generator urls
   -w  --wordlist      path to wordlist
   -c  --cloud         force a search, check config.yaml providers list
   -t  --threads       number of threads. Default: 80
   -T  --timeout       timeout per request in seconds. Default: 10
   -p  --proxy         use proxy list
   -a  --randomagent   user agent randomization
   -D  --debug         show debug logs. Default: false
   -q  --quite         suppress all output. Default: false
   -m  --mode          storage or app. Default: storage
   -o  --output        Output file. Default: out.txt
   -C  --configFolder  Config path. Default: /etc/cloudbrute/config
 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
