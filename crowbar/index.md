---
Title: crowbar
Homepage: https://github.com/galkan/crowbar
Repository: https://gitlab.com/kalilinux/packages/crowbar
Architectures: all
Version: 4.2-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### crowbar
 
  This package contains Crowbar (formally known as Levye). It is a brute forcing
  tool that can be used during penetration tests. It was developed to brute force
  some protocols in a different manner according to other popular brute forcing
  tools. As an example, while most brute forcing tools use username and password
  for SSH brute force, Crowbar uses SSH key(s). This allows for any private keys
  that have been obtained during penetration tests, to be used to attack other
  SSH servers.
   
  Currently Crowbar supports:
     * OpenVPN (-b openvpn)
     * Remote Desktop Protocol (RDP) with NLA support (-b rdp)
     * SSH private key authentication (-b sshkey)
     * VNC key authentication (-b vpn)
 
 **Installed size:** `450 KB`  
 **How to install:** `sudo apt install crowbar`  
 
 {{< spoiler "Dependencies:" >}}
 * freerdp2-x11
 * openvpn
 * python3
 * python3-nmap
 * python3-paramiko
 * vncviewer
 {{< /spoiler >}}
 
 ##### crowbar
 
 
 ```
 root@kali:~# crowbar -h
 usage: Usage: use --help for further information
 
 Crowbar is a brute force tool which supports OpenVPN, Remote Desktop Protocol,
 SSH Private Keys and VNC Keys.
 
 positional arguments:
   options
 
 options:
   -h, --help            show this help message and exit
   -b {openvpn,rdp,sshkey,vnckey}, --brute {openvpn,rdp,sshkey,vnckey}
                         Target service
   -s SERVER, --server SERVER
                         Static target
   -S SERVER_FILE, --serverfile SERVER_FILE
                         Multiple targets stored in a file
   -u USERNAME [USERNAME ...], --username USERNAME [USERNAME ...]
                         Static name to login with
   -U USERNAME_FILE, --usernamefile USERNAME_FILE
                         Multiple names to login with, stored in a file
   -n THREAD, --number THREAD
                         Number of threads to be active at once
   -l FILE, --log FILE   Log file (only write attempts)
   -o FILE, --output FILE
                         Output file (write everything else)
   -c PASSWD, --passwd PASSWD
                         Static password to login with
   -C FILE, --passwdfile FILE
                         Multiple passwords to login with, stored in a file
   -t TIMEOUT, --timeout TIMEOUT
                         [SSH] How long to wait for each thread (seconds)
   -p PORT, --port PORT  Alter the port if the service is not using the default
                         value
   -k KEY_FILE, --keyfile KEY_FILE
                         [SSH/VNC] (Private) Key file or folder containing
                         multiple files
   -m CONFIG, --config CONFIG
                         [OpenVPN] Configuration file
   -d, --discover        Port scan before attacking open ports
   -v, --verbose         Enable verbose output (-vv for more)
   -D, --debug           Enable debug mode
   -q, --quiet           Only display successful logins
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## crowbar Usage Examples

Brute force the RDP service on a single host with a specified username and wordlist, using 1 thread.

```
root@kali:~# crowbar -b rdp -s 192.168.86.61/32 -u victim -C /root/words.txt -n 1
2017-10-10 14:59:55 START
2017-10-10 14:59:55 Crowbar v0.3.5-dev
2017-10-10 14:59:55 Trying 192.168.86.61:3389
2017-10-10 15:00:08 RDP-SUCCESS : 192.168.86.61:3389 - victim:s3cr3t
2017-10-10 15:00:08 STOP
```
