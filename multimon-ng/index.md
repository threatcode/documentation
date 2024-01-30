---
Title: multimon-ng
Homepage: https://github.com/EliasOenal/multimon-ng/
Repository: https://salsa.debian.org/debian-hamradio-team/multimon-ng
Architectures: any
Version: 1.3.0+dfsg-1
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### multimon-ng
 
  The successor to multimon, with support for more modes and improved
  compatibility with moderns systems. It decodes the following digital
  transmission modes commonly found on VHF/UHF bands:
   
    POCSAG512 POCSAG1200 POCSAG2400
    FLEX
    EAS
    UFSK1200 CLIPFSK AFSK1200 AFSK2400 AFSK2400_2 AFSK2400_3
    HAPN4800
    FSK9600
    DTMF
    ZVEI1 ZVEI2 ZVEI3 DZVEI PZVEI
    EEA EIA CCIR
    MORSE CW
    X10
   
  Multiple decoders can run concurrently on the same signal, which is
  provided via a file or a pipe. Common setups are: a radio connected
  via a sound card (may require modifications to the radio); samples
  provided via a GNU Radio sink or the UDP audio stream in gqrx (via
  netcat and sox).
 
 **Installed size:** `138 KB`  
 **How to install:** `sudo apt install multimon-ng`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpulse0 
 * libx11-6
 {{< /spoiler >}}
 
 ##### multimon-ng
 
 Program to decode radio transmissions
 
 ```
 root@kali:~# multimon-ng --help
 multimon-ng: unrecognized option '--help'
 multimon-ng 1.3.0
   (C) 1996/1997 by Tom Sailer HB9JNX/AE4WA
   (C) 2012-2023 by Elias Oenal
 Available demodulators: POCSAG512 POCSAG1200 POCSAG2400 FLEX FLEX_NEXT EAS UFSK1200 CLIPFSK FMSFSK AFSK1200 AFSK2400 AFSK2400_2 AFSK2400_3 HAPN4800 FSK9600 DTMF ZVEI1 ZVEI2 ZVEI3 DZVEI PZVEI EEA EIA CCIR MORSE_CW DUMPCSV X10 SCOPE
 
 Usage: multimon-ng [file] [file] [file] ...
   If no [file] is given, input will be read from your default sound
   hardware. A filename of "-" denotes standard input.
   -t <type>  : Input file type (any other type than raw requires sox)
   -a <demod> : Add demodulator
   -s <demod> : Subtract demodulator
   -c         : Remove all demodulators (must be added with -a <demod>)
   -q         : Quiet
   -v <level> : Level of verbosity (e.g. '-v 3')
                For POCSAG and MORSE_CW '-v1' prints decoding statistics.
   -h         : This help
   -A         : APRS mode (TNC2 text output)
   -m         : Mute SoX warnings
   -r         : Call SoX in repeatable mode (e.g. fixed random seed for dithering)
   -n         : Don't flush stdout, increases performance.
   -j         : FMS: Just output hex data and CRC, no parsing.
   -e         : POCSAG: Hide empty messages.
   -u         : POCSAG: Heuristically prune unlikely decodes.
   -i         : POCSAG: Inverts the input samples. Try this if decoding fails.
   -p         : POCSAG: Show partially received messages.
   -f <mode>  : POCSAG: Overrides standards and forces decoding of data as <mode>
                        (<mode> can be 'numeric', 'alpha', 'skyper' or 'auto')
   -b <level> : POCSAG: BCH bit error correction level. Set 0 to disable, default is 2.
                        Lower levels increase performance and lower false positives.
   -C <cs>    : POCSAG: Set Charset.
   -o         : CW: Set threshold for dit detection (default: 500)
   -d         : CW: Dit length in ms (default: 50)
   -g         : CW: Gap length in ms (default: 50)
   -x         : CW: Disable auto threshold detection
   -y         : CW: Disable auto timing detection
   --timestamp: Add a time stamp in front of every printed line
   --label    : Add a label to the front of every printed line
    Raw input requires one channel, 16 bit, signed integer (platform-native)
    samples at the demodulator's input sampling rate, which is
    usually 22050 Hz. Raw input is assumed and required if piped input is used.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}


## multimon-ng Usage Example

Take raw input from rtl_fm (`-t raw`), add the POCSAG512, POCSAG1200, POCSAG2400, and SCOPE modules (`-a POCSAG512 -a POCSAG1200 -a POCSAG2400 -a SCOPE`), decode in alpha mode (`-f alpha`), reading from stdin (`/dev/stdin`):

```
root@kali:~# rtl_fm -f 149.614M -s 22050 -p -19 | multimon-ng -t raw -a POCSAG512 -a POCSAG1200 -a POCSAG2400 -a SCOPE -f alpha /dev/stdin
multimon-ng  (C) 1996/1997 by Tom Sailer HB9JNX/AE4WA
             (C) 2012/2013 by Elias Oenal
available demodulators: POCSAG512 POCSAG1200 POCSAG2400 EAS UFSK1200 CLIPFSK AFSK1200 AFSK2400 AFSK2400_2 AFSK2400_3 HAPN4800 FSK9600 DTMF ZVEI1 ZVEI2 ZVEI3 DZVEI PZVEI EEA EIA CCIR SCOPE
Enabled demodulators: POCSAG512 POCSAG1200 POCSAG2400 SCOPE
Found 1 device(s):
  0:  Realtek, RTL2838UHIDIR, SN: 00000001

Using device 0: ezcap USB 2.0 DVB-T/DAB/FM dongle
Found Rafael Micro R820T tuner
Oversampling input by: 46x.
Oversampling output by: 1x.
Buffer size: 8.08ms
Tuned to 149867575 Hz.
Sampling at 1014300 Hz.
Output at 22050 Hz.
Exact sample rate is: 1014300.020041 Hz
Tuner gain set to automatic.
```
