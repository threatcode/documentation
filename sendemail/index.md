---
Title: sendemail
Homepage: http://caspian.dotconf.net/menu/Software/SendEmail/
Repository: https://github.com/mogaal/sendemail
Architectures: all
Version: 1.56-5.2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sendemail
 
  SendEmail is a lightweight, completely command line based, SMTP email
  agent. It was designed to be used in bash scripts, Perl programs, and
  web sites, but it is also quite useful in many other contexts.
   
  SendEmail is written in Perl and is unique in that it
  requires no special modules. It has a straight forward interface,
  making it very easy to use.
 
 **Installed size:** `107 KB`  
 **How to install:** `sudo apt install sendemail`  
 
 {{< spoiler "Dependencies:" >}}
 * libio-socket-inet6-perl
 * perl
 {{< /spoiler >}}
 
 ##### sendEmail
 
 Lightweight, command line SMTP email client
 Lightweight, command line SMTP email client
 
 ```
 root@kali:~# sendEmail -h
 
 sendEmail-1.56 by Brandon Zehm <caspian@dotconf.net>
 
 Synopsis:  sendEmail -f ADDRESS [options]
 
   Required:
     -f ADDRESS                from (sender) email address
     * At least one recipient required via -t, -cc, or -bcc
     * Message body required via -m, STDIN, or -o message-file=FILE
 
   Common:
     -t ADDRESS [ADDR ...]     to email address(es)
     -u SUBJECT                message subject
     -m MESSAGE                message body
     -s SERVER[:PORT]          smtp mail relay, default is localhost:25
     -S [SENDMAIL_PATH]        use local sendmail utility (default: /usr/bin/sendmail) instead of network MTA
 
   Optional:
     -a   FILE [FILE ...]      file attachment(s)
     -cc  ADDRESS [ADDR ...]   cc  email address(es)
     -bcc ADDRESS [ADDR ...]   bcc email address(es)
     -xu  USERNAME             username for SMTP authentication
     -xp  PASSWORD             password for SMTP authentication
 
   Paranormal:
     -b BINDADDR[:PORT]        local host bind address
     -l LOGFILE                log to the specified file
     -v                        verbosity, use multiple times for greater effect
     -q                        be quiet (i.e. no STDOUT output)
     -o NAME=VALUE             advanced options, for details try: --help misc
         -o message-content-type=<auto|text|html>
         -o message-file=FILE         -o message-format=raw
         -o message-header=HEADER     -o message-charset=CHARSET
         -o reply-to=ADDRESS          -o timeout=SECONDS
         -o username=USERNAME         -o password=PASSWORD
         -o tls=<auto|yes|no>         -o fqdn=FQDN
 
 
   Help:
     --help                    the helpful overview you're reading now
     --help addressing         explain addressing and related options
     --help message            explain message body input and related options
     --help networking         explain -s, -b, etc
     --help output             explain logging and other output options
     --help misc               explain -o options, TLS, SMTP auth, and more
 
 ```
 
 - - -
 
 ##### sendemail
 
 Lightweight, command line SMTP email client
 Lightweight, command line SMTP email client
 
 ```
 root@kali:~# sendemail -h
 
 sendemail-1.56 by Brandon Zehm <caspian@dotconf.net>
 
 Synopsis:  sendemail -f ADDRESS [options]
 
   Required:
     -f ADDRESS                from (sender) email address
     * At least one recipient required via -t, -cc, or -bcc
     * Message body required via -m, STDIN, or -o message-file=FILE
 
   Common:
     -t ADDRESS [ADDR ...]     to email address(es)
     -u SUBJECT                message subject
     -m MESSAGE                message body
     -s SERVER[:PORT]          smtp mail relay, default is localhost:25
     -S [SENDMAIL_PATH]        use local sendmail utility (default: /usr/bin/sendmail) instead of network MTA
 
   Optional:
     -a   FILE [FILE ...]      file attachment(s)
     -cc  ADDRESS [ADDR ...]   cc  email address(es)
     -bcc ADDRESS [ADDR ...]   bcc email address(es)
     -xu  USERNAME             username for SMTP authentication
     -xp  PASSWORD             password for SMTP authentication
 
   Paranormal:
     -b BINDADDR[:PORT]        local host bind address
     -l LOGFILE                log to the specified file
     -v                        verbosity, use multiple times for greater effect
     -q                        be quiet (i.e. no STDOUT output)
     -o NAME=VALUE             advanced options, for details try: --help misc
         -o message-content-type=<auto|text|html>
         -o message-file=FILE         -o message-format=raw
         -o message-header=HEADER     -o message-charset=CHARSET
         -o reply-to=ADDRESS          -o timeout=SECONDS
         -o username=USERNAME         -o password=PASSWORD
         -o tls=<auto|yes|no>         -o fqdn=FQDN
 
 
   Help:
     --help                    the helpful overview you're reading now
     --help addressing         explain addressing and related options
     --help message            explain message body input and related options
     --help networking         explain -s, -b, etc
     --help output             explain logging and other output options
     --help misc               explain -o options, TLS, SMTP auth, and more
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
