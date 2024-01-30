---
Title: amass
Homepage: https://github.com/OWASP/Amass
Repository: https://gitlab.com/kalilinux/packages/amass
Architectures: any all
Version: 4.2.0-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-identify 
Icon: images/amass-logo.svg
PackagesInfo: |
 ### amass
 
  This package contains a tool to help information security professionals
  perform network mapping of attack surfaces and perform external asset
  discovery using open source information gathering and active reconnaissance
  techniques.
   
  Information Gathering Techniques Used:
     - DNS: Basic enumeration, Brute forcing (upon request), Reverse DNS
       sweeping, Subdomain name alterations/permutations, Zone transfers (upon
       request)
     - Scraping: Ask, Baidu, Bing, DNSDumpster, DNSTable, Dogpile, Exalead,
       Google, HackerOne, IPv4Info, Netcraft, PTRArchive, Riddler, SiteDossier,
       ViewDNS, Yahoo
     - Certificates: Active pulls (upon request), Censys, CertSpotter, Crtsh,
       Entrust, GoogleCT
     - APIs: AlienVault, BinaryEdge, BufferOver, CIRCL, CommonCrawl, DNSDB,
       HackerTarget, Mnemonic, NetworksDB, PassiveTotal, RADb, Robtex,
       SecurityTrails, ShadowServer, Shodan, Spyse (CertDB & FindSubdomains),
       Sublist3rAPI, TeamCymru, ThreatCrowd, Twitter, Umbrella, URLScan,
       VirusTotal
     - Web Archives: ArchiveIt, ArchiveToday, Arquivo, LoCArchive,
       OpenUKArchive, UKGovArchive, Wayback
   
  This package contains the command amass.
 
 **Installed size:** `34.57 MB`  
 **How to install:** `sudo apt install amass`  
 
 {{< spoiler "Dependencies:" >}}
 * amass-common 
 * libc6 
 {{< /spoiler >}}
 
 ##### amass
 
 
 ```
 root@kali:~# amass -h
 
         .+++:.            :                             .+++.
       +W@@@@@@8        &+W@#               o8W8:      +W@@@@@@#.   oW@@@W#+
      &@#+   .o@##.    .@@@o@W.o@@o       :@@#&W8o    .@#:  .:oW+  .@#+++&#&
     +@&        &@&     #@8 +@W@&8@+     :@W.   +@8   +@:          .@8
     8@          @@     8@o  8@8  WW    .@W      W@+  .@W.          o@#:
     WW          &@o    &@:  o@+  o@+   #@.      8@o   +W@#+.        +W@8:
     #@          :@W    &@+  &@+   @8  :@o       o@o     oW@@W+        oW@8
     o@+          @@&   &@+  &@+   #@  &@.      .W@W       .+#@&         o@W.
      WW         +@W@8. &@+  :&    o@+ #@      :@W&@&         &@:  ..     :@o
      :@W:      o@# +Wo &@+        :W: +@W&o++o@W. &@&  8@#o+&@W.  #@:    o@+
       :W@@WWWW@@8       +              :&W@@@@&    &W  .o#@@W&.   :W@WWW@@&
         +o&&&&+.                                                    +oooo.
 
                                                                       v4.2.0
                                            OWASP Amass Project - @owaspamass
                          In-depth Attack Surface Mapping and Asset Discovery
 
 
 Usage: amass intel|enum [options]
 
   -h	Show the program usage message
   -help
     	Show the program usage message
   -version
     	Print the version number of this Amass binary
 
 
 Subcommands: 
 
 	amass intel - Discover targets for enumerations
 	amass enum  - Perform enumerations and network mapping
 
 The user's guide can be found here: 
 https://github.com/owasp-amass/amass/blob/master/doc/user_guide.md
 
 An example configuration file can be found here: 
 https://github.com/owasp-amass/amass/blob/master/examples/config.yaml
 
 The Amass tutorial can be found here: 
 https://github.com/owasp-amass/amass/blob/master/doc/tutorial.md
 
 ```
 
 - - -
 
 ### amass-common
 
  This package contains a tool to help information security professionals
  perform network mapping of attack surfaces and perform external asset
  discovery using open source information gathering and active reconnaissance
  techniques.
   
  This package contains several wordlists for performing DNS name alterations
  and brute forcing.
 
 **Installed size:** `9.39 MB`  
 **How to install:** `sudo apt install amass-common`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
