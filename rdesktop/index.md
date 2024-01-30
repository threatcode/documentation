---
Title: rdesktop
Homepage: https://www.rdesktop.org/
Repository: 
Architectures: any
Version: 1.9.0-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rdesktop
 
  rdesktop is an open source client for Windows NT/2000 Terminal Server and
  Windows Server 2003/2008. Capable of natively speaking its Remote Desktop
  Protocol (RDP) in order to present the user's Windows desktop. Unlike Citrix
  ICA, no server extensions are required.
 
 **Installed size:** `683 KB`  
 **How to install:** `sudo apt install rdesktop`  
 
 {{< spoiler "Dependencies:" >}}
 * libasound2 
 * libc6 
 * libgmp10
 * libgnutls30 
 * libgssapi-krb5-2 
 * libhogweed6
 * libnettle8
 * libpcsclite1 
 * libtasn1-6 
 * libx11-6
 * libxcursor1 
 * libxrandr2
 {{< /spoiler >}}
 
 ##### rdesktop
 
 Remote Desktop Protocol client
 
 ```
 root@kali:~# rdesktop --help
 rdesktop: invalid option -- '-'
 rdesktop: A Remote Desktop Protocol client.
 Version 1.9.0. Copyright (C) 1999-2016 Matthew Chapman et al.
 See http://www.rdesktop.org/ for more information.
 
 Usage: rdesktop [options] server[:port]
    -u: user name
    -d: domain
    -s: shell / seamless application to start remotely
    -c: working directory
    -p: password (- to prompt)
    -n: client hostname
    -k: keyboard layout on server (en-us, de, sv, etc.)
    -g: desktop geometry (WxH[@DPI][+X[+Y]])
    -i: enables smartcard authentication, password is used as pin
    -f: full-screen mode
    -b: force bitmap updates
    -L: local codepage
    -A: path to SeamlessRDP shell, this enables SeamlessRDP mode
    -V: tls version (1.0, 1.1, 1.2, defaults to negotiation)
    -B: use BackingStore of X-server (if available)
    -e: disable encryption (French TS)
    -E: disable encryption from client to server
    -m: do not send motion events
    -M: use local mouse cursor
    -C: use private colour map
    -D: hide window manager decorations
    -K: keep window manager key bindings
    -S: caption button size (single application mode)
    -T: window title
    -t: disable use of remote ctrl
    -N: enable numlock synchronization
    -X: embed into another window with a given id.
    -a: connection colour depth
    -z: enable rdp compression
    -x: RDP5 experience (m[odem 28.8], b[roadband], l[an] or hex nr.)
    -P: use persistent bitmap caching
    -r: enable specified device redirection (this flag can be repeated)
          '-r comport:COM1=/dev/ttyS0': enable serial redirection of /dev/ttyS0 to COM1
              or      COM1=/dev/ttyS0,COM2=/dev/ttyS1
          '-r disk:floppy=/mnt/floppy': enable redirection of /mnt/floppy to 'floppy' share
              or   'floppy=/mnt/floppy,cdrom=/mnt/cdrom'
          '-r clientname=<client name>': Set the client name displayed
              for redirected disks
          '-r lptport:LPT1=/dev/lp0': enable parallel redirection of /dev/lp0 to LPT1
              or      LPT1=/dev/lp0,LPT2=/dev/lp1
          '-r printer:mydeskjet': enable printer redirection
              or      mydeskjet="HP LaserJet IIIP" to enter server driver as well
          '-r sound:[local[:driver[:device]]|off|remote]': enable sound redirection
                      remote would leave sound on server
                      available drivers for 'local':
                      alsa:	ALSA output driver, default device: default
          '-r clipboard:[off|PRIMARYCLIPBOARD|CLIPBOARD]': enable clipboard
                       redirection.
                       'PRIMARYCLIPBOARD' looks at both PRIMARY and CLIPBOARD
                       when sending data to server.
                       'CLIPBOARD' looks at only CLIPBOARD.
          '-r scard[:"Scard Name"="Alias Name[;Vendor Name]"[,...]]
           example: -r scard:"eToken PRO 00 00"="AKS ifdh 0"
                    "eToken PRO 00 00" -> Device in GNU/Linux and UNIX environment
                    "AKS ifdh 0"       -> Device shown in Windows environment 
           example: -r scard:"eToken PRO 00 00"="AKS ifdh 0;AKS"
                    "eToken PRO 00 00" -> Device in GNU/Linux and UNIX environment
                    "AKS ifdh 0"       -> Device shown in Microsoft Windows environment 
                    "AKS"              -> Device vendor name                 
    -0: attach to console
    -4: use RDP version 4
    -5: use RDP version 5 (default)
    -o: name=value: Adds an additional option to rdesktop.
            sc-csp-name        Specifies the Crypto Service Provider name which
                               is used to authenticate the user by smartcard
            sc-container-name  Specifies the container name, this is usually the username
            sc-reader-name     Smartcard reader name to use
            sc-card-name       Specifies the card name of the smartcard to use
    -v: enable verbose logging
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
