---
Title: gvm
Homepage: https://www.greenbone.net/
Repository: https://salsa.debian.org/pkg-security-team/gvm
Architectures: all
Version: 23.11.1
Metapackages: kali-linux-everything kali-tools-vulnerability 
Icon: images/gvm-logo.svg
PackagesInfo: |
 ### gvm
 
  The Greenbone Vulnerability Manager is a modular security auditing tool,
  used for testing remote systems for vulnerabilities that should be fixed.
   
  This package installs all the required packages. It provides scripts to setup,
  start and stop the GVM services.
   
  The tool was previously named OpenVAS.
 
 **Installed size:** `47 KB`  
 **How to install:** `sudo apt install gvm`  
 
 {{< spoiler "Dependencies:" >}}
 * gsad 
 * gvmd 
 * notus-scanner 
 * openvas-scanner 
 * ospd-openvas 
 * psmisc
 * rsync
 * xsltproc
 {{< /spoiler >}}
 
 ##### gvm-check-setup
 
 
 ```
 root@kali:~# gvm-check-setup -h
 gvm-check-setup 23.11.0
   Test completeness and readiness of GVM-23.11.0
 Step 1: Checking OpenVAS (Scanner)... 
         OK: OpenVAS Scanner is present in version 22.7.7.
         OK: Notus Scanner is present in version 22.6.2.
         OK: Server CA Certificate is present as /var/lib/gvm/CA/servercert.pem.
 Checking permissions of /var/lib/openvas/gnupg/*
         OK: _gvm owns all files in /var/lib/openvas/gnupg
         OK: redis-server is present.
         OK: scanner (db_address setting) is configured properly using the redis-server socket: /var/run/redis-openvas/redis-server.sock
         OK: the mqtt_server_uri is defined in /etc/openvas/openvas.conf
         OK: _gvm owns all files in /var/lib/openvas/plugins
         ERROR: The NVT collection is very small.
         FIX: Run the synchronization script greenbone-feed-sync.
         sudo greenbone-feed-sync --type nasl
 
  ERROR: Your GVM-23.11.0 installation is not yet complete!
 
 Please follow the instructions marked with FIX above and run this
 script again.
 
 ```
 
 - - -
 
 ##### gvm-feed-update
 
 
 ```
 root@kali:~# gvm-feed-update -h
 [>] This script is now deprecated
 [>] Please use 'sudo greenbone-feed-sync' instead
 ```
 
 - - -
 
 ##### gvm-setup
 
 
 ```
 root@kali:~# gvm-setup -h
 
 [>] Starting PostgreSQL service
 
 [>] Creating GVM's certificate files
 
 [>] Creating PostgreSQL database
 [i] User _gvm already exists in PostgreSQL
 [i] Database gvmd already exists in PostgreSQL
 [i] Role DBA already exists in PostgreSQL
 
 [*] Applying permissions
 GRANT ROLE
 [i] Extension uuid-ossp already exists for gvmd database
 [i] Extension pgcrypto already exists for gvmd database
 [i] Extension pg-gvm already exists for gvmd database
 [>] Migrating database
 [>] Checking for GVM admin user
 [*] Configure Feed Import Owner
 [*] Update GVM feeds
 Running as root. Switching to user '_gvm' and group '_gvm'.
 Trying to acquire lock on /var/lib/openvas/feed-update.lock
 Acquired lock on /var/lib/openvas/feed-update.lock
 ```
 
 - - -
 
 ##### gvm-start
 
 
 ```
 root@kali:~# gvm-start -h
 [>] Please wait for the GVM services to start.
 [>]
 [>] You might need to refresh your browser once it opens.
 [>]
 [>]  Web UI (Greenbone Security Assistant): https://127.0.0.1:9392
 
 ```
 
 - - -
 
 ##### gvm-stop
 
 
 ```
 root@kali:~# gvm-stop -h
 [>] Stopping GVM services
 * gsad.service - Greenbone Security Assistant daemon (gsad)
      Loaded: loaded (/lib/systemd/system/gsad.service; disabled; preset: disabled)
      Active: inactive (dead)
        Docs: man:gsad(8)
              https://www.greenbone.net
 
 * gvmd.service - Greenbone Vulnerability Manager daemon (gvmd)
      Loaded: loaded (/lib/systemd/system/gvmd.service; disabled; preset: disabled)
      Active: inactive (dead)
        Docs: man:gvmd(8)
 
 Dec 01 06:25:10 kali systemd[1]: Started gvmd.service - Greenbone Vulnerability Manager daemon (gvmd).
 Dec 01 06:25:23 kali systemd[1]: Stopping gvmd.service - Greenbone Vulnerability Manager daemon (gvmd)...
 Dec 01 06:25:23 kali systemd[1]: gvmd.service: Deactivated successfully.
 Dec 01 06:25:23 kali systemd[1]: Stopped gvmd.service - Greenbone Vulnerability Manager daemon (gvmd).
 Dec 01 09:28:02 kali systemd[1]: Starting gvmd.service - Greenbone Vulnerability Manager daemon (gvmd)...
 Dec 01 09:28:02 kali systemd[1]: gvmd.service: Can't open PID file /run/gvmd/gvmd.pid (yet?) after start: No such file or directory
 Dec 01 09:28:03 kali systemd[1]: Started gvmd.service - Greenbone Vulnerability Manager daemon (gvmd).
 Dec 01 09:28:16 kali systemd[1]: Stopping gvmd.service - Greenbone Vulnerability Manager daemon (gvmd)...
 Dec 01 09:28:16 kali systemd[1]: gvmd.service: Deactivated successfully.
 Dec 01 09:28:16 kali systemd[1]: Stopped gvmd.service - Greenbone Vulnerability Manager daemon (gvmd).
 
 * ospd-openvas.service - OSPd Wrapper for the OpenVAS Scanner (ospd-openvas)
      Loaded: loaded (/lib/systemd/system/ospd-openvas.service; disabled; preset: disabled)
      Active: inactive (dead)
        Docs: man:ospd-openvas(8)
              man:openvas(8)
 
 Dec 01 06:25:23 kali systemd[1]: Stopping ospd-openvas.service - OSPd Wrapper for the OpenVAS Scanner (ospd-openvas)...
 Dec 01 06:25:23 kali systemd[1]: ospd-openvas.service: Deactivated successfully.
 Dec 01 06:25:23 kali systemd[1]: Stopped ospd-openvas.service - OSPd Wrapper for the OpenVAS Scanner (ospd-openvas).
 Dec 01 06:25:23 kali systemd[1]: ospd-openvas.service: Consumed 1.509s CPU time.
 Dec 01 09:28:01 kali systemd[1]: Starting ospd-openvas.service - OSPd Wrapper for the OpenVAS Scanner (ospd-openvas)...
 Dec 01 09:28:02 kali systemd[1]: Started ospd-openvas.service - OSPd Wrapper for the OpenVAS Scanner (ospd-openvas).
 Dec 01 09:28:16 kali systemd[1]: Stopping ospd-openvas.service - OSPd Wrapper for the OpenVAS Scanner (ospd-openvas)...
 Dec 01 09:28:16 kali systemd[1]: ospd-openvas.service: Deactivated successfully.
 Dec 01 09:28:16 kali systemd[1]: Stopped ospd-openvas.service - OSPd Wrapper for the OpenVAS Scanner (ospd-openvas).
 Dec 01 09:28:16 kali systemd[1]: ospd-openvas.service: Consumed 1.144s CPU time.
 
 * notus-scanner.service - Notus Scanner
      Loaded: loaded (/lib/systemd/system/notus-scanner.service; disabled; preset: disabled)
      Active: inactive (dead)
        Docs: https://github.com/greenbone/notus-scanner
 
 Dec 01 06:25:08 kali systemd[1]: Starting notus-scanner.service - Notus Scanner...
 Dec 01 06:25:09 kali systemd[1]: Started notus-scanner.service - Notus Scanner.
 Dec 01 06:25:23 kali systemd[1]: Stopping notus-scanner.service - Notus Scanner...
 Dec 01 06:25:23 kali systemd[1]: notus-scanner.service: Deactivated successfully.
 Dec 01 06:25:23 kali systemd[1]: Stopped notus-scanner.service - Notus Scanner.
 Dec 01 09:28:01 kali systemd[1]: Starting notus-scanner.service - Notus Scanner...
 Dec 01 09:28:02 kali systemd[1]: Started notus-scanner.service - Notus Scanner.
 Dec 01 09:28:16 kali systemd[1]: Stopping notus-scanner.service - Notus Scanner...
 Dec 01 09:28:16 kali systemd[1]: notus-scanner.service: Deactivated successfully.
 Dec 01 09:28:16 kali systemd[1]: Stopped notus-scanner.service - Notus Scanner.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

![gvm](images/openvas.png)
