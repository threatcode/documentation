---
Title: cntlm
Homepage: http://cntlm.sourceforge.net/
Repository: http://projects.planetwatson.co.uk/repositories/show/cntlm
Architectures: any
Version: 0.92.3-1.2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cntlm
 
  Cntlm is a fast and efficient NTLM proxy, with support for TCP/IP tunneling,
  authenticated connection caching, ACLs, proper daemon logging and behaviour
  and much more. It has up to ten times faster responses than similar NTLM
  proxies, while using by orders or magnitude less RAM and CPU. Manual page
  contains detailed information.
 
 **Installed size:** `148 KB`  
 **How to install:** `sudo apt install cntlm`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 {{< /spoiler >}}
 
 ##### cntlm
 
 Authenticating HTTP(S) proxy with TCP/IP tunneling and acceleration
 
 ```
 root@kali:~# cntlm -h
 Usage: cntlm [-AaBcDdFfgHhILlMPpSsTUuvw] <proxy_host>[:]<proxy_port> ...
 	-A  <address>[/<net>]
 	    ACL allow rule. IP or hostname, net must be a number (CIDR notation)
 	-a  ntlm | nt | lm
 	    Authentication type - combined NTLM, just LM, or just NT. Default NTLM.
 	    It is the most versatile setting and likely to work for you.
 	-B  Enable NTLM-to-basic authentication.
 	-c  <config_file>
 	    Configuration file. Other arguments can be used as well, overriding
 	    config file settings.
 	-D  <address>[/<net>]
 	    ACL deny rule. Syntax same as -A.
 	-d  <domain>
 	    Domain/workgroup can be set separately.
 	-f  Run in foreground, do not fork into daemon mode.
 	-F  <flags>
 	    NTLM authentication flags.
 	-G  <pattern>
 	    User-Agent matching for the trans-isa-scan plugin.
 	-g  Gateway mode - listen on all interfaces, not only loopback.
 	-H  Print password hashes for use in config file (NTLMv2 needs -u and -d).
 	-h  Print this help info along with version number.
 	-I  Prompt for the password interactively.
 	-L  [<saddr>:]<lport>:<rhost>:<rport>
 	    Forwarding/tunneling a la OpenSSH. Same syntax - listen on lport
 	    and forward all connections through the proxy to rhost:rport.
 	    Can be used for direct tunneling without corkscrew, etc.
 	-l  [<saddr>:]<lport>
 	    Main listening port for the NTLM proxy.
 	-M  <testurl>
 	    Magic autodetection of proxy's NTLM dialect.
 	-N  "<hostname_wildcard1>[, <hostname_wildcardN>"
 	    List of URL's to serve direcly as stand-alone proxy (e.g. '*.local')
 	-O  [<saddr>:]<lport>
 	    Enable SOCKS5 proxy on port lport (binding to address saddr)
 	-P  <pidfile>
 	    Create a PID file upon successful start.
 	-p  <password>
 	    Account password. Will not be visible in "ps", /proc, etc.
 	-r  "HeaderName: value"
 	    Add a header substitution. All such headers will be added/replaced
 	    in the client's requests.
 	-S  <size_in_kb>
 	    Enable automation of GFI WebMonitor ISA scanner for files < size_in_kb.
 	-s  Do not use threads, serialize all requests - for debugging only.
 	-U  <uid>
 	    Run as uid. It is an important security measure not to run as root.
 	-u  <user>[@<domain]
 	    Domain/workgroup can be set separately.
 	-v  Print debugging information.
 	-w  <workstation>
 	    Some proxies require correct NetBIOS hostname.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
