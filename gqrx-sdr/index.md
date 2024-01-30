---
Title: gqrx-sdr
Homepage: http://gqrx.dk/
Repository: https://salsa.debian.org/bottoms/pkg-gqrx-sdr
Architectures: any
Version: 2.17.3-1
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gqrx-sdr
 
  Gqrx works with hardware supported by gr-osmosdr, including Funcube
  Dongle, RTL-SDR, Airspy, HackRF, BladeRF, RFSpace, USRP and SoapySDR.
   
  Gqrx can operate as an AM/FM/SSB receiver with audio output or as an
  FFT-only instrument. The built-in Gqrx AFSK1200 decoder can decode
  and display AX.25 packets.  There are also various hooks for
  interacting with external applications using network sockets.
   
  Wideband FM mode has mono, stereo, and RDS (Radio Data System) modes.
  Displays FFT plot and spectrum waterfall.
   
  It is powered by GNU Radio and the Qt GUI toolkit.
 
 **Installed size:** `2.20 MB`  
 **How to install:** `sudo apt install gqrx-sdr`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgnuradio-analog3.10.8 
 * libgnuradio-blocks3.10.8 
 * libgnuradio-digital3.10.8 
 * libgnuradio-fft3.10.8 
 * libgnuradio-filter3.10.8 
 * libgnuradio-network3.10.8 
 * libgnuradio-osmosdr0.2.0 
 * libgnuradio-pmt3.10.8 
 * libgnuradio-runtime3.10.8 
 * libpulse0 
 * libqt6core6 
 * libqt6gui6 
 * libqt6network6 
 * libqt6svgwidgets6 
 * libqt6widgets6 
 * libstdc++6 
 * libvolk3.0 
 {{< /spoiler >}}
 
 ##### gqrx
 
 Software Defined Radio GUI application
 
 ```
 root@kali:~# man gqrx
 GQRX(1)                          User Commands                         GQRX(1)
 
 NAME
        gqrx - Software Defined Radio GUI application
 
 DESCRIPTION
        Gqrx  is  a software defined radio (SDR) receiver implemented using GNU
        Radio and the Qt GUI toolkit. It works with hardware supported  by  gr-
        osmosdr,  including  Funcube  Dongle, RTL-SDR, Airspy, HackRF, BladeRF,
        RFSpace, USRP and SoapySDR.
 
        Gqrx can operate as an AM/FM/SSB receiver with audio output  or  as  an
        FFT-only  instrument. There are also various hooks for interacting with
        external applications using network sockets.
 
        It is strongly recommended to run the volk_profile utility before  run-
        ning gqrx. This will detect and enable processor-specific optimisations
        and will in many cases give a significant performance boost.
 
        The  first time you start gqrx it will open a device configuration dia-
        log.  Supported devices that are connected to the computer are  discov-
        ered  automatically  and  you  can  select any of them in the drop-down
        list.
 
        If you don't see your device listed in the drop-down list it  could  be
        because:
 
        o      The driver has not been included in a binary distribution
 
        o      The udev rule has not been properly configured
 
        o      Linux kernel driver is blocking access to the device
 
        You can test your device using device specific tools, such as rtl_test,
        airspy_rx, hackrf_transfer, qthid, etc.
 
        Gqrx  supports multiple configurations and sessions if you have several
        devices or if you want to use the same device under different  configu-
        rations. You can load a configuration from the GUI or using the -c com-
        mand line argument.
 
 OPTIONS
        -h, --help
               Display the help page
 
        -s, --style style
               Use the given style (fusion, windows)
 
        -l, --list
               List existing configurations
 
        -c, --conf file
               Start with a specific configuration file
 
        -e, --edit
               Edit the configuration file before using it
 
        -r, --reset
               Reset the configuration file
 
 SEE ALSO
        https://gqrx.dk/
 
 gqrx 2.17.3                    October 20, 2023                        GQRX(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
