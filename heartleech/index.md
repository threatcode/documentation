---
Title: heartleech
Homepage: https://github.com/robertdavidgraham/heartleech
Repository: https://gitlab.com/kalilinux/packages/heartleech
Architectures: any
Version: 0~git20140607.3ab1d60-0kali2
Metapackages: kali-linux-everything kali-tools-web kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### heartleech
 
  This is a typical "heartbleed" tool. It can scan for systems vulnerable
  to the bug, and then be used to download them. Some important features:
   
   * conclusive/inconclusive verdicts as to whether the target is vulnerable
   * bulk/fast download of heartbleed data into a large files for offline
     processing using many threads
   * automatic retrieval of private keys with no additional steps
   * some limited IDS evasion
   * STARTTLS support
   * IPv6 support
   * Tor/Socks5n proxy support
   * extensive connection diagnostic information
 
 **Installed size:** `976 KB`  
 **How to install:** `sudo apt install heartleech`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 {{< /spoiler >}}
 
 ##### heartleech
 
 Exploits OpenSSL heartbleed vulnerability
 
 ```
 root@kali:~# heartleech -h
 
 > heartleech ~ Scanner detecting systems vulnerable to the heartbleed OpenSSL bug
 
 /usr/share/windows-resources/heartleech/
 `-- heartleech.exe
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
