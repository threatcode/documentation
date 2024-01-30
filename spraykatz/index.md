---
Title: spraykatz
Homepage: https://github.com/aas-n/spraykatz
Repository: https://gitlab.com/kalilinux/packages/spraykatz
Architectures: all
Version: 0.9.9-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### spraykatz
 
  This package contains a tool without any pretention able to retrieve
  credentials on Windows machines and large Active Directory environments.
   
  It simply tries to procdump machines and parse dumps remotely in order to
  avoid detections by antivirus software as much as possible.
 
 **Installed size:** `780 KB`  
 **How to install:** `sudo apt install spraykatz`  
 
 {{< spoiler "Dependencies:" >}}
 * nmap
 * python3
 * python3-impacket
 * python3-lxml
 * python3-openssl
 * python3-pyasn1
 * python3-pycryptodome
 * python3-pypykatz
 * python3-wget
 {{< /spoiler >}}
 
 ##### spraykatz
 
 
 ```
 root@kali:~# spraykatz -h
 
 ███████╗██████╗ ██████╗  █████╗ ██╗   ██╗██╗  ██╗ █████╗ ████████╗███████╗
 ██╔════╝██╔══██╗██╔══██╗██╔══██╗╚██╗ ██╔╝██║ ██╔╝██╔══██╗╚══██╔══╝╚══███╔╝
 ███████╗██████╔╝██████╔╝███████║ ╚████╔╝ █████╔╝ ███████║   ██║     ███╔╝ 
 ╚════██║██╔═══╝ ██╔══██╗██╔══██║  ╚██╔╝  ██╔═██╗ ██╔══██║   ██║    ███╔╝  
 ███████║██║     ██║  ██║██║  ██║   ██║   ██║  ██╗██║  ██║   ██║   ███████╗
 ╚══════╝╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚══════╝v0.9.9
                                                                           
                     Written by @aas_s3curity                       
                                                                           
 usage: spraykatz.py [-h] -u USERNAME -p PASSWORD -t TARGETS [-d DOMAIN] [-r]
                     [-v {warning,info,debug}] [-w WAIT]
 
 A tool to spray love around the world!
 
 options:
   -h, --help            show this help message and exit
 
 Mandatory Arguments:
   -u USERNAME, --username USERNAME
                         User to spray with. He must have admin rights on
                         targeted systems in order to gain remote code
                         execution.
   -p PASSWORD, --password PASSWORD
                         User's password or NTLM hash in the LM:NT format.
   -t TARGETS, --targets TARGETS
                         IP addresses and/or IP address ranges. You can submit
                         them via a file of targets (one target per line), or
                         inline (separated by commas).
 
 Optional Arguments:
   -d DOMAIN, --domain DOMAIN
                         User's domain. If he is not member of a domain, simply
                         use "-d ." instead.
   -r, --remove          Only try to remove ProcDump and dumps left behind on
                         distant machines. Just in case.
   -v {warning,info,debug}, --verbosity {warning,info,debug}
                         Verbosity mode. Default is info.
   -w WAIT, --wait WAIT  How many seconds Spraykatz waits before exiting
                         gracefully. Default is 180 seconds.
 
 => Do not use this on production environments!
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
