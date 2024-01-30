---
Title: whois
Homepage: 
Repository: https://github.com/rfc1036/whois
Architectures: any
Version: 5.5.20
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-identify 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### whois
 
  This package provides a commandline client for the WHOIS (RFC 3912)
  protocol, which queries online servers for information such as contact
  details for domains and IP address assignments.
  It can intelligently select the appropriate WHOIS server for most queries.
   
  The package also contains mkpasswd, a features-rich front end to the
  password encryption function crypt(3).
 
 **Installed size:** `387 KB`  
 **How to install:** `sudo apt install whois`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcrypt1 
 * libidn2-0 
 {{< /spoiler >}}
 
 ##### mkpasswd
 
 Overfeatured front end to crypt(3)
 
 ```
 root@kali:~# mkpasswd -h
 Usage: mkpasswd [OPTIONS]... [PASSWORD [SALT]]
 Crypts the PASSWORD using crypt(3).
 
       -m, --method=TYPE     select method TYPE
       -5                    like --method=md5crypt
       -S, --salt=SALT       use the specified SALT
       -R, --rounds=NUMBER   use the specified NUMBER of rounds
       -P, --password-fd=NUM read the password from file descriptor NUM
                             instead of /dev/tty
       -s, --stdin           like --password-fd=0
       -h, --help            display this help and exit
       -V, --version         output version information and exit
 
 If PASSWORD is missing then it is asked interactively.
 If no SALT is specified, a random one is generated.
 If TYPE is 'help', available methods are printed.
 
 Report bugs to <md+whois@linux.it>.
 ```
 
 - - -
 
 ##### whois
 
 Client for the whois directory service
 
 ```
 root@kali:~# whois --help
 Usage: whois [OPTION]... OBJECT...
 
 -h HOST, --host HOST   connect to server HOST
 -p PORT, --port PORT   connect to PORT
 -I                     query whois.iana.org and follow its referral
 -H                     hide legal disclaimers
       --verbose        explain what is being done
       --no-recursion   disable recursion from registry to registrar servers
       --help           display this help and exit
       --version        output version information and exit
 
 These flags are supported by whois.ripe.net and some RIPE-like servers:
 -l                     find the one level less specific match
 -L                     find all levels less specific matches
 -m                     find all one level more specific matches
 -M                     find all levels of more specific matches
 -c                     find the smallest match containing a mnt-irt attribute
 -x                     exact match
 -b                     return brief IP address ranges with abuse contact
 -B                     turn off object filtering (show email addresses)
 -G                     turn off grouping of associated objects
 -d                     return DNS reverse delegation objects too
 -i ATTR[,ATTR]...      do an inverse look-up for specified ATTRibutes
 -T TYPE[,TYPE]...      only look for objects of TYPE
 -K                     only primary keys are returned
 -r                     turn off recursive look-ups for contact information
 -R                     force to show local copy of the domain object even
                        if it contains referral
 -a                     also search all the mirrored databases
 -s SOURCE[,SOURCE]...  search the database mirrored from SOURCE
 -g SOURCE:FIRST-LAST   find updates from SOURCE from serial FIRST to LAST
 -t TYPE                request template for object of TYPE
 -v TYPE                request verbose template for object of TYPE
 -q [version|sources|types]  query specified server info
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
