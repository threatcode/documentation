---
Title: hb-honeypot
Homepage: https://packetstormsecurity.com/files/126068/Heartbleed-Honeypot-Script.html
Repository: https://gitlab.com/kalilinux/packages/hb-honeypot
Architectures: all
Version: 0.1.1-1kali4
Metapackages: kali-linux-everything kali-tools-identify 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hb-honeypot
 
  This Perl script listens on TCP port 443 and responds with completely bogus
  SSL heartbeat responses, unless it detects the start of a byte pattern similar
  to that used in Jared Stafford's (jspenguin@jspenguin.org) demo for
  CVE-2014-0160 'Heartbleed'. Run as root for the privileged port. Outputs IPs
  of suspected heartbleed scan to the console. Rickrolls scanner in the hex
  dump.
 
 **Installed size:** `13 KB`  
 **How to install:** `sudo apt install hb-honeypot`  
 
 {{< spoiler "Dependencies:" >}}
 * perl
 {{< /spoiler >}}
 
 ##### hb-honeypot
 
 
 
 - - -
 
 ##### hb_honeypot.pl
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
