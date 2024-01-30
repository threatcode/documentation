---
Title: gr-osmosdr
Homepage: http://sdr.osmocom.org/trac/wiki/GrOsmoSDR
Repository: https://salsa.debian.org/bottoms/pkg-gr-osmosdr
Architectures: any
Version: 0.2.4-1
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gr-osmosdr
 
  The Osmocom project is a family of projects regarding Open source
  mobile communications.
   
  While primarily being developed for the OsmoSDR hardware, this block
  as well supports:
   - FUNcube Dongle through gr-funcube
   - FUNcube Dongle Pro+ through gr-funcube
   - RTL2832U based DVB-T dongles through librtlsdr
   - RTL-TCP spectrum server (see librtlsdr project)
   - gnuradio .cfile input through libgnuradio-blocks
   - RFSPACE SDR-IQ, SDR-IP, NetSDR (incl. X2 option)
   - Great Scott Gadgets HackRF through libhackrf
   - Nuand LLC bladeRF through libbladeRF library
   - Ettus USRP Devices through Ettus UHD library
   - Fairwaves UmTRX through Fairwaves' fork of UHD
   - AIRSPY Receiver
   - AIRSPY HF+ Receiver
   - SoapySDR support
   - Red Pitaya SDR transceiver (http://bazaar.redpitaya.com)
   - FreeSRP through libfreesrp
   
  Example applications include osmocom_fft, osmocom_siggen,
  and osmocom_spectrum_sense.
   
  By using the OsmoSDR block you can take advantage of a common
  software API in your application(s) independent of the underlying
  radio hardware. This package provides C++ header files,
  documentation, and Python3 wrappers to the library.
 
 **Installed size:** `8.20 MB`  
 **How to install:** `sudo apt install gr-osmosdr`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgnuradio-osmosdr0.2.0 
 * libgnuradio-runtime3.10.8 
 * libstdc++6 
 * python3
 * python3 
 * python3-numpy 
 * python3-numpy-abi9
 {{< /spoiler >}}
 
 ##### osmocom_fft
 
 Spectrum Browser
 
 ```
 root@kali:~# man osmocom_fft
 osmocom_fft(1)                   User Commands                  osmocom_fft(1)
 
 NAME
        osmocom_fft - Spectrum Browser
 
 SYNOPSIS
        osmocom_fft [options]
 
 DESCRIPTION
        Spectrum Browser
 
 OPTIONS
        -h, --help
               show this help message and exit
 
        -a ARGS, --args=ARGS
               Device args, [default=]
 
        -A ANTENNA, --antenna=ANTENNA
               Select RX antenna where appropriate
 
        -s SAMP_RATE, --samp-rate=SAMP_RATE
               Set sample rate (bandwidth), minimum by default
 
        -f FREQ, --center-freq=FREQ
               Set frequency to FREQ
 
        -c FREQ_CORR, --freq-corr=FREQ_CORR
               Set frequency correction (ppm)
 
        -g GAIN, --gain=GAIN
               Set gain in dB (default is midpoint)
 
        -W, --waterfall
               Enable waterfall display
 
        -S, --oscilloscope
               Enable oscilloscope display
 
        --avg-alpha=AVG_ALPHA
               Set fftsink averaging factor, default=[0.1]
 
        --averaging
               Enable fftsink averaging, default=[False]
 
        --ref-scale=REF_SCALE
               Set dBFS=0dB input value, default=[1.0]
 
        --fft-size=FFT_SIZE
               Set number of FFT bins [default=1024]
 
        --fft-rate=FFT_RATE
               Set FFT update rate, [default=30]
 
        -v, --verbose
               Use verbose console output [default=False]
 
 SEE ALSO
        The  full  documentation  for linux; is maintained as a Texinfo manual.
        If the info and linux; programs are properly installed  at  your  site,
        the command
 
               info linux;
 
        should give you access to the complete manual.
 
 Device specification
        You  can  specify  the  source  or  sink device using a comma separated
        string of argument=value pairs. The always-up-to-date block  documenta-
        tion with examples is available right here.
 
 FCD Source
        Argument
               Notes
 
        fcd=<device-index>
               0-based device identifier, optional
 
        device=hw:2
               overrides the audio device
 
        type=2 selects the dongle type, 1 for Classic, 2 for Pro+
 
        The "device" argument overrides the audio device used by the underlying
        driver to access the dongle's IQ sample stream.
 
        The "type" argument selects the dongle type, 1 for Classic, 2 for Pro+.
 
 OsmoSDR Source
        Argument
               Notes
 
        osmosdr=<device-index>
               0-based device identifier
 
        buffers=<number-of-buffers>
               Default is 32
 
        buflen=<length-of-buffer>
               Default is 256kB, must be multiple of 512
 
 RTL-SDR Source
        Argument
               Notes
 
        rtl=<device-index>
               0-based device identifier OR serial number
 
        rtl_xtal=<frequency>
               Frequency (Hz) used for the RTL chip, accepts eng notation
 
        tuner_xtal=<frequency>
               Frequency (Hz) used for the tuner chip, accepts eng notation
 
        buffers=<number-of-buffers>
               Default is 32
 
        buflen=<length-of-buffer>
               Default is 256kB, must be multiple of 512
 
        direct_samp=0|1|2
               Enable  direct sampling mode on the RTL chip. 0: Disable, 1: use
               I channel, 2: use Q channel
 
        offset_tune=0|1
               Enable offset tune mode for E4000 tuners
 
        NOTE: use rtl_eeprom -s to program your own serial number to the device
 
        NOTE: if you don't specify rtl_xtal/tuner_xtal, the  underlying  driver
        will use 28.0MHz
 
 RTL-SDR TCP Source
        Argument
               Notes
 
        rtl_tcp=<hostname>:<port>
               hostname defaults to "localhost", port to "1234"
 
        psize=<payload-size>
               Default is 16384 bytes
 
        direct_samp=0|1|2
               Enable direct sampling mode on the RTL chip 0=Off, 1=I-ADC input
               enabled, 2=Q-ADC input enabled
 
        offset_tune=0|1
               Enable offset tune mode for E4000 tuners
 
 Miri Source
        Argument
               Notes
 
        miri=<device-index>
               0-based device identifier
 
        buffers=<number-of-buffers>
               Default is 32
 
 UHD Source / Sink
        Argument Notes
 
        uhd    Use this argument without a value
 
        nchan=<channel-count>
               For multichannel USRP configurations use the subdev parameter to
               specify stream mapping
 
        subdev=<subdev-spec>
               Examples:  "A:0",  "B:0", "A:0 B:0" when nchan=2. Refer original
               ettus documentation on this
 
        lo_offset=<frequency>
               Offset frequency in Hz, must be within daughterboard  bandwidth.
               Accepts eng notation
 
        Additional  argument/value  pairs will be passed to the underlying dri-
        ver, for more information see specifying the subdevice and  common  de-
        vice identifiers in the Ettus documentation.
 
 bladeRF Source / Sink
        Argument
               Notes
 
        bladerf[=0]
               0-based device identifier (optional)
 
        fw='/path/to/the/firmware.img'
               program  MCU firmware from given file. usually not needed. power
               cycle required.
 
        fpga='/path/to/the/bitstream.rbf'
               load FPGA bitstream from given file. required only at first  run
               at the moment.
 
 HackRF Source / Sink
        Argument
               Notes
 
        hackrf Use this argument without a value
 
        buffers=<number-of-buffers>
               Default is 32
 
        Only  the  first device found may be used at the moment because of lib-
        hackrf limitation.
 
        Transmit support has been verified by using the  crc-mmbTools  DAB  sdr
        transmitter.
 
 IQ File Source
        Argument
               Notes
 
        file=<path-to-file-name>
 
        freq=<frequency>
               Center frequency in Hz, accepts eng notation
 
        rate=<sampling-rate>
               Mandatory, in samples/s, accepts eng notation
 
        repeat=true|false
               Default is true
 
        throttle=true|false
               Throttle flow of samples, default is true
 
 EXAMPLES
        osmocom_fft -a rtl=0 -v -f 100e6 -s 2.4e6 -g 15
 
        osmocom_fft -a hackrf -v
 
        osmocom_fft -a uhd -v
 
 SEE ALSO
        osmocom_siggen(1) osmocom_siggen_nogui(1) osmocom_spectrum_sense(1)
 
 OSMOCOM                          October 2013                   osmocom_fft(1)
 ```
 
 - - -
 
 ##### osmocom_siggen_nogui
 
 Signal generator application
 
 ```
 root@kali:~# osmocom_siggen_nogui -h
 Usage: osmocom_siggen_nogui: [options]
 
 Options:
   -h, --help            show this help message and exit
   -a ARGS, --args=ARGS  Device args, [default=]
   -A ANTENNA, --antenna=ANTENNA
                         Select Rx Antenna where appropriate
   --clock-source=CLOCK_SOURCE
                         Set the clock source; typically 'internal',
                         'external', 'external_1pps', 'mimo' or 'gpsdo'
   -s SAMP_RATE, --samp-rate=SAMP_RATE
                         Set sample rate (bandwidth), minimum by default
   -g GAIN, --gain=GAIN  Set gain in dB (default is midpoint)
   -G GAINS, --gains=GAINS
                         Set named gain in dB, name:gain,name:gain,...
   -f FREQ, --tx-freq=FREQ
                         Set carrier frequency to FREQ [default=mid-point]
   -c FREQ_CORR, --freq-corr=FREQ_CORR
                         Set carrier frequency correction [default=0]
   -x WAVEFORM_FREQ, --waveform-freq=WAVEFORM_FREQ
                         Set baseband waveform frequency to FREQ [default=0]
   -y WAVEFORM2_FREQ, --waveform2-freq=WAVEFORM2_FREQ
                         Set 2nd waveform frequency to FREQ [default=none]
   --sine                Generate a carrier modulated by a complex sine wave
   --const               Generate a constant carrier
   --offset=OFFSET       Set waveform phase offset to OFFSET [default=0]
   --gaussian            Generate Gaussian random output
   --uniform             Generate Uniform random output
   --2tone               Generate Two Tone signal for IMD testing
   --sweep               Generate a swept sine wave
   --gsm                 Generate GMSK modulated GSM Burst Sequence
   --amplitude=AMPL      Set output amplitude to AMPL (0.1-1.0) [default=0.3]
   -v, --verbose         Use verbose console output [default=False]
 ```
 
 - - -
 
 ### libgnuradio-osmosdr0.2.0
 
  The Osmocom project is a family of projects regarding Open source
  mobile communications. This library provides hardware support for
  a variety of radio hardware in the form of gnuradio blocks.
   
  This package contains the shared library.
 
 **Installed size:** `1.12 MB`  
 **How to install:** `sudo apt install libgnuradio-osmosdr0.2.0`  
 
 {{< spoiler "Dependencies:" >}}
 * libairspy0 
 * libairspyhf1 
 * libbladerf2 
 * libboost-chrono1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libfreesrp0
 * libgcc-s1 
 * libgnuradio-blocks3.10.8 
 * libgnuradio-funcube3.10.0 
 * libgnuradio-iqbalance3.9.0 
 * libgnuradio-pmt3.10.8 
 * libgnuradio-runtime3.10.8 
 * libgnuradio-uhd3.10.8 
 * libhackrf0 
 * librtlsdr0 
 * libsoapysdr0.8 
 * libstdc++6 
 * libuhd4.5.0 
 * libvolk3.0 
 * libxtrx0 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
