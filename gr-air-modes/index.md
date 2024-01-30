---
Title: gr-air-modes
Homepage: https://github.com/bistromath/gr-air-modes
Repository: https://salsa.debian.org/bottoms/pkg-gr-air-modes
Architectures: any
Version: 0.0.20210211-3
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gr-air-modes
 
  A software-defined radio receiver for Mode S
  transponder signals, including ADS-B reports from equipped aircraft.
   
  Multiple output formats are supported:
   * Raw (or minimally processed) output of packet data
   * Parsed text
   * SQLite database
   * KML for use with Google Earth
   * SBS-1-compatible output for use with e.g. PlanePlotter or Virtual
     Radar Server
   * FlightGear multiplayer interface for real-time display of traffic
     within the simulator
 
 **Installed size:** `389 KB`  
 **How to install:** `sudo apt install gr-air-modes`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgnuradio-air-modes1 
 * libgnuradio-runtime3.10.8 
 * libstdc++6 
 * python3
 * python3 
 * python3-numpy 
 * python3-numpy-abi9
 * python3-zmq
 {{< /spoiler >}}
 
 ##### modes_rx
 
 Gnuradio Mode-S/ADS-B receiver
 
 ```
 root@kali:~# modes_rx -h
 gr-air-modes warning: numpy+scipy not installed, FlightGear interface not supported
 Usage: modes_rx: [options]
 
 Options:
   -h, --help            show this help message and exit
   -l LOCATION, --location=LOCATION
                         GPS coordinates of receiving station in format
                         xx.xxxxx,xx.xxxxx
   -a REMOTE, --remote=REMOTE
                         specify additional servers from which to take data in
                         format tcp://x.x.x.x:y,tcp://....
   -n, --no-print        disable printing decoded packets to stdout
   -K KML, --kml=KML     filename for Google Earth KML output
   -P, --sbs1            open an SBS-1-compatible server on port 30003
   -m MULTIPLAYER, --multiplayer=MULTIPLAYER
                         FlightGear server to send aircraft data, in format
                         host:port
 
   Receiver setup options:
     -s SOURCE, --source=SOURCE
                         Choose source: uhd, osmocom, <filename>, or <ip:port>
                         [default=uhd]
     -t PORT, --tcp=PORT
                         Open a TCP server on this port to publish reports
     -R SUBDEV, --subdev=SUBDEV
                         select USRP Rx side A or B
     -A ANTENNA, --antenna=ANTENNA
                         select which antenna to use on daughterboard
     -D ARGS, --args=ARGS
                         arguments to pass to radio constructor
     -f FREQ, --freq=FREQ
                         set receive frequency in Hz [default=1090000000.0]
     -g dB, --gain=dB    set RF gain
     -r RATE, --rate=RATE
                         set sample rate [default=4000000.0]
     -T THRESHOLD, --threshold=THRESHOLD
                         set pulse detection threshold above noise in dB
                         [default=7.0]
     -p, --pmf           Use pulse matched filtering [default=True]
     -d, --dcblock       Use a DC blocking filter (best for HackRF Jawbreaker)
                         [default=False]
 ```
 
 - - -
 
 ### libgnuradio-air-modes1
 
  A software-defined radio receiver for Mode S
  transponder signals, including ADS-B reports from equipped aircraft.
   
  This package provides a shared library.
 
 **Installed size:** `104 KB`  
 **How to install:** `sudo apt install libgnuradio-air-modes1`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgnuradio-pmt3.10.8 
 * libgnuradio-runtime3.10.8 
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
