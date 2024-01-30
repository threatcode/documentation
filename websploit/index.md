---
Title: websploit
Homepage: https://sourceforge.net/projects/websploit/
Repository: https://salsa.debian.org/pkg-security-team/websploit
Architectures: all
Version: 4.0.4-3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### websploit
 
  WebSploit is an open source project which is used to scan
  and analysis remote system in order to find various type of
  vulnerabilites. This tool is very powerful and supports
  multiple vulnerabilities.
 
 **Installed size:** `76 KB`  
 **How to install:** `sudo apt install websploit`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-requests
 * python3-scapy
 {{< /spoiler >}}
 
 ##### websploit
 
 Advanced MITM Framework
 
 ```
 root@kali:~# man websploit
 WEBSPLOIT(1)                General Commands Manual               WEBSPLOIT(1)
 
 NAME
        websploit - Advanced MITM Framework
 
 SYNOPSIS
        websploit
 
 DESCRIPTION
        Websploit is an automatic vulnerability assessment, web scanner and ex-
        ploiter  tool. It is python command line tool that is composed on modu-
        lar structure pretty similar to Metasploit. There are currently 7  mod-
        ules.  The command line does not accept any options. User just get into
        console  typing "websploit" as root and the prompt will change to this:
        wsf >
 
 OPTIONS
        wsf > help
               Shows all command you can type in the websploit console. Some of
               them are only aplicable when using a certain module.
 
        wsf > show
               Show Modules of Current Database
 
        wsf > use <module_name>
               Select Module For Use
 
        wsf > options
               Show Current Options Of Selected Module
 
        wsf > set <module_option>
               Once you had seen the options of the selected  module,  you  may
               use this command to define its desired value.
 
        wsf > back
               Exit current module
 
        wsf > update
               Disabled on Debian systems in order to avoid conflicts with apt-
               get.
 
        wsf > about
               Shows info about the author.
 
 EXAMPLES
        Here is a simple example on how to use scan_wifi module in order to
        hunt existing wifi networks.
 
        $wsf > scan_wifi > execute
        SSID              BSSID               CHANNEL   SIGNAL   BARS   SECURITY
        EDTSTAR_2350      1C-B0-44-38-98-49   11        89              WPA2
        JAZZTWE_aJpE      00-4A-77-4D-C4-CC   1         69       _      WPA1 WPA2
        RadioPatioA1985   74-9D-79-2A-47-60   11        57       _      WPA2
        MIWIFI_dsTp       EC-BE-ED-39-1A-D2   1         44       __     WPA2
        DabaduNet4434     78-84-B4-51-44-35   8         44       __     WPA2
        MyHomenet821      74-7D-79-52-2A-00   1         37       __     WPA2
 
                                                                   WEBSPLOIT(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## websploit Usage Example

```
root@kali:~# websploit
WARNING: No route found for IPv6 destination :: (no default route?)

     __          __  _               _       _ _
     \ \        / / | |             | |     (_) |
      \ \  /\  / /__| |__  ___ _ __ | | ___  _| |_
       \ \/  \/ / _ \ '_ \/ __| '_ \| |/ _ \| | __|
        \  /\  /  __/ |_) \__ \ |_) | | (_) | | |_
         \/  \/ \___|_.__/|___/ .__/|_|\___/|_|\__|
                              | |
                              |_|

        --=[WebSploit FrameWork
    +---**---==[Version :2.0.5 BETA
    +---**---==[Codename :We're Not Crying Wolf
    +---**---==[Available Modules : 19
        --=[Update Date : [r2.0.5-000 2.3.2014]



wsf > use web/dir_scanner
wsf:Dir_Scanner > set TARGET http://192.168.1.202
TARGET =>  192.168.1.202
wsf:Dir_Scanner > run
[*] Your Target : 192.168.1.202
[*]Loading Path List ... Please Wait ...
[index] ... [400 Bad Request]
[images] ... [400 Bad Request]
[download] ... [400 Bad Request]
[2006] ... [400 Bad Request]
[news] ... [400 Bad Request]
[crack] ... [400 Bad Request]
```
