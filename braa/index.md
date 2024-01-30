---
Title: braa
Homepage: http://s-tech.elsat.net.pl/
Repository: https://salsa.debian.org/pkg-security-team/braa
Architectures: any
Version: 0.82-7
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### braa
 
  Braa is a mass snmp scanner. The intended usage of such a tool is of course
  making SNMP queries - but unlike snmpget or snmpwalk from net-snmp, it is able
  to query dozens or hundreds of hosts simultaneously, and in a single process.
  Thus, it consumes very few system resources and does the scanning VERY fast.
   
  Braa implements its OWN snmp stack, so it does NOT need any SNMP libraries
  like net-snmp. The implementation is very dirty, supports only several data
  types, and in any case cannot be stated 'standard-conforming'! It was designed
  to be fast, and it is fast. For this reason (well, and also because of author
  laziness ;), there is no ASN.1 parser in braa - the user HAVE to know the
  numerical values of OID's
  (for instance .1.3.6.1.2.1.1.5.0 instead of system.sysName.0).
 
 **Installed size:** `62 KB`  
 **How to install:** `sudo apt install braa`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### braa
 
 Mass SNMP scanner
 
 ```
 root@kali:~# braa -h
 braa 0.82 - Mateusz 'mteg' Golicz <mtg@elsat.net.pl>, 2003 - 2006
 usage: braa [options] [query1] [query2] ...
   -h        Show this help.
   -2        Claim to be a SNMP2C agent.
   -v        Show short summary after doing all queries.
   -x        Hexdump octet-strings
   -t <s>    Wait <s> seconds for responses.
   -d <s>    Wait <s> microseconds after sending each packet.
   -p <s>    Wait <s> milliseconds between subsequent passes.
   -f <file> Load queries from file <file> (one by line).
   -a <time> Quit after <time> seconds, independent on what happens.
   -r <rc>   Retry count (default: 3).
 
 Query format:
   GET:   [community@]iprange[:port]:oid[/id]
   WALK:  [community@]iprange[:port]:oid.*[/id]
   SET:   [community@]iprange[:port]:oid=value[/id]
 
 Examples:
          public@10.253.101.1:161:.1.3.6.*
          10.253.101.1-10.253.101.255:.1.3.6.1.2.1.1.4.0=sme
          10.253.101.1:.1.3.6.1.2.1.1.1.0/description
 
 It is also possible to specify multiple queries at once:
          10.253.101.1-10.253.101.255:.1.3.6.1.2.1.1.4.0=sme,.1.3.6.*
          (Will set .1.3.6.1.2.1.1.4.0 to 'me' and do a walk starting from .1.3.6)
 
 
 Values for SET queries have to be prepended with a character specifying the value type:
   i      is INTEGER
   a      is IPADDRESS
   s      is OCTET STRING
   o      is OBJECT IDENTIFIER
 If the type specifier is missing, the value type is auto-detected
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## braa Usage Example

Walk the SNMP tree on `192.168.1.215` using the community string of `public`, querying all OIDs under `.1.3.6`:

````
root@kali:~# braa public@192.168.1.215:.1.3.6.*
192.168.1.215:122ms:.1.3.6.1.2.1.1.1.0:Linux redhat.biz.local 2.4.20-8 #1 Thu Mar 13 17:54:28 EST 2003 i686
192.168.1.215:143ms:.1.3.6.1.2.1.1.2.0:.1.3.6.1.4.1.8072.3.2.10
192.168.1.215:122ms:.1.3.6.1.2.1.1.3.0:4051218219
192.168.1.215:122ms:.1.3.6.1.2.1.1.4.0:Root <root@localhost> (configure /etc/snmp/snmp.local.conf)
192.168.1.215:143ms:.1.3.6.1.2.1.1.5.0:redhat.biz.local
```
