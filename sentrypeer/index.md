---
Title: sentrypeer
Homepage: https://sentrypeer.org
Repository: https://gitlab.com/kalilinux/packages/sentrypeer
Architectures: amd64 arm64
Version: 3.0.0-0kali2
Metapackages: kali-linux-everything kali-tools-detect 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sentrypeer
 
  SentryPeer is a distributed list of bad IP addresses and phone numbers
  collected via a SIP Honeypot.
  SentryPeer is a fraud detection tool. It lets bad actors try to make phone
  calls and saves the IP address they came from and number they tried to call.
  Those details can then be used to raise notifications at the service providers
  network and the next time a user/customer tries to call a collected number,
  you can act anyway you see fit.
   
  Traditionally this data is shipped to a central place, so you don't own
  the data you've collected. This project is all about Peer to Peer sharing
  of that data. The user owning the data and various Service Provider /
  Network Provider related feeds of the data is the key bit for me. I'm
  sick of all the services out there that keep it and sell it. If you've
  collected it, you should have the choice to keep it and/or opt in to
  share it with other SentryPeer community members via p2p methods.
 
 **Installed size:** `103 KB`  
 **How to install:** `sudo apt install sentrypeer`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * libcurl4 
 * libjansson4 
 * libmicrohttpd12 
 * libosip2-15 
 * libpcre2-8-0 
 * libsqlite3-0 
 * libuuid1 
 {{< /spoiler >}}
 
 ##### sentrypeer
 
 A distributed list of bad IP addresses and phone numbers collected via a SIP Honeypot
 
 ```
 root@kali:~# sentrypeer -h
 Usage: sentrypeer [-h] [-V] [-w https://api.example.com/events] [-j] [-p] [-b bootstrap.example.com] [-i OAuth_2_Client_ID] [-c OAuth_2_Client_Secret] [-f fullpath for sentrypeer.db] [-l fullpath for sentrypeer_json.log] [-r] [-R] [-a] [-s] [-v] [-d]
 
 Options:
   -h,      Print this help
   -V,      Print version
   -f,      Set 'sentrypeer.db' location or use SENTRYPEER_DB_FILE env
   -j,      Enable json logging or use SENTRYPEER_JSON_LOG env
   -p,      Enable Peer to Peer mode or use SENTRYPEER_PEER_TO_PEER env
   -b,      Set Peer to Peer bootstrap node or use SENTRYPEER_BOOTSTRAP_NODE env
   -i,      Set OAuth 2 client ID or use SENTRYPEER_OAUTH2_CLIENT_ID env to get a Bearer token for WebHook
   -c,      Set OAuth 2 client secret or use SENTRYPEER_OAUTH2_CLIENT_SECRET env to get a Bearer token for WebHook
   -a,      Enable RESTful API mode or use SENTRYPEER_API env
   -w,      Set WebHook URL for bad actor json POSTs or use SENTRYPEER_WEBHOOK_URL env
   -r,      Enable SIP responsive mode or use SENTRYPEER_SIP_RESPONSIVE env
   -R,      Disable SIP mode completely or use SENTRYPEER_SIP_DISABLE env
   -l,      Set 'sentrypeer_json.log' location or use SENTRYPEER_JSON_LOG_FILE env
   -s,      Enable syslog logging or use SENTRYPEER_SYSLOG env
   -v,      Enable verbose logging or use SENTRYPEER_VERBOSE env
   -d,      Enable debug mode or use SENTRYPEER_DEBUG env
 
 Report bugs to https://github.com/SentryPeer/SentryPeer/issues
 
 See https://sentrypeer.org for more information.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
