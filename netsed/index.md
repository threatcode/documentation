---
Title: netsed
Homepage: http://silicone.homelinux.org/projects/netsed/
Repository: https://anonscm.debian.org/cgit/collab-maint/netsed.git
Architectures: any
Version: 1.2-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### netsed
 
  NetSED is a small and handy utility designed to alter, in real time,
  the contents of packets forwarded through your network. It is really
  useful for network packet alteration, forging, or manipulation.
  NetSED supports:
   
    * black-box protocol auditing - whenever there are two or more
      proprietary boxes communicating using some undocumented protocol.
      By enforcing changes in ongoing transmissions, you will be able
      to test if the examined application can be claimed secure;
    * fuzz generating experiments, integrity tests - whenever you do
      stability tests of an application to see how it cares for data
      integrity;
    * other common use-cases: deceptive transfers, content filtering,
      protocol conversion - whatever best fits your task at hand.
   
  It ideally complements a tool suite based on ngrep, netcat, and tcpdump.
 
 **Installed size:** `55 KB`  
 **How to install:** `sudo apt install netsed`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### netsed
 
 A network stream editor.
 
 ```
 root@kali:~# netsed -h
 Usage: netsed [option] proto lport rhost rport rule1 [ rule2 ... ]
 
   options - can be --ipv4 or -4 to force address resolution in IPv4,
             --ipv6 or -6 to force address resolution in IPv6,
             --ipany to resolve the address in either IPv4 or IPv6.
           - --help or -h to display this usage information.
   proto   - protocol specification (tcp or udp)
   lport   - local port to listen on (see README for transparent
             traffic intercepting on some systems)
   rhost   - where connection should be forwarded (0 = use destination
             address of incoming connection, see README)
   rport   - destination port (0 = dst port of incoming connection)
   ruleN   - replacement rules (see below)
 
 General syntax of replacement rules: s/pat1/pat2[/expire]
 
 This will replace all occurrences of pat1 with pat2 in any matching packet.
 An additional parameter, 'expire' of the form [CHAR][NUM], can be used to
 expire a rule after NUM successful substitutions during a given connection.
 The character CHAR is one of "iIoO", with the effect of restricting the rule
 to apply to incoming ("iI") or to outgoing ("oO") packets only, as seen from
 the client's perspective. Both of CHAR and NUM are optional.
 
 Eight-bit characters, including NULL and '/', can be applied using HTTP-like
 hex escape sequences (e.g. CRLF as %0a%0d).
 A match on '%' can be achieved by specifying '%%'.
 
 Examples:
   's/andrew/mike/1'     - replace 'andrew' with 'mike' (only first time)
   's/andrew/mike'       - replace all occurrences of 'andrew' with 'mike'
   's/andrew/mike%00%00' - replace 'andrew' with 'mike\x00\x00'
                           (manually padding to keep original size)
   's/%%/%2f/20'         - replace the 20 first occurrence of '%' with '/'
   's/andrew/mike/o'     - the server will always see 'mike', never 'andrew'
 
   's/Rilke/Proust/o s/Proust/Rilke/i'
                         - let Rilke travel incognito as Proust
 
 Rules are not active across packet boundaries, and they are evaluated
 from first to last, not yet expired rule, as stated on the command line.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
