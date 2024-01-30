---
Title: inspectrum
Homepage: https://github.com/miek/inspectrum
Repository: https://salsa.debian.org/debian-hamradio-team/inspectrum
Architectures: any
Version: 0.2.3-3
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### inspectrum
 
  inspectrum is a tool for analysing captured signals, primarily from
  software-defined radio receivers.
   
  inspectrum supports the following file types:
   *.sigmf-meta, *.sigmf-data - Signal Metadata Format (SigMF) recordings
   *.cf32, *.cfile - Complex 32-bit floating point (GNURadio, osmocom_fft)
   *.cf64 - Complex 64-bit floating point samples
   *.cs16 - Complex 16-bit signed integer (BladeRF)
   *.cs8 - Complex 8-bit signed integer (HackRF)
   *.cu8 - Complex 8-bit unsigned integer (RTL-SDR)
   *.f32 - Real 32-bit floating point samples
   *.f64 - Real 64-bit floating point samples (MATLAB)
   *.s16 - Real 16-bit signed integer samples
   *.s8 - Real 8-bit signed integer samples
   *.u8 - Real 8-bit unsigned integer samples
   
  Features:
   * Large (100GB+) file support
   * Spectrogram with zoom/pan
   * Plots of amplitude, frequency, phase and IQ samples
   * Cursors for measuring period, symbol rate and extracting symbols
   * Export of selected time period, filtered samples and demodulated data
 
 **Installed size:** `304 KB`  
 **How to install:** `sudo apt install inspectrum`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfftw3-single3 
 * libgcc-s1 
 * libliquid1 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5widgets5 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### inspectrum
 
 Tool for visualising captured radio signals
 
 ```
 root@kali:~# man inspectrum
 INSPECTRUM(1)                    User Commands                   INSPECTRUM(1)
 
 NAME
        inspectrum - tool for visualising captured radio signals
 
 DESCRIPTION
        inspectrum  is  a  tool  for analysing captured signals, primarily from
        software-defined radio receivers.
 
 OPTIONS
        -r rate
 
        Sample rate in Hz.
 
         file
 
        Currently inspectrum can only read  files  with  interleaved  (complex)
        32-bit floats, such as those produced by GNURadio or osmocom_fft.
 
 FEATURES
        Spectrogram with zoom/pan
 
        Large (multi-gigabyte) file support
 
 CONTACT
        #inspectrum on freenode IRC
 
 SEE ALSO
        osmocom-fft(1)
 
 INSPECTRUM                         Oct 2015                      INSPECTRUM(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
