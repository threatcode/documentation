---
Title: reconspider
Homepage: https://github.com/bhavsec/reconspider
Repository: https://gitlab.com/kalilinux/packages/reconspider
Architectures: all
Version: 1.0.7-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### reconspider
 
  This package contains Advanced Open Source Intelligence (OSINT) Framework for
  scanning IP Address, Emails, Websites, Organizations and find out information
  from different sources.
   
  ReconSpider can be used by Infosec Researchers, Penetration Testers, Bug
  Hunters and Cyber Crime Investigators to find deep information about their
  target.
   
  ReconSpider aggregate all the raw data, visualize it on a dashboard and
  facilitate alerting and monitoring on the data.
   
  Recon Spider also combines the capabilities of Wave, Photon and Recon Dog to
  do a comprehensive enumeration of attack surface.
   
  This package includes IP2Proxy LITE data available from
  https://www.ip2location.com/proxy-database.
 
 **Installed size:** `371.90 MB`  
 **How to install:** `sudo apt install reconspider`  
 
 {{< spoiler "Dependencies:" >}}
 * h8mail
 * python3
 * python3-bs4
 * python3-click
 * python3-gmplot
 * python3-ip2proxy
 * python3-lxml
 * python3-nmap
 * python3-paramiko
 * python3-pil
 * python3-prompt-toolkit
 * python3-pythonping
 * python3-requests
 * python3-shodan
 * python3-tweepy
 * python3-urllib3
 * python3-whois
 {{< /spoiler >}}
 
 ##### reconspider
 
 
 ```
 root@kali:~# reconspider -h
 
 __________                               _________       __     ___
 \______   \ ____   ____  ____   ____    /   _____/_____ |__| __| _/___________
  |       _// __ \_/ ___\/  _ \ /    \   \_____  \\____ \|  |/ __ |/ __ \_  __ \
  |    |   \  ___/\  \__(  <_> )   |  \  /        \  |_> >  / /_/ \  ___/|  | \/
  |____|_  /\___  >\___  >____/|___|  / /_______  /   __/|__\____ |\___  >__|
         \/     \/     \/           \/          \/|__|           \/    \/
 
 
 Seems like you haven't add your shodan API key in /etc/reconspider/reconspider.conf, Please add the missing API keys
 
 Add your ipstack api key to /etc/reconspider/reconspider.conf
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
