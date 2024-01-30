---
Title: tnftp
Homepage: https://en.wikipedia.org/wiki/Tnftp
Repository: https://salsa.debian.org/debian/tnftp
Architectures: any all
Version: 20230507-2
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ftp
 
  This is a dummy transitional package transitioning ftp to tnftp.
 
 **Installed size:** `53 KB`  
 **How to install:** `sudo apt install ftp`  
 
 {{< spoiler "Dependencies:" >}}
 * tnftp
 {{< /spoiler >}}
 
 
 - - -
 
 ### tnftp
 
  tnftp is what many users affectionately call the enhanced ftp
  client in NetBSD (http://www.netbsd.org).
   
  This package is a `port' of the NetBSD ftp client to other systems.
   
  The enhancements over the standard ftp client in 4.4BSD include:
     * command-line editing within ftp
     * command-line fetching of URLS, including support for:
         - http proxies (c.f: $http_proxy, $ftp_proxy)
         - authentication
     * context sensitive command and filename completion
     * dynamic progress bar
     * IPv6 support (from the WIDE project)
     * modification time preservation
     * paging of local and remote files, and of directory listings
       (c.f: `lpage', `page', `pdir')
     * passive mode support, with fallback to active mode
     * `set option' override of ftp environment variables
     * TIS Firewall Toolkit gate ftp proxy support (c.f: `gate')
     * transfer-rate throttling (c.f: `-T', `rate')
 
 **Installed size:** `254 KB`  
 **How to install:** `sudo apt install tnftp`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libedit2 
 * libssl3 
 {{< /spoiler >}}
 
 ##### tnftp
 
 Internet file transfer program
 
 ```
 root@kali:~# tnftp -h
 tnftp: -h: unknown option
 usage: tnftp [-46AadefginpRtVv] [-N NETRC] [-o OUTPUT] [-P PORT] [-q QUITTIME]
            [-r RETRY] [-s SRCADDR] [-T DIR,MAX[,INC]] [-x XFERSIZE]
            [[USER@]HOST [PORT]]
            [[USER@]HOST:[PATH][/]]
            [file:///PATH]
            [ftp://[USER[:PASSWORD]@]HOST[:PORT]/PATH[/][;type=TYPE]]
            [http://[USER[:PASSWORD]@]HOST[:PORT]/PATH]
            [https://[USER[:PASSWORD]@]HOST[:PORT]/PATH]
            ...
        tnftp -u URL FILE ...
        tnftp -?
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
