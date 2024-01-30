---
Title: sipsak
Homepage: https://github.com/nils-ohlmeier/sipsak
Repository: https://salsa.debian.org/pkg-voip-team/sipsak
Architectures: any
Version: 0.9.8.1-1
Metapackages: kali-linux-everything kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sipsak
 
  sipsak is a small command line tool for developers and administrators of
  Session Initiation Protocol (SIP) applications.
  It can be used for some simple tests on SIP applications and devices.
 
 **Installed size:** `131 KB`  
 **How to install:** `sudo apt install sipsak`  
 
 {{< spoiler "Dependencies:" >}}
 * libc-ares2 
 * libc6 
 * libgnutls30 
 {{< /spoiler >}}
 
 ##### sipsak
 
 A utility for various tests on sip servers and user agents
 
 ```
 root@kali:~# sipsak --help
 long option help
 sipsak 0.9.8.1 by Nils Ohlmeier
  Copyright (C) 2002-2004 FhG Fokus
  Copyright (C) 2004-2005 Nils Ohlmeier
  report bugs to github@ohlmeier.org
 
  shoot  : sipsak [-f FILE] [-L] -s SIPURI
  trace  : sipsak -T -s SIPURI
  usrloc : sipsak -U [-I|M] [-b NUMBER] [-e NUMBER] [-x NUMBER] [-z NUMBER] -s SIPURI
  usrloc : sipsak -I|M [-b NUMBER] [-e NUMBER] -s SIPURI
  usrloc : sipsak -U [-C SIPURI] [-x NUMBER] -s SIPURI
  message: sipsak -M [-B STRING] [-O STRING] [-c SIPURI] -s SIPURI
  flood  : sipsak -F [-e NUMBER] -s SIPURI
  random : sipsak -R [-t NUMBER] -s SIPURI
 
  additional parameter in every mode:
    [-a PASSWORD] [-d] [-i] [-H HOSTNAME] [-l PORT] [-m NUMBER] [-n] [-N]
    [-r PORT] [-v] [-V] [-w]
 
   --help                     displays this help message
   --version                  prints version string only
   --filename=FILE            the file which contains the SIP message to send
                                use - for standard input
   --no-crlf                  de-activate CR (\r) insertion
   --sip-uri=SIPURI           the destination server URI in form
                                sip:[user@]servername[:port]
   --traceroute               activates the traceroute mode
   --usrloc-mode              activates the usrloc mode
   --invite-mode              simulates a successful calls with itself
   --message-mode             sends messages to itself
   --contact=SIPURI           use the given URI as Contact in REGISTER
   --appendix-begin=NUMBER    the starting number appendix to the user name (default: 0)
   --appendix-end=NUMBER      the ending number of the appendix to the user name
   --sleep=NUMBER             sleep number ms before sending next request
   --expires=NUMBER           the expires header field value (default: 15)
   --remove-bindings=NUMBER   activates randomly removing of user bindings
   --flood-mode               activates the flood mode
   --random-mode              activates the random mode (dangerous)
   --trash-chars=NUMBER       the maximum number of trashed character in random mode
                                (default: request length)
   --local-port=PORT          the local port to use (default: any)
   --remote-port=PORT         the remote port to use (default: 5060)
   --outbound-proxy=HOSTNAME  request target (outbound proxy)
   --hostname=HOSTNAME        overwrites the local hostname in all headers
   --max-forwards=NUMBER      the value for the max-forwards header field
   --numeric                  use FQDN instead of IP in the Via-Line
   --processes=NUMBER         Divide the workflow among the number of processes
   --auth-username=STRING     username for authentication
   --no-via                   deactivate the insertion of a Via-Line
   --password=PASSWORD        password for authentication
                                (if omitted password=username)
   --ignore-redirects         ignore redirects
   --verbose                  each v produces more verbosity (max. 3)
   --extract-ip               extract IP from the warning in reply
   --replace-string=STRING    replacement for a special mark in the message
   --replace                  activates replacement of variables
   --nagios-code              returns exit codes Nagios compliant
   --nagios-warn=NUMBER       return Nagios warning if retrans > number
   --message-body=STRING      send a message with string as body
   --disposition=STRING       Content-Disposition value
   --search=REGEXP            search for a RegExp in replies and return error
                              on failure
   --timing=NUMBER            number of test runs and print just the timings
   --symmetric                send and received on the same port
   --from=SIPURI              use the given URI as From in MESSAGE
   --timeout-factor=NUMBER    timeout multiplier for INVITE transactions
                              on non-reliable transports (default: 64)
   --timer-t1=NUMBER          timeout T1 in ms (default: 500)
   --transport=STRING         specify transport to be used
   --headers=STRING           adds additional headers to the request
   --local-ip=STRING          specify local ip address to be used
   --authhash=STRING          HA1 hash for authentication instead of password
   --syslog=NUMBER            log exit message to syslog with given log level
   --tls-ca-cert=FILE         file with the cert of the root CA
   --tls-client-cert=FILE     file with the cert which sipsak will send
   --tls-ignore-cert-failure  ignore failures during the TLS handshake
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
