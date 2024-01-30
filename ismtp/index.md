---
Title: ismtp
Homepage: https://github.com/altjx/ipwn/
Repository: https://gitlab.com/kalilinux/packages/ismtp
Architectures: all
Version: 1.6+git20190922-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ismtp
 
  Test for SMTP user enumeration (RCPT TO and VRFY), internal spoofing, and
  relay.
 
 **Installed size:** `40 KB`  
 **How to install:** `sudo apt install ismtp`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### ismtp
 
 
 ```
 root@kali:~# ismtp -h
 
  Error: option -h requires argument
 
  ---------------------------------------------------------------------
   iSMTP v1.6 - SMTP Server Tester, Alton Johnson (alton.jx@gmail.com)
  ---------------------------------------------------------------------
  
  Usage: ./iSMTP.py <OPTIONS>
 
  Required:
 
 	-f <import file>	Imports a list of SMTP servers for testing.
 				(Cannot use with '-h'.)
 	-h <host>		The target IP and port (IP:port).
 				(Cannot use with '-f'.)
 
  Spoofing:
 
 	-i <consultant email>	The consultant's email address.
 	-s <sndr email>		The sender's email address.
 	-r <rcpt email>		The recipient's email address.
 	   --sr <email>		Specifies both the sender's and recipient's email address.
 	-S <sndr name>		The sender's first and last name.
 	-R <rcpt name>		The recipient's first and last name.
 	   --SR <name>		Specifies both the sender's and recipient's first and last name.
 	-m			Enables SMTP spoof testing.
 	-a			Includes .txt attachment with spoofed email.
 
  SMTP enumeration:
 
 	-e <file>	Enable SMTP user enumeration testing and imports email list.
 	-l <1|2|3>	Specifies enumeration type (1 = VRFY, 2 = RCPT TO, 3 = all).
 			(Default is 3.)
 
  SMTP relay:
 
 	-i <consultant email>	The consultant's email address.
 	-x			Enables SMTP external relay testing.
 
  Misc:
 
 	-t <secs>	The timeout value. (Default is 10.)
 	-o		Creates "ismtp-results" directory and writes output to
 			ismtp-results/smtp_<service>_<ip>(port).txt
 
  Note: Any combination of options is supported (e.g., enumeration, relay, both, all, etc.).
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## iSMTP Usage Example

Test a list of IPs from a file (`-f smtp-ips.txt`) enumerating usernames from a dictionary file (`-e /usr/share/wordlists/metasploit/unix_users.txt`):

```
root@kali:~# ismtp -f smtp-ips.txt -e /usr/share/wordlists/metasploit/unix_users.txt

 ---------------------------------------------------------------------
  iSMTP v1.6 - SMTP Server Tester, Alton Johnson (alton.jx@gmail.com)
 ---------------------------------------------------------------------

 Testing SMTP server [user enumeration]: 192.168.1.25:25
 Emails provided for testing: 109

 Performing SMTP VRFY test...

 [-] 4Dgifts ------------- [ invalid ]
 [-] EZsetup ------------- [ invalid ]
 [+] ROOT ---------------- [ success ]
 [+] adm ----------------- [ success ]
```
