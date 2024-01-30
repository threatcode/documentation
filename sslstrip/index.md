---
Title: sslstrip
Homepage: https://github.com/L1ghtn1ng/sslstrip
Repository: https://gitlab.com/kalilinux/packages/sslstrip
Architectures: all
Version: 1.0+git20211125.9ac747b-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sslstrip
 
  sslstrip is a tool that transparently hijacks HTTP traffic on a network, watch
  for HTTPS links and redirects, and then map those links into look-alike HTTP
  links or homograph-similar HTTPS links. It also supports modes for supplying a
  favicon which looks like a lock icon, selective logging, and session
  denial.
 
 **Installed size:** `60 KB`  
 **How to install:** `sudo apt install sslstrip`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-twisted
 {{< /spoiler >}}
 
 ##### sslstrip
 
 Manual page for sslstrip
 
 ```
 root@kali:~# sslstrip -h
 
 sslstrip 1.0 by Moxie Marlinspike
 Usage: sslstrip <options>
 
 Options:
 -w <filename>, --write=<filename> Specify file to log to (optional).
 -p , --post                       Log only SSL POSTs. (default)
 -s , --ssl                        Log all SSL traffic to and from server.
 -a , --all                        Log all SSL and HTTP traffic to and from server.
 -l <port>, --listen=<port>        Port to listen on (default 10000).
 -f , --favicon                    Substitute a lock favicon on secure requests.
 -k , --killsessions               Kill sessions in progress.
 -h                                Print this help message.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
