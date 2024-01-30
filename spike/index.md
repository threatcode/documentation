---
Title: spike
Homepage: http://www.immunitysec.com/resources-freesoftware.shtml
Repository: https://gitlab.com/kalilinux/packages/spike
Architectures: any
Version: 2.9-1kali9
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-fuzzing kali-tools-vulnerability 
Icon: images/spike-logo.svg
PackagesInfo: |
 ### spike
 
  When you need to analyze a new network protocol for buffer
  overflows or similar weaknesses, the SPIKE is the tool of
  choice for professionals. While it requires a strong
  knowledge of C to use, it produces results second to none
  in the field.
 
 **Installed size:** `3.77 MB`  
 **How to install:** `sudo apt install spike`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### citrix
 
 
 ```
 root@kali:~# citrix -h
 Usage: ./citrix target port
 ./citrix 192.168.1.101 1494
 ```
 
 - - -
 
 ##### closed_source_web_server_fuzz
 
 
 ```
 root@kali:~# closed_source_web_server_fuzz -h
 Example: ./closed localhost 80 POST /_vti_bin/ shtml .exe 0 0
 Don't forget the period before the extention.
 Common Extentions are: .asa .asp .cdx .cer .htw .htr .ida .idc .idq .shtm .shtml .stm .printer .jsp .jhtml .bat .exe .com .gif .jpg .mpg .rma .wma .cfm .pl .py .pike, etc
 Common methods are OPTIONS, TRACE, GET, HEAD, DELETE, PUT, POST, COPY, MOVE, MKCOL, PROPFIND, PROPPATCH, LOCK, UNLOCK, SEARCH, BROWSE
 Try with both existing and NON existing files. Also try .dll with .exe and vice versa
 Try ALL the extentions and go into your server settings windows and try all methods and all directories as well. If it crashes, ask for a refund.
 Anything that says, 500 Server Error, also indicates a buggy web server. Might even be exploitable.
 Likewise to anything like Error (not 0x80040e14, which MS uses for 'not an overflow' for some reason) caught while processing query. These are signs of serious problems in the web server.
 Happy bug hunting!
 contact Dave Aitel if you find anything cool. :> 
 ```
 
 - - -
 
 ##### dceoversmb
 
 
 ```
 root@kali:~# dceoversmb -h
 Argc=2 not 9
 Usage: ./dceoversmb target pipe GUID Version VersionMinor(usually 0) function_number number_of_tries max_number_of_random_items
 Example: ./dceoversmb 10.25.25.15 \\pipe\\srvsvc e1af8308-5d1f-11c9-91a4-08002b14a0fa 3 0 2 10 3 [login password]
 Read the msrpc readme when you get a chance.
 ```
 
 - - -
 
 ##### dltest
 
 
 ```
 root@kali:~# dltest -h
 Couldn't open file test.spk to parse with s_parse()
 ```
 
 - - -
 
 ##### do_post
 
 
 ```
 root@kali:~# do_post -h
 Usage: ./post_spike target port optional
 ```
 
 - - -
 
 ##### generic_chunked
 
 
 ```
 root@kali:~# generic_chunked -h
 Usage: ./generic_web_server_fuzz target port file.spk skipvariables skipfuzzstring
 Example: ./gwsf exchange1 80 owa1.spk 0 0
 http://www.immunitysec.com/spike.html
 ```
 
 - - -
 
 ##### generic_listen_tcp
 
 
 ```
 root@kali:~# generic_listen_tcp -h
 argc=2
 Usage: ./generic_listen_tcp port spike_script
 ./generic_listen_tcp 70 gopherd.spk
 ```
 
 - - -
 
 ##### generic_send_tcp
 
 
 ```
 root@kali:~# generic_send_tcp -h
 argc=2
 Usage: ./generic_send_tcp host port spike_script SKIPVAR SKIPSTR
 ./generic_send_tcp 192.168.1.100 701 something.spk 0 0
 ```
 
 - - -
 
 ##### generic_send_udp
 
 
 ```
 root@kali:~# generic_send_udp -h
 argc=2
 Usage: ./gsu target port file.spk startvariable startfuzzstring startvariable startstring totaltosend
 ./gsu 192.168.1.104 80 file.spk 0 0 5000
 ```
 
 - - -
 
 ##### generic_web_server_fuzz
 
 
 ```
 root@kali:~# generic_web_server_fuzz -h
 Usage: ./generic_web_server_fuzz target port file.spk skipvariables skipfuzzstring
 Example: ./gwsf exchange1 80 owa1.spk 0 0
 http://www.immunitysec.com/spike.html
 ```
 
 - - -
 
 ##### generic_web_server_fuzz2
 
 
 ```
 root@kali:~# generic_web_server_fuzz2 -h
 Usage: ./generic_web_server_fuzz target port file.spk skipvariables skipfuzzstring
 Example: ./gwsf exchange1 80 owa1.spk 0 0
 http://www.immunitysec.com/spike.html
 ```
 
 - - -
 
 ##### gopherd
 
 
 
 - - -
 
 ##### halflife
 
 
 ```
 root@kali:~# halflife -h
 Usage: ./halflife target port
 ./halflife 192.168.1.101 27010
 ```
 
 - - -
 
 ##### line_send_tcp
 
 
 ```
 root@kali:~# line_send_tcp -h
 argc=2
 Usage: ./line_send_tcp host port spike_script SKIPVAR SKIPSTR
 ./line_send_tcp 192.168.1.100 701 something.spk 0 0
 ```
 
 - - -
 
 ##### msrpcfuzz
 
 
 ```
 root@kali:~# msrpcfuzz -h
 Argc=2 not 9
 Usage: ./msrpcfuzz target port GUID Version VersionMinor(usually 0) function_number number_of_tries max_number_of_random_items
 Example: ./msrpcfuzz 10.25.25.15 135 e1af8308-5d1f-11c9-91a4-08002b14a0fa 3 0 2 10 3 [OBJECT UUID]
 use a while [ 1 ]; do ./msrpcfuzz ... ; done loop to make things continue nicely.
 You're using MSRPCFUZZ written by Dave Aitel in November 2001
 This program protected by GPL v 2.0
 This program's Version = 1.0 I hope you know what you're doing. :>
 Set RANDVAL=int if you don't want to use getpid()
 If you're doing that, set MSRPC_DO=int as well.
 Read the msrpc readme when you get a chance.
 ```
 
 - - -
 
 ##### msrpcfuzz_udp
 
 
 ```
 root@kali:~# msrpcfuzz_udp -h
 Argc=2 not 9
 Usage: ./msrpcfuzz_udp target port GUID Version VersionMinor(usually 0) function_number number_of_tries max_number_of_random_items
 Example: ./msrpcfuzz_udp 10.25.25.15 135 e1af8308-5d1f-11c9-91a4-08002b14a0fa 3 0 2 10 3 [OBJECT UUID]
 use a while [ 1 ]; do ./msrpcfuzz ... ; done loop to make things continue nicely.
 You're using MSRPCFUZZ written by Dave Aitel in November 2001
 This program protected by GPL v 2.0
 This program's Version = 1.0 I hope you know what you're doing. :>
 Set RANDVAL=int if you don't want to use getpid()
 If you're doing that, set MSRPC_DO=int as well.
 Read the msrpc readme when you get a chance.
 ```
 
 - - -
 
 ##### ntlm2
 
 
 ```
 root@kali:~# ntlm2 -h
 Usage: ./ntlm_brute target port username[@domain] password url
 If you get a nice message from the server saying Use Localhost only, then you got the right password. Use a shell script to spam this througha word list or something. 
 ```
 
 - - -
 
 ##### ntlm_brute
 
 
 ```
 root@kali:~# ntlm_brute -h
 Usage: ./ntlm_brute target port username[@domain] password url
 If you get a nice message from the server saying Use Localhost only, then you got the right password. Use a shell script to spam this througha word list or something. 
 ```
 
 - - -
 
 ##### pmspike
 
 
 
 - - -
 
 ##### post_fuzz
 
 
 ```
 root@kali:~# post_fuzz -h
 Usage: ./post_fuzz target port file
 Example: ./post_fuzz localhost 80 /bob2.php
 This should find the php bug, and similar bugs
 Happy bug hunting!
 contact Dave Aitel if you find anything cool. :> 
 ```
 
 - - -
 
 ##### post_spike
 
 
 ```
 root@kali:~# post_spike -h
 Usage: ./post_spike target port
 ```
 
 - - -
 
 ##### quake
 
 
 ```
 root@kali:~# quake -h
 Usage: ./quake target port
 ./quake 192.168.1.102 27960
 ```
 
 - - -
 
 ##### quakeserver
 
 
 ```
 root@kali:~# quakeserver -h
 Usage: ./quakeserver clienthost port
 ./quakeserver 192.168.1.102 27960
 ```
 
 - - -
 
 ##### sendmsrpc
 
 
 ```
 root@kali:~# sendmsrpc -h
 Argc=2 not 4
 Usage: ./sendmsrpc target port function
 ```
 
 - - -
 
 ##### ss_spike
 
 
 
 - - -
 
 ##### statd_spike
 
 
 
 - - -
 
 ##### sunrpcfuzz
 
 
 ```
 root@kali:~# sunrpcfuzz -h
 
 Usage:
 sunrpcfuzz -h <target host> <-s and/or -a> [optional args]
 	-s <n>	Test a specific RCP program 'n' [requires -v, and -p]
 	-a	Test all registered RPC programs
 
 WARNING: avoid running with -a or -s 100000 against
 localhost--doing so will probably register a bunch of bogus
 RPC programs with the local portmapper.
 
 Optional Arguments:
 	-v <program version>
 	-p <protocol number, 17 for UDP or 6 for TCP>
 	-i <n>	Do 'n' fuzzed messages per procedure
 	-l <n>	'n' is last procedure to test
 	-f <n>	'n' is first procedure to test
 	-r <n>	Push 'n' random xdr items onto the SPIKE
 
 ```
 
 - - -
 
 ##### webfuzz
 
 
 
 - - -
 
 ##### x11_spike
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
