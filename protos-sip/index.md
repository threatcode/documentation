---
Title: protos-sip
Homepage: https://www.ee.oulu.fi/research/ouspg/PROTOS_Test-Suite_c07-sip
Repository: https://gitlab.com/kalilinux/packages/protos-sip
Architectures: all
Version: 1.0-1kali5
Metapackages: kali-linux-everything kali-linux-large kali-tools-voip kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### protos-sip
 
  The purpose of this test-suite is to evaluate implementation
  level security and robustness of Session Initiation Protocol
  (SIP) implementations.
 
 **Installed size:** `2.15 MB`  
 **How to install:** `sudo apt install protos-sip`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 * java-wrappers
 {{< /spoiler >}}
 
 ##### protos-sip
 
 
 ```
 root@kali:~# protos-sip -h
 Usage java -jar <jarfile>.jar [ [OPTIONS] | -touri <SIP-URI> ]
 
   -touri  <addr>        Recipient of the request
                         Example: <addr> : you@there.com
   -fromuri <addr>       Initiator of the request
                         Default: user@kali
   -sendto <domain>      Send packets to <domain> instead of
                         domainname of -touri
   -callid <callid>      Call id to start test-case call ids from
                         Default: 0
   -dport <port>         Portnumber to send packets on host.
                         Default: 5060
   -lport <port>         Local portnumber to send packets from
                         Default: 5060
   -delay <ms>           Time to wait before sending new test-case
                         Defaults to 100 ms (milliseconds)
   -replywait <ms>       Maximum time to wait for host to reply
                         Defaults to 100 ms (milliseconds)
   -file <file>          Send file <file> instead of test-case(s)
   -help                 Display this help
   -jarfile <file>       Get data from an alternate bugcat
                         JAR-file <file>
   -showreply            Show received packets
   -showsent             Show sent packets
   -teardown             Send CANCEL/ACK
   -single <index>       Inject a single test-case <index>
   -start <index>        Inject test-cases starting from <index>
   -stop <index>         Stop test-case injection to <index>
   -maxpdusize <int>     Maximum PDU size
                         Default to 65507 bytes
   -validcase            Send valid case (case #0) after each
                         test-case and wait for a response. May
                         be used to check if the target is still
                         responding. Default: off
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
