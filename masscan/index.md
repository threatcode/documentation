---
Title: masscan
Homepage: https://github.com/robertdavidgraham/masscan
Repository: https://salsa.debian.org/pkg-security-team/masscan
Architectures: any
Version: 2:1.3.2+ds1-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: images/masscan-logo.svg
PackagesInfo: |
 ### masscan
 
  MASSCAN is TCP port scanner which transmits SYN packets
  asynchronously and produces results similar to nmap,
  the most famous port scanner. Internally, it operates
  more like scanrand, unicornscan, and ZMap, using
  asynchronous transmission.
  It's a flexible utility that allows arbitrary address and
  port ranges.
 
 **Installed size:** `553 KB`  
 **How to install:** `sudo apt install masscan`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### masscan
 
 Fast scan of the Internet
 
 ```
 root@kali:~# masscan --help
 MASSCAN is a fast port scanner. The primary input parameters are the
 IP addresses/ranges you want to scan, and the port numbers. An example
 is the following, which scans the 10.x.x.x network for web servers:
  masscan 10.0.0.0/8 -p80
 The program auto-detects network interface/adapter settings. If this
 fails, you'll have to set these manually. The following is an
 example of all the parameters that are needed:
  --adapter-ip 192.168.10.123
  --adapter-mac 00-11-22-33-44-55
  --router-mac 66-55-44-33-22-11
 Parameters can be set either via the command-line or config-file. The
 names are the same for both. Thus, the above adapter settings would
 appear as follows in a configuration file:
  adapter-ip = 192.168.10.123
  adapter-mac = 00-11-22-33-44-55
  router-mac = 66-55-44-33-22-11
 All single-dash parameters have a spelled out double-dash equivalent,
 so '-p80' is the same as '--ports 80' (or 'ports = 80' in config file).
 To use the config file, type:
  masscan -c <filename>
 To generate a config-file from the current settings, use the --echo
 option. This stops the program from actually running, and just echoes
 the current configuration instead. This is a useful way to generate
 your first config file, or see a list of parameters you didn't know
 about. I suggest you try it now:
  masscan -p1234 --echo
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/31820.js" id="asciicast-31820" async></script>

## masscan Usage Example

Scan for a selection of ports (`-p22,80,445`) across a given subnet (`192.168.1.0/24`):

```
root@kali:~# masscan -p22,80,445 192.168.1.0/24

Starting masscan 1.0.3 (http://bit.ly/14GZzcT) at 2014-05-13 21:35:12 GMT
 -- forced options: -sS -Pn -n --randomize-hosts -v --send-eth
Initiating SYN Stealth Scan
Scanning 256 hosts [3 ports/host]
Discovered open port 22/tcp on 192.168.1.217
Discovered open port 445/tcp on 192.168.1.220
Discovered open port 80/tcp on 192.168.1.230
```
