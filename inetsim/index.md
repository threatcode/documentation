---
Title: inetsim
Homepage: https://www.inetsim.org/index.html
Repository: https://salsa.debian.org/pkg-security-team/inetsim
Architectures: all
Version: 1.3.2+dfsg.1-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### inetsim
 
  INetSim is a software suite for simulating common internet services
  in a lab environment, e.g. for analyzing the network behaviour of
  unknown malware samples.
   
  INetSim supports simulation of the following services:
  HTTP, SMTP, POP3, DNS, FTP, NTP, TFTP, IRC, Ident, Finger, Syslog,
  'Small servers' (Daytime, Time, Echo, Chargen, Discard, Quotd)
   
  Additional features:
   * Faketime
   * Connection redirection
   * Detailed logging and reports
   * TLS/SSL support for several services
 
 **Installed size:** `1.08 MB`  
 **How to install:** `sudo apt install inetsim`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * init-system-helpers 
 * libdigest-sha-perl
 * libipc-shareable-perl
 * libnet-dns-perl 
 * libnet-server-perl
 * lsb-base
 * openssl
 * perl
 {{< /spoiler >}}
 
 ##### inetsim
 
 INetSim is a suite for simulating common internet services
 
 ```
 root@kali:~# inetsim --help
 INetSim 1.3.2 (2020-05-19) by Matthias Eckert & Thomas Hungenberg
 
 Usage: /usr/bin/inetsim [options]
 
 Available options:
   --help                         Print this help message.
   --version                      Show version information.
   --config=<filename>            Configuration file to use.
   --log-dir=<directory>          Directory logfiles are written to.
   --data-dir=<directory>         Directory containing service data.
   --report-dir=<directory>       Directory reports are written to.
   --bind-address=<IP address>    Default IP address to bind services to.
                                  Overrides configuration option 'default_bind_address'.
   --max-childs=<num>             Default maximum number of child processes per service.
                                  Overrides configuration option 'default_max_childs'.
   --user=<username>              Default user to run services.
                                  Overrides configuration option 'default_run_as_user'.
   --faketime-init-delta=<secs>   Initial faketime delta (seconds).
                                  Overrides configuration option 'faketime_init_delta'.
   --faketime-auto-delay=<secs>   Delay for auto incrementing faketime (seconds).
                                  Overrides configuration option 'faketime_auto_delay'.
   --faketime-auto-incr=<secs>    Delta for auto incrementing faketime (seconds).
                                  Overrides configuration option 'faketime_auto_increment'.
   --session=<id>                 Session id to use. Defaults to main process id.
   --pidfile=<filename>           Pid file to use. Defaults to '/var/run/inetsim.pid'.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
