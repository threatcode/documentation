---
Title: rtlsdr-scanner
Homepage: https://github.com/CdeMills/RTLSDR-Scanner
Repository: https://gitlab.com/kalilinux/packages/rtlsdr-scanner
Architectures: all
Version: 1:1.3.2+git20210822-0kali2
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rtlsdr-scanner
 
  A cross platform Python frequency scanning GUI for the OsmoSDR rtl-sdr library.
   
  The scanner attempts to overcome the tuner's frequency response by averaging
  scans from both the positive and negative frequency offsets of the baseband
  data.
 
 **Installed size:** `2.46 MB`  
 **How to install:** `sudo apt install rtlsdr-scanner`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-ipdb
 * python3-matplotlib
 * python3-numpy
 * python3-pil
 * python3-rtlsdr
 * python3-serial
 * python3-visvis
 * python3-wxgtk4.0
 {{< /spoiler >}}
 
 ##### rtlsdr-scanner
 
 
 ```
 root@kali:~# rtlsdr-scanner -h
 RTLSDR Scanner
 
 usage: rtlsdr_scan.py [-h] [-s START] [-e END] [-w SWEEPS] [-p DELAY]
                       [-g GAIN] [-d DWELL] [-f FFT] [-l LO] [-c CONF]
                       [-i INDEX | -r REMOTE]
                       [file]
 
 Scan a range of frequencies and save the results to a file
 
 positional arguments:
   file                  Output file (.rfs.csv, .plt, .m or .sdb2)
 
 options:
   -h, --help            show this help message and exit
   -s START, --start START
                         Start frequency (MHz)
   -e END, --end END     End frequency (MHz)
   -w SWEEPS, --sweeps SWEEPS
                         Number of sweeps
   -p DELAY, --delay DELAY
                         Delay between sweeps (s)
   -g GAIN, --gain GAIN  Gain (dB)
   -d DWELL, --dwell DWELL
                         Dwell time (seconds)
   -f FFT, --fft FFT     FFT bins
   -l LO, --lo LO        Local oscillator offset
   -c CONF, --conf CONF  Load a config file
   -i INDEX, --index INDEX
                         Device index (from 0)
   -r REMOTE, --remote REMOTE
                         Server IP and port
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
rtlsdr-scanner
```

![rtlsdr-scanner](images/rtlsdr-scanner.png)
