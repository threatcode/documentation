---
Title: bed
Homepage: http://www.snake-basket.de
Repository: https://gitlab.com/kalilinux/packages/bed
Architectures: any
Version: 0.5-1kali7
Metapackages: kali-linux-everything kali-linux-large kali-tools-vulnerability 
Icon: images/bed-logo.svg
PackagesInfo: |
 ### bed
 
  BED is a program which is designed to check daemons
  for potential buffer overflows, format strings et. al.
 
 **Installed size:** `73 KB`  
 **How to install:** `sudo apt install bed`  
 
 {{< spoiler "Dependencies:" >}}
 * perl
 {{< /spoiler >}}
 
 ##### bed
 
 
 ```
 root@kali:~# bed -h
 
  BED 0.5 by mjm ( www.codito.de ) & eric ( www.snake-basket.de )
 
 
  Usage:
 
  bed -s <plugin> -t <target> -p <port> -o <timeout> [ depends on the plugin ]
 
  <plugin>   = FTP/SMTP/POP/HTTP/IRC/IMAP/PJL/LPD/FINGER/SOCKS4/SOCKS5
  <target>   = Host to check (default: localhost)
  <port>     = Port to connect to (default: standard port)
  <timeout>  = seconds to wait after each test (default: 2 seconds)
  use "bed -s <plugin>" to obtain the parameters you need for the plugin.
 
  Only -s is a mandatory switch.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## bed Usage Example

Use the HTTP plugin (`-s HTTP`) to fuzz the target server (`-t 192.168.1.15`):

```
root@kali:~# bed -s HTTP -t 192.168.1.15

 BED 0.5 by mjm ( www.codito.de ) & eric ( www.snake-basket.de )

 + Buffer overflow testing:
        testing: 1  HEAD XAXAX HTTP/1.0
```
