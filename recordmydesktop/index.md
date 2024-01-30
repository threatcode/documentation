---
Title: recordmydesktop
Homepage: https://enselic.github.io/recordmydesktop/
Repository: 
Architectures: any
Version: 0.4.0-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-reporting 
Icon: images/recordmydesktop-logo.svg
PackagesInfo: |
 ### recordmydesktop
 
  The application produces an ogg-encapsulated theora-vorbis file.
  recordMyDesktop tries to be as unobstrusive as possible by proccessing only
  regions of the screen that have changed
 
 **Installed size:** `125 KB`  
 **How to install:** `sudo apt install recordmydesktop`  
 
 {{< spoiler "Dependencies:" >}}
 * libasound2 
 * libc6 
 * libjack-jackd2-0  | libjack-0.125
 * libogg0 
 * libpopt0 
 * libtheora0 
 * libvorbis0a 
 * libvorbisenc2 
 * libx11-6 
 * libxdamage1 
 * libxext6
 * libxfixes3
 * zlib1g 
 {{< /spoiler >}}
 
 ##### recordmydesktop
 
 Record desktop sessions to an Ogg Theora video file with Vorbis audio
 
 ```
 root@kali:~# recordmydesktop -h
 Usage: recordmydesktop [OPTIONS]^filename
 
 Generic Options
   -h, --help                              Print this help and exit.
       --version                           Print program version and exit.
       --print-config                      Print info about options selected
                                           during compilation and exit.
 
 Image Options
       --windowid=id_of_window             id of window to be recorded.
       --display=DISPLAY                   Display to connect to.
   -x, --x=N>=0                            Offset in x direction.
   -y, --y=N>=0                            Offset in y direction.
       --width=N>0                         Width of recorded window.
       --height=N>0                        Height of recorded window.
       --dummy-cursor=color                Color of the dummy cursor
                                           [black|white]
       --no-cursor                         Disable drawing of the cursor.
       --no-shared                         Disable usage of MIT-shared memory
                                           extension(Not Recommended!).
       --full-shots                        Take full screenshot at every
                                           frame(Not recomended!).
       --follow-mouse                      Makes the capture area follow the
                                           mouse cursor. Autoenables
                                           --full-shots.
       --quick-subsampling                 Do subsampling of the chroma planes
                                           by discarding, not averaging.
       --fps=N(number>0.0)                 A positive number denoting desired
                                           framerate.
 
 Sound Options
       --channels=N                        A positive number denoting desired
                                           sound channels in recording.
       --freq=N                            A positive number denoting desired
                                           sound frequency.
       --buffer-size=N                     A positive number denoting the
                                           desired sound buffer size (in
                                           frames,when using ALSA or OSS)
       --ring-buffer-size=N                A float number denoting the desired
                                           ring buffer size (in seconds,when
                                           using JACK only).
       --device=SOUND_DEVICE               Sound device(default default).
       --use-jack=port1 port2... portn     Record audio from the specified list
                                           of space-separated jack ports.
       --no-sound                          Do not record sound.
 
 Encoding Options
       --on-the-fly-encoding               Encode the audio-video data, while
                                           recording.
       --v_quality=n                       A number from 0 to 63 for desired
                                           encoded video quality(default 63).
       --v_bitrate=n                       A number from 0 to 200000000 for
                                           desired encoded video
                                           bitrate(default 0).
       --s_quality=n                       Desired audio quality(-1 to 10).
 
 Misc Options
       --rescue=path_to_data               Encode data from a previous,
                                           crashed, session.
       --no-wm-check                       Do not try to detect the window
                                           manager(and set options according to
                                           it)
       --no-frame                          Don not show the frame that
                                           visualizes the recorded area.
       --pause-shortcut=MOD+KEY            Shortcut that will be used for
                                           (un)pausing (default Control+Mod1+p).
       --stop-shortcut=MOD+KEY             Shortcut that will be used to stop
                                           the recording (default
                                           Control+Mod1+s).
       --compress-cache                    Image data are cached with light
                                           compression.
       --workdir=DIR                       Location where a temporary directory
                                           will be created to hold project
                                           files(default $HOME).
       --delay=n[H|h|M|m]                  Number of secs(default),minutes or
                                           hours before capture starts(number
                                           can be float)
       --overwrite                         If there is already a file with the
                                           same name, delete it (default is to
                                           add a number postfix to the new one).
   -o, --output=filename                   Name of recorded video(default
                                           out.ogv).
 
 	If no other options are specified, filename can be given without the -o switch.
 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
