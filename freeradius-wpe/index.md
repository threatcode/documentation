---
Title: freeradius-wpe
Homepage: https://www.freeradius.org/
Repository: https://gitlab.com/kalilinux/packages/freeradius-wpe
Architectures: any
Version: 3.2.3+dfsg3-0kali1
Metapackages: kali-linux-everything kali-tools-802-11 kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### freeradius-wpe
 
  This package is FreeRadius Wireless Pawn Edition.
  There are supported and tested EAP Types/Inner Authentication Methods (others
  may also work):
    * PEAP/PAP (OTP)
    * PEAP/MSCHAPv2
    * EAP-TTLS/PAP (includes OTPs)
    * EAP-TTLS/MSCHAPv1
    * EAP-TTLS/MSCHAPv2
    * EAP-MD5
 
 **Installed size:** `4.62 MB`  
 **How to install:** `sudo apt install freeradius-wpe`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcrypt1 
 * libct4 
 * libgdbm6 
 * libjson-c5 
 * libpam0g 
 * libpcap0.8 
 * libperl5.36 
 * libpython3.11 
 * libsqlite3-0 
 * libssl3 
 * libsystemd0
 * libtalloc2 
 * libwbclient0 
 * python3
 * ssl-cert
 {{< /spoiler >}}
 
 ##### freeradius-wpe
 
 
 ```
 root@kali:~# freeradius-wpe -h
 Usage: freeradius [options]
 Options:
   -C            Check configuration and exit.
   -f            Run as a foreground process, not a daemon.
   -h            Print this help message.
   -i <ipaddr>   Listen on ipaddr ONLY.
   -l <log_file> Logging output will be written to this file.
   -m            On SIGINT or SIGQUIT clean up all used memory instead of just exiting.
   -n <name>     Read raddb/name.conf instead of raddb/radiusd.conf.
   -p <port>     Listen on port ONLY.
   -P            Always write out PID, even with -f.
   -s            Do not spawn child processes to handle requests (same as -ft).
   -t            Disable threads.
   -v            Print server version information.
   -X            Turn on full debugging (similar to -tfxxl stdout).
   -x            Turn on additional debugging (-xx gives more debugging).
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
