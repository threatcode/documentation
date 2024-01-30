---
Title: Dradis Community Edition
Homepage: https://dradis.com/ce/
Repository: https://gitlab.com/kalilinux/packages/dradis
Architectures: amd64
Version: 4.10.0-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-reporting 
Icon: images/dradis-logo.svg
PackagesInfo: |
 ### Dradis CE
 
 Dradis is a tool to help you simplify reporting and collaboration.

   - Spend more time testing and less time reporting
   - Ensure consistent quality across your assessments
   - Combine the output of your favorite scanners
 
  Dradis is an open-source project released in 2007 that has been refined for over a decade by security professionals around the world.
 
 
 **Installed size:** `594.34 MB`  
 **How to install:** `sudo apt install dradis`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * bundler
 * git
 * libc6 
 * libgcc-s1 
 * libpq5 
 * libruby3.1 
 * libstdc++6 
 * lsof
 * pwgen
 * ruby 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### dradis
 
 
 ```
 root@kali:~# dradis -h
 [i] Something is already using port: 3000/tcp
 COMMAND     PID   USER   FD   TYPE  DEVICE SIZE/OFF NODE NAME
 ruby3.1 2796705 dradis   14u  IPv6 1933002      0t0  TCP localhost:3000 (LISTEN)
 ruby3.1 2796705 dradis   15u  IPv4 1933003      0t0  TCP localhost:3000 (LISTEN)
 
 UID          PID    PPID  C STIME TTY      STAT   TIME CMD
 dradis   2796705       1 38 09:09 ?        Ssl    0:01 /usr/bin/ruby3.1 bin/rails server
 
 [*] Please wait for the Dradis service to start.
 [*]
 [*] You might need to refresh your browser once it opens.
 [*]
 [*]  Web UI: http://127.0.0.1:3000
 
 ```
 
 - - -
 
 ##### dradis-stop
 
 
 ```
 root@kali:~# dradis-stop -h
 * dradis.service - Dradis web application
      Loaded: loaded (/lib/systemd/system/dradis.service; disabled; preset: disabled)
      Active: inactive (dead)
 
 Dec 01 09:09:15 kali bundle[2796705]:         <internal:/usr/lib/ruby/vendor_ruby/rubygems/core_ext/kernel_require.rb>:38:in `require'
 Dec 01 09:09:15 kali bundle[2796705]:         <internal:/usr/lib/ruby/vendor_ruby/rubygems/core_ext/kernel_require.rb>:38:in `require'
 Dec 01 09:09:15 kali bundle[2796705]:         /usr/lib/dradis/ruby/3.1.0/gems/bootsnap-1.16.0/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:32:in `require'
 Dec 01 09:09:15 kali bundle[2796705]:         bin/rails:5:in `<main>'
 Dec 01 09:09:15 kali bundle[2796705]: [2023-12-01 09:09:15] INFO  going to shutdown ...
 Dec 01 09:09:15 kali bundle[2796705]: [2023-12-01 09:09:15] INFO  WEBrick::HTTPServer#start done.
 Dec 01 09:09:15 kali bundle[2796705]: Exiting
 Dec 01 09:09:16 kali systemd[1]: dradis.service: Deactivated successfully.
 Dec 01 09:09:16 kali systemd[1]: Stopped dradis.service - Dradis web application.
 Dec 01 09:09:16 kali systemd[1]: dradis.service: Consumed 2.005s CPU time.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}


```
service dradis start
```

## Screenshots

![Dradis login screen](images/dradis-01.png)
![Dradis dashboard](images/dradis-02.png)
![Dradis issue list](images/dradis-03.png)
![Dradis methodologies](images/dradis-04.png)
