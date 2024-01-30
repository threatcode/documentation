---
Title: tlssled
Homepage: http://www.taddong.com/en/lab.html
Repository: https://gitlab.com/kalilinux/packages/tlssled
Architectures: all
Version: 1.3-0kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tlssled
 
  TLSSLed is a Linux shell script whose purpose is to evaluate
  the security of a target SSL/TLS (HTTPS) web server
  implementation. It is based on sslscan, a thorough SSL/TLS
  scanner that is based on the openssl library, and on the
  "openssl s_client" command line tool. The current tests
  include checking if the target supports the SSLv2 protocol,
  the NULL cipher, weak ciphers based on their key length (40
  or 56 bits), the availability of strong ciphers (like AES),
  if the digital certificate is MD5 signed, and the current
  SSL/TLS renegotiation capabilities.
 
 **Installed size:** `38 KB`  
 **How to install:** `sudo apt install tlssled`  
 
 {{< spoiler "Dependencies:" >}}
 * openssl
 * sslscan
 {{< /spoiler >}}
 
 ##### tlssled
 
 
 ```
 root@kali:~# tlssled -h
 ------------------------------------------------------
  TLSSLed - (1.3) based on sslscan and openssl
                  by Raul Siles (www.taddong.com)
 ------------------------------------------------------
     openssl version: OpenSSL 3.0.11 19 Sep 2023 (Library: OpenSSL 3.0.11 19 Sep 2023)
     
 ------------------------------------------------------
     Date: 20231201-104140
 ------------------------------------------------------
 
 [!] Usage: /usr/bin/tlssled <hostname or IP_address> <port>
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## TLSSLed Usage Example

Check SSL/TLS on the host (`192.168.1.1`) and port (`443`):

```
root@kali:~# tlssled 192.168.1.1 443
------------------------------------------------------
 TLSSLed - (1.3) based on sslscan and openssl
                 by Raul Siles (www.taddong.com)
------------------------------------------------------
    openssl version: OpenSSL 1.0.1e 11 Feb 2013
    sslscan version 1.8.2
------------------------------------------------------
    Date: 20140513-165131
------------------------------------------------------

[*] Analyzing SSL/TLS on 192.168.1.1:443 ...
    [.] Output directory: TLSSLed_1.3_192.168.1.1_443_20140513-165131 ...

[*] Checking if the target service speaks SSL/TLS...
    [.] The target service 192.168.1.1:443 seems to speak SSL/TLS...

    [.] Using SSL/TLS protocol version:
        (empty means I'm using the default openssl protocol version(s))

[*] Running sslscan on 192.168.1.1:443 ...

    [-] Testing for SSLv2 ...

    [-] Testing for the NULL cipher ...
```
