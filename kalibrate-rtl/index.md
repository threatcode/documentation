---
Title: kalibrate-rtl
Homepage: https://github.com/steve-m/kalibrate-rtl
Repository: https://gitlab.com/kalilinux/packages/kalibrate-rtl
Architectures: any
Version: 0.4.1+git20191125-0kali2
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### kalibrate-rtl
 
  Kalibrate, or kal, can scan for GSM base stations in a given frequency band and
  can use those GSM base stations to calculate the local oscillator frequency
  offset.
 
 **Installed size:** `61 KB`  
 **How to install:** `sudo apt install kalibrate-rtl`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfftw3-double3 
 * libgcc-s1 
 * librtlsdr0 
 * libstdc++6 
 * rtl-sdr
 {{< /spoiler >}}
 
 ##### kal
 
 
 ```
 root@kali:~# kal -h
 kalibrate v0.4.1-rtl, Copyright (c) 2010, Joshua Lackey
 modified for use with rtl-sdr devices, Copyright (c) 2012, Steve Markgraf
 Usage:
 	GSM Base Station Scan:
 		kal <-s band indicator> [options]
 
 	Clock Offset Calculation:
 		kal <-f frequency | -c channel> [options]
 
 Where options are:
 	-s	band to scan (GSM850, GSM-R, GSM900, EGSM, DCS, PCS)
 	-f	frequency of nearby GSM base station
 	-c	channel of nearby GSM base station
 	-b	band indicator (GSM850, GSM-R, GSM900, EGSM, DCS, PCS)
 	-g	gain in dB
 	-d	rtl-sdr device index
 	-e	initial frequency error in ppm
 	-E	manual frequency offset in hz
 	-v	verbose
 	-D	enable debug messages
 	-h	help
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## kal Usage Example

Scan for GSM base stations in the GSM-850 band (`-s GSM850`), then use channel 128 (`-c 128`) to get the frequency offset:

```
root@kali:~# kal -s GSM850
Found 1 device(s):
  0:  ezcap USB 2.0 DVB-T/DAB/FM dongle

Using device 0: ezcap USB 2.0 DVB-T/DAB/FM dongle
Found Rafael Micro R820T tuner
Exact sample rate is: 270833.002142 Hz
kal: Scanning for GSM-850 base stations.
GSM-850:
    chan: 128 (869.2MHz - 3.988kHz) power: 486634.32
    chan: 143 (872.2MHz - 3.760kHz) power: 56331.63

root@kali:~# kal -c 128
Found 1 device(s):
  0:  ezcap USB 2.0 DVB-T/DAB/FM dongle

Using device 0: ezcap USB 2.0 DVB-T/DAB/FM dongle
Found Rafael Micro R820T tuner
Exact sample rate is: 270833.002142 Hz
kal: Calculating clock frequency offset.
Using GSM-850 channel 128 (869.2MHz)
average     [min, max]  (range, stddev)
- 4.093kHz      [-4102, -4083]  (20, 5.314593)
overruns: 0
not found: 0
average absolute error: 4.709 ppm
```
