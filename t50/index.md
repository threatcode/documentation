---
Title: t50
Homepage: https://gitlab.com/fredericopissarra/t50
Repository: https://salsa.debian.org/pkg-security-team/t50
Architectures: linux-any
Version: 5.8.7b-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### t50
 
  Multi-protocol packet injector tool for *nix systems,
  actually supporting 15 protocols.
   
  Features:
   
   - Flooding
   - CIDR support
   - TCP, UDP, ICMP, IGMPv2, IGMPv3, EGP, DCCP, RSVP, RIPv1,
     RIPv2, GRE, ESP, AH, EIGRP and OSPF support.
   - TCP Options.
   - High performance.
   - Can hit about 1.000.000 packets per second.
 
 **Installed size:** `116 KB`  
 **How to install:** `sudo apt install t50`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### t50
 
 Network packet injector
 
 ```
 root@kali:~# t50 -h
 T50 Experimental Mixed Packet Injector Tool v5.8.7b
 Originally created by Nelson Brito <nbrito@sekure.org>
 Previously maintained by Fernando Mercês <fernando@mentebinaria.com.br>
 Maintained by Frederico Lamberti Pissarra <fredericopissarra@gmail.com>
 
 Usage: t50 <host[/cidr]> [options]
 Common Options:
     --threshold NUM           Threshold of packets to send     (default 1000)
     --flood                   This option supersedes the 'threshold'
     --encapsulated            Encapsulated protocol (GRE)      (default OFF)
  -B,--bogus-csum              Bogus checksum                   (default OFF)
     --shuffle                 Shuffling for T50 protocol       (default OFF)
  -q,--quiet                   Disable INFOs
     --turbo                   Extend the performance           (default OFF)
  -l,--list-protocols          List all available protocols
  -v,--version                 Print version and exit
  -h,--help                    Display this help and exit
 
 GRE Options:
     --gre-seq-present         GRE sequence # present           (default OFF)
     --gre-key-present         GRE key present                  (default OFF)
     --gre-sum-present         GRE checksum present             (default OFF)
     --gre-key NUM             GRE key                          (default RANDOM)
     --gre-sequence NUM        GRE sequence #                   (default RANDOM)
     --gre-saddr ADDR          GRE IP source IP address         (default RANDOM)
     --gre-daddr ADDR          GRE IP destination IP address    (default RANDOM)
 
 DCCP/TCP/UDP Options:
     --sport NUM               DCCP|TCP|UDP source port         (default RANDOM)
     --dport NUM               DCCP|TCP|UDP destination port    (default RANDOM)
 
 TCP Options:
     --ack-seq NUM             TCP ACK sequence #               (default RANDOM)
     --sequence NUM            TCP SYN sequence #               (default RANDOM)
     --data-offset NUM         TCP data offset                  (default 5)
  -F,--fin                     TCP FIN flag                     (default OFF)
  -S,--syn                     TCP SYN flag                     (default OFF)
  -R,--rst                     TCP RST flag                     (default OFF)
  -P,--psh                     TCP PSH flag                     (default OFF)
  -A,--ack                     TCP ACK flag                     (default OFF)
  -U,--urg                     TCP URG flag                     (default OFF)
  -E,--ece                     TCP ECE flag                     (default OFF)
  -C,--cwr                     TCP CWR flag                     (default OFF)
  -W,--window NUM              TCP Window size                  (default NONE)
     --urg-pointer NUM         TCP URG pointer                  (default NONE)
     --mss NUM                 TCP Maximum Segment Size         (default NONE)
     --wscale NUM              TCP Window Scale                 (default NONE)
     --tstamp NUM:NUM          TCP Timestamp (TSval:TSecr)      (default NONE)
     --sack-ok                 TCP SACK-Permitted               (default OFF)
     --ttcp-cc NUM             T/TCP Connection Count (CC)      (default NONE)
     --ccnew NUM               T/TCP Connection Count (CC.NEW)  (default NONE)
     --ccecho NUM              T/TCP Connection Count (CC.ECHO) (default NONE)
     --sack NUM:NUM            TCP SACK Edges (Left:Right)      (default NONE)
     --md5-signature           TCP MD5 signature included       (default OFF)
     --authentication          TCP-AO authentication included   (default OFF)
     --auth-key-id NUM         TCP-AO authentication key ID     (default 1)
     --auth-next-key NUM       TCP-AO authentication next key   (default 1)
     --nop                     TCP No-Operation                 (default EOL)
 
 IP Options:
  -s,--saddr ADDR              IP source IP address             (default RANDOM)
     --tos NUM                 IP type of service               (default 0x40)
     --id NUM                  IP identification                (default RANDOM)
     --frag-offset NUM         IP fragmentation offset          (default 0)
     --ttl NUM                 IP time to live                  (default 255)
     --protocol PROTO          IP protocol                      (default TCP)
 
 ICMP Options:
     --icmp-type NUM           ICMP type                        (default 8)
     --icmp-code NUM           ICMP code                        (default 0)
     --icmp-gateway ADDR       ICMP redirect gateway            (default RANDOM)
     --icmp-id NUM             ICMP identification              (default RANDOM)
     --icmp-sequence NUM       ICMP sequence #                  (default RANDOM)
 
 EGP Options:
     --egp-type NUM            EGP type                         (default 3)
     --egp-code NUM            EGP code                         (default 3)
     --egp-status NUM          EGP status                       (default 1)
     --egp-as NUM              EGP autonomous system            (default RANDOM)
     --egp-sequence NUM        EGP sequence #                   (default RANDOM)
     --egp-hello NUM           EGP hello interval               (default RANDOM)
     --egp-poll NUM            EGP poll interval                (default RANDOM)
 
 RIP Options:
     --rip-command NUM         RIPv1/v2 command                 (default 2)
     --rip-family NUM          RIPv1/v2 address family          (default 2)
     --rip-address ADDR        RIPv1/v2 router address          (default RANDOM)
     --rip-metric NUM          RIPv1/v2 router metric           (default RANDOM)
     --rip-domain NUM          RIPv2 router domain              (default RANDOM)
     --rip-tag NUM             RIPv2 router tag                 (default RANDOM)
     --rip-netmask ADDR        RIPv2 router subnet mask         (default RANDOM)
     --rip-next-hop ADDR       RIPv2 router next hop            (default RANDOM)
     --rip-authentication      RIPv2 authentication included    (default OFF)
     --rip-auth-key-id NUM     RIPv2 authentication key ID      (default 1)
     --rip-auth-sequence NUM   RIPv2 authentication sequence #  (default RANDOM)
 
 DCCP Options:
     --dccp-data-offset NUM    DCCP data offset                 (default VARY)
     --dccp-cscov NUM          DCCP checksum coverage           (default 0)
     --dccp-ccval NUM          DCCP HC-Sender CCID              (default RANDOM)
     --dccp-type NUM           DCCP type                        (default 0)
     --dccp-extended           DCCP extend for sequence #       (default OFF)
     --dccp-sequence-1 NUM     DCCP sequence #                  (default RANDOM)
     --dccp-sequence-2 NUM     DCCP extended sequence #         (default RANDOM)
     --dccp-sequence-3 NUM     DCCP sequence # low              (default RANDOM)
     --dccp-service NUM        DCCP service code                (default RANDOM)
     --dccp-acknowledge-1 NUM  DCCP acknowledgment # high       (default RANDOM)
     --dccp-acknowledge-2 NUM  DCCP acknowledgment # low        (default RANDOM)
     --dccp-reset-code NUM     DCCP reset code                  (default RANDOM)
 
 RSVP Options:
     --rsvp-flags NUM          RSVP flags                       (default 1)
     --rsvp-type NUM           RSVP message type                (default 1)
     --rsvp-ttl NUM            RSVP time to live                (default 254)
     --rsvp-session-addr ADDR  RSVP SESSION destination address (default RANDOM)
     --rsvp-session-proto NUM  RSVP SESSION protocol ID         (default 1)
     --rsvp-session-flags NUM  RSVP SESSION flags               (default 1)
     --rsvp-session-port NUM   RSVP SESSION destination port    (default RANDOM)
     --rsvp-hop-addr ADDR      RSVP HOP neighbor address        (default RANDOM)
     --rsvp-hop-iface NUM      RSVP HOP logical interface       (default RANDOM)
     --rsvp-time-refresh NUM   RSVP TIME refresh interval       (default 360)
     --rsvp-error-addr ADDR    RSVP ERROR node address          (default RANDOM)
     --rsvp-error-flags NUM    RSVP ERROR flags                 (default 2)
     --rsvp-error-code NUM     RSVP ERROR code                  (default 2)
     --rsvp-error-value NUM    RSVP ERROR value                 (default 8)
     --rsvp-scope NUM          RSVP SCOPE # of address(es)      (default 1)
     --rsvp-address ADDR,...   RSVP SCOPE address(es)           (default RANDOM)
     --rsvp-style-option NUM   RSVP STYLE option vector         (default 18)
     --rsvp-sender-addr ADDR   RSVP SENDER TEMPLATE address     (default RANDOM)
     --rsvp-sender-port NUM    RSVP SENDER TEMPLATE port        (default RANDOM)
     --rsvp-tspec-traffic      RSVP TSPEC service traffic       (default OFF)
     --rsvp-tspec-guaranteed   RSVP TSPEC service guaranteed    (default OFF)
     --rsvp-tspec-r NUM        RSVP TSPEC token bucket rate     (default RANDOM)
     --rsvp-tspec-b NUM        RSVP TSPEC token bucket size     (default RANDOM)
     --rsvp-tspec-p NUM        RSVP TSPEC peak data rate        (default RANDOM)
     --rsvp-tspec-m NUM        RSVP TSPEC minimum policed unit  (default RANDOM)
     --rsvp-tspec-M NUM        RSVP TSPEC maximum packet size   (default RANDOM)
     --rsvp-adspec-ishop NUM   RSVP ADSPEC IS HOP count         (default RANDOM)
     --rsvp-adspec-path NUM    RSVP ADSPEC path b/w estimate    (default RANDOM)
     --rsvp-adspec-m NUM       RSVP ADSPEC minimum path latency (default RANDOM)
     --rsvp-adspec-mtu NUM     RSVP ADSPEC composed MTU         (default RANDOM)
     --rsvp-adspec-guaranteed  RSVP ADSPEC service guaranteed   (default OFF)
     --rsvp-adspec-Ctot NUM    RSVP ADSPEC ETE composed value C (default RANDOM)
     --rsvp-adspec-Dtot NUM    RSVP ADSPEC ETE composed value D (default RANDOM)
     --rsvp-adspec-Csum NUM    RSVP ADSPEC SLR point composed C (default RANDOM)
     --rsvp-adspec-Dsum NUM    RSVP ADSPEC SLR point composed D (default RANDOM)
     --rsvp-adspec-controlled  RSVP ADSPEC service controlled   (default OFF)
     --rsvp-confirm-addr ADDR  RSVP CONFIRM receiver address    (default RANDOM)
 
 IPSEC Options:
     --ipsec-ah-length NUM     IPSec AH header length           (default NONE)
     --ipsec-ah-spi NUM        IPSec AH SPI                     (default RANDOM)
     --ipsec-ah-sequence NUM   IPSec AH sequence #              (default RANDOM)
     --ipsec-esp-spi NUM       IPSec ESP SPI                    (default RANDOM)
     --ipsec-esp-sequence NUM  IPSec ESP sequence #             (default RANDOM)
 
 EIGRP Options:
     --eigrp-opcode NUM        EIGRP opcode                     (default 1)
     --eigrp-flags NUM         EIGRP flags                      (default RANDOM)
     --eigrp-sequence NUM      EIGRP sequence #                 (default RANDOM)
     --eigrp-acknowledge NUM   EIGRP acknowledgment #           (default RANDOM)
     --eigrp-as NUM            EIGRP autonomous system          (default RANDOM)
     --eigrp-type NUM          EIGRP type                       (default 258)
     --eigrp-length NUM        EIGRP length                     (default NONE)
     --eigrp-k1 NUM            EIGRP parameter K1 value         (default 1)
     --eigrp-k2 NUM            EIGRP parameter K2 value         (default 0)
     --eigrp-k3 NUM            EIGRP parameter K3 value         (default 1)
     --eigrp-k4 NUM            EIGRP parameter K4 value         (default 0)
     --eigrp-k5 NUM            EIGRP parameter K5 value         (default 0)
     --eigrp-hold NUM          EIGRP parameter hold time        (default 360)
     --eigrp-ios-ver NUM.NUM   EIGRP IOS release version        (default 12.4)
     --eigrp-rel-ver NUM.NUM   EIGRP PROTO release version      (default 1.2)
     --eigrp-next-hop ADDR     EIGRP [in|ex]ternal next-hop     (default RANDOM)
     --eigrp-delay NUM         EIGRP [in|ex]ternal delay        (default RANDOM)
     --eigrp-bandwidth NUM     EIGRP [in|ex]ternal bandwidth    (default RANDOM)
     --eigrp-mtu NUM           EIGRP [in|ex]ternal MTU          (default 1500)
     --eigrp-hop-count NUM     EIGRP [in|ex]ternal hop count    (default RANDOM)
     --eigrp-load NUM          EIGRP [in|ex]ternal load         (default RANDOM)
     --eigrp-reliability NUM   EIGRP [in|ex]ternal reliability  (default RANDOM)
     --eigrp-daddr ADDR/CIDR   EIGRP [in|ex]ternal address(es)  (default RANDOM)
     --eigrp-src-router ADDR   EIGRP external source router     (default RANDOM)
     --eigrp-src-as NUM        EIGRP external autonomous system (default RANDOM)
     --eigrp-tag NUM           EIGRP external arbitrary tag     (default RANDOM)
     --eigrp-proto-metric NUM  EIGRP external protocol metric   (default RANDOM)
     --eigrp-proto-id NUM      EIGRP external protocol ID       (default 2)
     --eigrp-ext-flags NUM     EIGRP external flags             (default RANDOM)
     --eigrp-address ADDR      EIGRP multicast sequence address (default RANDOM)
     --eigrp-multicast NUM     EIGRP multicast sequence #       (default RANDOM)
     --eigrp-authentication    EIGRP authentication included    (default OFF)
     --eigrp-auth-key-id NUM   EIGRP authentication key ID      (default 1)
 
 OSPF Options:
     --ospf-type NUM           OSPF type                        (default 1)
     --ospf-length NUM         OSPF length                      (default NONE)
     --ospf-router-id ADDR     OSPF router ID                   (default RANDOM)
     --ospf-area-id ADDR       OSPF area ID                     (default 0.0.0.0)
  -1,--ospf-option-MT          OSPF multi-topology / TOS-based  (default RANDOM)
  -2,--ospf-option-E           OSPF external routing capability (default RANDOM)
  -3,--ospf-option-MC          OSPF multicast capable           (default RANDOM)
  -4,--ospf-option-NP          OSPF NSSA supported              (default RANDOM)
  -5,--ospf-option-L           OSPF LLS data block contained    (default RANDOM)
  -6,--ospf-option-DC          OSPF demand circuits supported   (default RANDOM)
  -7,--ospf-option-O           OSPF Opaque-LSA                  (default RANDOM)
  -8,--ospf-option-DN          OSPF DOWN bit                    (default RANDOM)
     --ospf-netmask ADDR       OSPF router subnet mask          (default RANDOM)
     --ospf-hello-interval NUM OSPF HELLO interval              (default RANDOM)
     --ospf-hello-priority NUM OSPF HELLO router priority       (default 1)
     --ospf-hello-dead NUM     OSPF HELLO router dead interval  (default 360)
     --ospf-hello-design ADDR  OSPF HELLO designated router     (default RANDOM)
     --ospf-hello-backup ADDR  OSPF HELLO backup designated     (default RANDOM)
     --ospf-neighbor NUM       OSPF HELLO # of neighbor(s)      (default NONE)
     --ospf-address ADDR,...   OSPF HELLO neighbor address(es)  (default RANDOM)
     --ospf-dd-mtu NUM         OSPF DD MTU                      (default 1500)
     --ospf-dd-dbdesc-MS       OSPF DD master/slave bit option  (default RANDOM)
     --ospf-dd-dbdesc-M        OSPF DD more bit option          (default RANDOM)
     --ospf-dd-dbdesc-I        OSPF DD init bit option          (default RANDOM)
     --ospf-dd-dbdesc-R        OSPF DD out-of-band resync       (default RANDOM)
     --ospf-dd-sequence NUM    OSPF DD sequence #               (default RANDOM)
     --ospf-dd-include-lsa     OSPF DD include LSA header       (default OFF)
     --ospf-lsa-age NUM        OSPF LSA age                     (default 360)
     --ospf-lsa-do-not-age     OSPF LSA do not age              (default OFF)
     --ospf-lsa-type NUM       OSPF LSA type                    (default 1)
     --ospf-lsa-id ADDR        OSPF LSA ID address              (default RANDOM)
     --ospf-lsa-router ADDR    OSPF LSA advertising router      (default RANDOM)
     --ospf-lsa-sequence NUM   OSPF LSA sequence #              (default RANDOM)
     --ospf-lsa-metric NUM     OSPF LSA metric                  (default RANDOM)
     --ospf-lsa-flag-B         OSPF Router-LSA border router    (default RANDOM)
     --ospf-lsa-flag-E         OSPF Router-LSA external router  (default RANDOM)
     --ospf-lsa-flag-V         OSPF Router-LSA virtual router   (default RANDOM)
     --ospf-lsa-flag-W         OSPF Router-LSA wild router      (default RANDOM)
     --ospf-lsa-flag-NT        OSPF Router-LSA NSSA translation (default RANDOM)
     --ospf-lsa-link-id ADDR   OSPF Router-LSA link ID          (default RANDOM)
     --ospf-lsa-link-data ADDR OSPF Router-LSA link data        (default RANDOM)
     --ospf-lsa-link-type NUM  OSPF Router-LSA link type        (default 1)
     --ospf-lsa-attached ADDR  OSPF Network-LSA attached router (default RANDOM)
     --ospf-lsa-larger         OSPF ASBR/NSSA-LSA ext. larger   (default OFF)
     --ospf-lsa-forward ADDR   OSPF ASBR/NSSA-LSA forward       (default RANDOM)
     --ospf-lsa-external ADDR  OSPF ASBR/NSSA-LSA external      (default RANDOM)
     --ospf-vertex-router      OSPF Group-LSA type router       (default RANDOM)
     --ospf-vertex-network     OSPF Group-LSA type network      (default RANDOM)
     --ospf-vertex-id ADDR     OSPF Group-LSA vertex ID         (default RANDOM)
     --ospf-lls-extended-LR    OSPF LLS Extended option LR      (default OFF)
     --ospf-lls-extended-RS    OSPF LLS Extended option RS      (default OFF)
     --ospf-authentication     OSPF authentication included     (default OFF)
     --ospf-auth-key-id NUM    OSPF authentication key ID       (default 1)
     --ospf-auth-sequence NUM  OSPF authentication sequence #   (default RANDOM)
 
 Some considerations while running this program:
  1. There is no limitation of using as many options as possible.
  2. Report t50 bugs at https://gitlab.com/fredericopissarra/t50.git.
  3. Some header fields with default values MUST be set to '0' for RANDOM.
  4. Mandatory arguments to long options are mandatory for short options too.
  5. Be nice when using t50, the author DENIES its use for DoS/DDoS purposes.
  6. Running t50 with '--protocol T50' option sends ALL protocols sequentially.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## t50 Usage Example

Run a default flood test (`–flood`) against the destination IP (`192.168.1.1`):

```
root@kali:~# t50 --flood 192.168.1.1
entering in flood mode...
hit CTRL+C to break.
T50 5.4.1-rc1 successfully launched on May 17th 2014 10:48:51
```
