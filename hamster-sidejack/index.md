---
Title: hamster-sidejack
Homepage: http://www.erratasec.com/research.html
Repository: https://gitlab.com/kalilinux/packages/hamster-sidejack
Architectures: any
Version: 2.0-1kali6
Metapackages: kali-linux-everything kali-linux-large kali-tools-sniffing-spoofing kali-tools-web 
Icon: images/hamster-sidejack-logo.svg
PackagesInfo: |
 ### hamster-sidejack
 
  Hamster is tool or "sidejacking". It acts as a proxy server that
  replaces your cookies with session cookies stolen from somebody
  else, allowing you to hijack their sessions.
   
  Cookies are sniffed using the Ferret program. You need a copy of
  that as well.
 
 **Installed size:** `154 KB`  
 **How to install:** `sudo apt install hamster-sidejack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### hamster-sidejack
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## hamster Usage Example

```
root@kali:~# hamster
--- HAMPSTER 2.0 side-jacking tool ---
Set browser to use proxy http://127.0.0.1:1234
DEBUG: set_ports_option(1234)
DEBUG: mg_open_listening_port(1234)
Proxy: listening on 127.0.0.1:1234
begining thread
```
