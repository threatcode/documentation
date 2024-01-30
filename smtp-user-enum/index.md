---
Title: smtp-user-enum
Homepage: http://pentestmonkey.net/tools/user-enumeration/smtp-user-enum
Repository: https://gitlab.com/kalilinux/packages/smtp-user-enum
Architectures: all
Version: 1.2-1kali4
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### smtp-user-enum
 
  Username guessing tool primarily for use against the
  default Solaris SMTP service. Can use either EXPN, VRFY or
  RCPT TO.
 
 **Installed size:** `98 KB`  
 **How to install:** `sudo apt install smtp-user-enum`  
 
 {{< spoiler "Dependencies:" >}}
 * libio-socket-ip-perl
 * libsocket-perl
 * perl
 {{< /spoiler >}}
 
 ##### smtp-user-enum
 
 
 ```
 root@kali:~# smtp-user-enum -h
 smtp-user-enum v1.2 ( http://pentestmonkey.net/tools/smtp-user-enum )
 
 Usage: smtp-user-enum [options] ( -u username | -U file-of-usernames ) ( -t host | -T file-of-targets )
 
 options are:
         -m n     Maximum number of processes (default: 5)
 	-M mode  Method to use for username guessing EXPN, VRFY or RCPT (default: VRFY)
 	-u user  Check if user exists on remote system
 	-f addr  MAIL FROM email address.  Used only in "RCPT TO" mode (default: user@example.com)
         -D dom   Domain to append to supplied user list to make email addresses (Default: none)
                  Use this option when you want to guess valid email addresses instead of just usernames
                  e.g. "-D example.com" would guess foo@example.com, bar@example.com, etc.  Instead of 
                       simply the usernames foo and bar.
 	-U file  File of usernames to check via smtp service
 	-t host  Server host running smtp service
 	-T file  File of hostnames running the smtp service
 	-p port  TCP port on which smtp service runs (default: 25)
 	-d       Debugging output
 	-w n     Wait a maximum of n seconds for reply (default: 5)
 	-v       Verbose
 	-h       This help message
 
 Also see smtp-user-enum-user-docs.pdf from the smtp-user-enum tar ball.
 
 Examples:
 
 $ smtp-user-enum -M VRFY -U users.txt -t 10.0.0.1
 $ smtp-user-enum -M EXPN -u admin1 -t 10.0.0.1
 $ smtp-user-enum -M RCPT -U users.txt -T mail-server-ips.txt
 $ smtp-user-enum -M EXPN -D example.com -U users.txt -t 10.0.0.1
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## smtp-user-enum Usage Example

Use the VRFY method (`-M VRFY`) to search for the specified user (`-u root`) on the target server (`-t 192.168.1.25`):

```
root@kali:~# smtp-user-enum -M VRFY -u root -t 192.168.1.25
Starting smtp-user-enum v1.2 ( http://pentestmonkey.net/tools/smtp-user-enum )

 ----------------------------------------------------------
|                   Scan Information                       |
 ----------------------------------------------------------

Mode ..................... VRFY
Worker Processes ......... 5
Target count ............. 1
Username count ........... 1
Target TCP port .......... 25
Query timeout ............ 5 secs
Target domain ............

######## Scan started at Tue May 13 16:06:28 2014 #########
192.168.1.25: root exists
######## Scan completed at Tue May 13 16:06:29 2014 #########
1 results.

1 queries in 1 seconds (1.0 queries / sec)
```
