---
Title: hostsman
Homepage: https://github.com/qszhuan/hostsman
Repository: https://gitlab.com/kalilinux/packages/hostsman
Architectures: all
Version: 1.1.5-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hostsman
 
  cross-platform command line tool for adding, removing or listing mappings in
  hosts file.
 
 **Installed size:** `51 KB`  
 **How to install:** `sudo apt install hostsman`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-colorama
 * python3-mock
 * python3-nose
 * python3-pygments
 {{< /spoiler >}}
 
 ##### hostsman
 
 
 ```
 root@kali:~# hostsman -h
 usage: hostsman [-h] [-l | -c HOSTNAME [HOSTNAME ...] | -i HOSTNAME[:IP]
                 [HOSTNAME[:IP] ...] | -r HOSTNAME [HOSTNAME ...]]
 
 add, remove or list mappings in hosts file
 
 options:
   -h, --help            show this help message and exit
   -l, --list            Show the content of hosts file
   -c HOSTNAME [HOSTNAME ...], --check HOSTNAME [HOSTNAME ...]
                         Check if the host name existed in the host file
   -i HOSTNAME[:IP] [HOSTNAME[:IP] ...], --insert HOSTNAME[:IP] [HOSTNAME[:IP] ...]
                         Insert HOSTNAME[:IP] mappings
   -r HOSTNAME [HOSTNAME ...], --remove HOSTNAME [HOSTNAME ...]
                         Remove mapping for HOSTNAME from hosts file.
 
 hosts file location: /etc/hosts
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
