---
Title: pwnat
Homepage: http://samy.pl/pwnat/
Repository: https://gitlab.com/kalilinux/packages/pwnat
Architectures: any
Version: 0.3-beta+git20140908-0kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation 
Icon: images/pwnat-logo.svg
PackagesInfo: |
 ### pwnat
 
  pwnat, pronounced "poe-nat", is a tool that allows any
  number of clients behind NATs to communicate with a
  server behind a separate NAT with *no* port forwarding
  and *no* DMZ setup on any routers in order to directly
  communicate with each other. The server does not need
  to know anything about the clients trying to connect.
 
 **Installed size:** `62 KB`  
 **How to install:** `sudo apt install pwnat`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### pwnat
 
 
 ```
 root@kali:~# pwnat -h
 usage: pwnat <-s | -c> <args>
   -c    client mode (default)
         <args>: [local ip] <local port> <proxy host> [proxy port (def:2222)] <remote host> <remote port>
   -s    server mode
         <args>: [local ip] [proxy port (def:2222)] [[allowed host]:[allowed port] ...]
   -6    use IPv6
   -v    show debug output (up to 2)
   -h    show this help and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## pwnat Usage Example

On the server, run in server mode (`-s`) on port 8080 (`8080`.

On the client, run in client mode (`-c`) on local port 8000 (`8000`), connect to the server IP (`192.168.1.202`) on port 8080 (`8080`) and use it to connect to google.com on port 80 (`google.com 80`).

```
root@kali:~# pwnat -s 8080
Listening on UDP 0.0.0.0:8080
```

```
root@kali:~# pwnat -c 8000 192.168.1.202 8080 google.com 80
Listening on TCP 0.0.0.0:8000
New connection(1): tcp://127.0.0.1:41318 -> udp://192.168.1.202:8080
```
