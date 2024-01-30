---
Title: blue-hydra
Homepage: https://github.com/ZeroChaos-/blue_hydra
Repository: https://gitlab.com/kalilinux/packages/blue-hydra
Architectures: any
Version: 1.9.17-0kali6
Metapackages: kali-linux-everything kali-tools-bluetooth kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### blue-hydra
 
  BlueHydra is a Bluetooth device discovery service built on top of
  the bluez library. BlueHydra makes use of ubertooth where available
  and attempts to track both classic and low energy (LE) bluetooth devices
  over time.
 
 **Installed size:** `8.23 MB`  
 **How to install:** `sudo apt install blue-hydra`  
 
 {{< spoiler "Dependencies:" >}}
 * bluez-test-scripts
 * libc6 
 * libruby3.1 
 * libsqlite3-0 
 * python3
 * ruby 
 {{< /spoiler >}}
 
 ##### blue_hydra
 
 
 ```
 root@kali:~# blue_hydra -h
 Usage: BlueHydra [options]
     -d, --daemonize                  Suppress output and run in daemon mode
     -z, --demo                       Hide mac addresses in CLI UI
     -p, --pulse                      Send results to hermes
         --pulse-debug                Store results in a file for review
         --no-db                      Keep db in ram only
         --rssi-api                   Open 127.0.0.1:1124 to allow other processes to poll for seen devices and rssi
         --no-info                    For the purposes for fox hunting, don't info scan.  Some info may be missing, but there will be less gaps during tracking
         --mohawk-api                 For the purposes of making a hat to cover a mohawk, shit out the ui as json at /dev/shm/blue_hydra.json
     -v, --version                    Show version and quit
     -h, --help                       Show this message
 ```
 
 - - -
 
 ##### rfkill-reset
 
 
 ```
 root@kali:~# rfkill-reset --help
 rfkill error: rfkill: invalid option -- 'E'
 Try 'rfkill --help' for more information.
 Unable to automagically fix
 ```
 
 - - -
 
 ##### test-discovery
 
 
 ```
 root@kali:~# test-discovery -h
 Usage: test-discovery [options]
 
 Options:
   -i DEV_ID, --device=DEV_ID
   -t TIMEOUT, --timeout=TIMEOUT
   -h, --help            show this help message and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
