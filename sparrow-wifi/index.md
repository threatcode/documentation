---
Title: sparrow-wifi
Homepage: https://github.com/ghostop14/sparrow-wifi
Repository: https://gitlab.com/kalilinux/packages/sparrow-wifi
Architectures: all
Version: 0.0~git20230403-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sparrow-wifi
 
  This package contains a gaphical Wi-Fi analyser for Linux. It provides a more
  comprehensive GUI-based replacement for tools like inSSIDer and linssid that
  runs specifically on Linux. In its most comprehensive use cases, sparrow-wifi
  integrates Wi-Fi, software-defined radio (hackrf), advanced bluetooth tools
  (traditional and Ubertooth), traditional GPS (via gpsd), and drone/rover GPS
  via mavlink in one solution.
 
 **Installed size:** `1.88 MB`  
 **How to install:** `sudo apt install sparrow-wifi`  
 
 {{< spoiler "Dependencies:" >}}
 * gpsd
 * gpsd-clients
 * python3
 * python3-dateutil
 * python3-dronekit
 * python3-gps3
 * python3-manuf
 * python3-matplotlib
 * python3-numpy
 * python3-pyqt5.qsci
 * python3-pyqt5.qtchart
 * python3-requests
 * python3-tk
 * usbutils
 * wireless-tools
 {{< /spoiler >}}
 
 ##### sparrow-wifi
 
 
 
 - - -
 
 ##### sparrowwifiagent
 
 
 ```
 root@kali:~# sparrowwifiagent -h
 usage: sparrowwifiagent.py [-h] [--port PORT] [--allowedips ALLOWEDIPS]
                            [--staticcoord STATICCOORD]
                            [--mavlinkgps MAVLINKGPS] [--sendannounce]
                            [--userpileds] [--recordinterface RECORDINTERFACE]
                            [--ignorecfg] [--cfgfile CFGFILE] [--allowcors]
                            [--delaystart DELAYSTART] [--debughttp]
 
 Sparrow-wifi agent
 
 options:
   -h, --help            show this help message and exit
   --port PORT           Port for HTTP server to listen on. Default is 8020.
   --allowedips ALLOWEDIPS
                         IP addresses allowed to connect to this agent. Default
                         is any. This can be a comma-separated list for
                         multiple IP addresses
   --staticcoord STATICCOORD
                         Use user-defined lat,long,altitude(m) rather than GPS.
                         Ex: 40.1,-75.3,150
   --mavlinkgps MAVLINKGPS
                         Use Mavlink (drone) for GPS. Options are: '3dr' for a
                         Solo, 'sitl' for local simulator, or full connection
                         string ('udp/tcp:<ip>:<port>' such as:
                         'udp:10.1.1.10:14550')
   --sendannounce        Send a UDP broadcast packet on the specified port to
                         announce presence
   --userpileds          Use RPi LEDs to signal state. Red=GPS
                         [off=None,blinking=Unsynchronized,solid=synchronized],
                         Green=Agent Running [On=Running, blinking=servicing
                         HTTP request]
   --recordinterface RECORDINTERFACE
                         Automatically start recording locally with the given
                         wireless interface (headless mode) in a recordings
                         directory
   --ignorecfg           Don't load any config files (useful for overriding
                         and/or testing)
   --cfgfile CFGFILE     Use the specified config file rather than the default
                         sparrowwifiagent.cfg file
   --allowcors           Allow Cross Domain Resource Sharing
   --delaystart DELAYSTART
                         Wait <delaystart> seconds before initializing
   --debughttp           Print each URL request
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
