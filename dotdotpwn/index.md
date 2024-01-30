---
Title: dotdotpwn
Homepage: https://dotdotpwn.blogspot.ca
Repository: https://gitlab.com/kalilinux/packages/dotdotpwn
Architectures: any
Version: 3.0.2-0kali4
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dotdotpwn
 
  DotDotPwn is a very flexible intelligent fuzzer to discover traversal
  directory vulnerabilities in software such as HTTP/FTP/TFTP
  servers, Web platforms such as CMSs, ERPs, Blogs, etc.
 
 **Installed size:** `236 KB`  
 **How to install:** `sudo apt install dotdotpwn`  
 
 {{< spoiler "Dependencies:" >}}
 * libnet-tftp-perl
 * libwww-perl
 * perl
 {{< /spoiler >}}
 
 ##### dotdotpwn
 
 
 ```
 root@kali:~# dotdotpwn -h
 #################################################################################
 #                                                                               #
 #  CubilFelino                                                       Chatsubo   #
 #  Security Research Lab              and            [(in)Security Dark] Labs   #
 #  chr1x.sectester.net                             chatsubo-labs.blogspot.com   #
 #                                                                               #
 #                               pr0udly present:                                #
 #                                                                               #
 #  ________            __  ________            __  __________                   #
 #  \______ \    ____ _/  |_\______ \    ____ _/  |_\______   \__  _  __ ____    #
 #   |    |  \  /  _ \\   __\|    |  \  /  _ \\   __\|     ___/\ \/ \/ //    \   #
 #   |    `   \(  <_> )|  |  |    `   \(  <_> )|  |  |    |     \     /|   |  \  #
 #  /_______  / \____/ |__| /_______  / \____/ |__|  |____|      \/\_/ |___|  /  #
 #          \/                      \/                                      \/   #
 #                              - DotDotPwn v3.0.2 -                             #
 #                         The Directory Traversal Fuzzer                        #
 #                         http://dotdotpwn.sectester.net                        #
 #                            dotdotpwn@sectester.net                            #
 #                                                                               #
 #                               by chr1x & nitr0us                              #
 #################################################################################
 
 Usage: ./dotdotpwn.pl -m <module> -h <host> [OPTIONS]
 	Available options:
 	-m	Module [http | http-url | ftp | tftp | payload | stdout]
 	-h	Hostname
 	-O	Operating System detection for intelligent fuzzing (nmap)
 	-o	Operating System type if known ("windows", "unix" or "generic")
 	-s	Service version detection (banner grabber)
 	-d	Depth of traversals (e.g. deepness 3 equals to ../../../; default: 6)
 	-f	Specific filename (e.g. /etc/motd; default: according to OS detected, defaults in TraversalEngine.pm)
 	-E	Add @Extra_files in TraversalEngine.pm (e.g. web.config, httpd.conf, etc.)
 	-S	Use SSL for HTTP and Payload module (not needed for http-url, use a https:// url instead)
 	-u	URL with the part to be fuzzed marked as TRAVERSAL (e.g. http://foo:8080/id.php?x=TRAVERSAL&y=31337)
 	-k	Text pattern to match in the response (http-url & payload modules - e.g. "root:" if trying /etc/passwd)
 	-p	Filename with the payload to be sent and the part to be fuzzed marked with the TRAVERSAL keyword
 	-x	Port to connect (default: HTTP=80; FTP=21; TFTP=69)
 	-t	Time in milliseconds between each test (default: 300 (.3 second))
 	-X	Use the Bisection Algorithm to detect the exact deepness once a vulnerability has been found
 	-e	File extension appended at the end of each fuzz string (e.g. ".php", ".jpg", ".inc")
 	-U	Username (default: 'anonymous')
 	-P	Password (default: 'dot@dot.pwn')
 	-M	HTTP Method to use when using the 'http' module [GET | POST | HEAD | COPY | MOVE] (default: GET)
 	-r	Report filename (default: 'HOST_MM-DD-YYYY_HOUR-MIN.txt')
 	-b	Break after the first vulnerability is found
 	-q	Quiet mode (doesn't print each attempt)
 	-C	Continue if no data was received from host
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## dotdotpwn Usage Example

Use the HTTP scan module (`-m http`) against a host (`-h 192.168.1.1`) , using the GET method (`-M GET`):

```
root@kali:~# dotdotpwn.pl -m http -h 192.168.1.1 -M GET
#################################################################################
#                                                                               #
#  CubilFelino                                                       Chatsubo   #
#  Security Research Lab              and            [(in)Security Dark] Labs   #
#  chr1x.sectester.net                             chatsubo-labs.blogspot.com   #
#                                                                               #
#                               pr0udly present:                                #
#                                                                               #
#  ________            __  ________            __  __________                   #
#  \______ \    ____ _/  |_\______ \    ____ _/  |_\______   \__  _  __ ____    #
#   |    |  \  /  _ \\   __\|    |  \  /  _ \\   __\|     ___/\ \/ \/ //    \   #
#   |    `   \(  <_> )|  |  |    `   \(  <_> )|  |  |    |     \     /|   |  \  #
#  /_______  / \____/ |__| /_______  / \____/ |__|  |____|      \/\_/ |___|  /  #
#          \/                      \/                                      \/   #
#                               - DotDotPwn v3.0 -                              #
#                         The Directory Traversal Fuzzer                        #
#                         http://dotdotpwn.sectester.net                        #
#                            dotdotpwn@sectester.net                            #
#                                                                               #
#                               by chr1x & nitr0us                              #
#################################################################################

[+] Report name: Reports/192.168.1.1_05-20-2014_08-41.txt

[========== TARGET INFORMATION ==========]
[+] Hostname: 192.168.1.1
[+] Protocol: http
[+] Port: 80

[=========== TRAVERSAL ENGINE ===========]
[+] Creating Traversal patterns (mix of dots and slashes)
[+] Multiplying 6 times the traversal patterns (-d switch)
[+] Creating the Special Traversal patterns
[+] Translating (back)slashes in the filenames
[+] Adapting the filenames according to the OS type detected (generic)
[+] Including Special sufixes
[+] Traversal Engine DONE ! - Total traversal tests created: 19680

[=========== TESTING RESULTS ============]
[+] Ready to launch 3.33 traversals per second
[+] Press Enter to start the testing (You can stop it pressing Ctrl + C)
```
