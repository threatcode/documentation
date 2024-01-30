---
Title: driftnet
Homepage: https://github.com/deiv/driftnet
Repository: https://github.com/deiv/driftnet
Architectures: any
Version: 1.5.0-0.2
Metapackages: kali-linux-everything kali-linux-large kali-tools-sniffing-spoofing 
Icon: images/driftnet-logo.svg
PackagesInfo: |
 ### driftnet
 
  Inspired by EtherPEG, Driftnet is a program which listens to network
  traffic and picks out images from TCP streams it observes. It is
  interesting to run it on a host which sees a lot of web traffic.
   
  (Obviously, this is an invasion of privacy of a fairly blatant sort.
  Also, if you are possessed of Victorian sensibilities, and share an
  unswitched network with others who are not, you should probably not
  use it.)
 
 **Installed size:** `112 KB`  
 **How to install:** `sudo apt install driftnet`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcairo2 
 * libgif7 
 * libglib2.0-0 
 * libgtk-3-0 
 * libjpeg62-turbo 
 * libpcap0.8 
 * libpng16-16 
 * libwebp7 
 * libwebsockets19 
 {{< /spoiler >}}
 
 ##### driftnet
 
 Capture images from network traffic and display them in an X window; optionally, capture audio streams and play them.
 
 ```
 root@kali:~# driftnet -h
 driftnet, version 1.5.0
 Capture images from network traffic and display them.
 
 Synopsis: driftnet [options] [filter code]
 
 Options:
 
   -h               Display this help message.
   -v               Verbose operation.
   -b               Beep when a new image is captured.
   -i interface     Select the interface on which to listen (default: all
                    interfaces).
   -f file          Instead of listening on an interface, read captured
                    packets from a pcap dump file; file can be a named pipe
                    for use with Kismet or similar.
   -p               Do not put the listening interface into promiscuous mode.
   -a               Adjunct mode: do not display images on screen, but save
                    them to a temporary directory and announce their names on
                    standard output.
   -m number        Maximum number of images to keep in temporary directory
                    in adjunct mode.
   -d directory     Use the named temporary directory.
   -x prefix        Prefix to use when saving images.
   -s               Attempt to extract streamed audio data from the network,
                    in addition to images. At present this supports MPEG data
                    only.
   -S               Extract streamed audio but not images.
   -M command       Use the given command to play MPEG audio data extracted
                    with the -s option; this should process MPEG frames
                    supplied on standard input. Default: `mpg123 -'.
   -Z username      Drop privileges to user 'username' after starting pcap.
   -l               List the system capture interfaces.
   -p               Put the interface in monitor mode (not supported on all interfaces).
   -g               Enable GTK display (this is the default).
   -w               Enable the HTTP server to display images.
   -W               Port number for the HTTP server (implies -w). Default: 9090.
 
 Filter code can be specified after any options in the manner of tcpdump(8).
 The filter code will be evaluated as `tcp and (user filter code)'
 
 You can save images to the current directory by clicking on them.
 
 Adjunct mode is designed to be used by other programs which want to use
 driftnet to gather images from the network. With the -m option, driftnet will
 silently drop images if more than the specified number of images are saved
 in its temporary directory. It is assumed that some other process is
 collecting and deleting the image files.
 
 driftnet, copyright (c) 2001-2002 Chris Lightfoot <chris@ex-parrot.com>
           copyright (c) 2012-2022 David Suárez <david.sephirot@gmail.com>
 home page: https://github.com/deiv/driftnet
 old home page: http://www.ex-parrot.com/~chris/driftnet/
 
 This program is free software; you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation; either version 2 of the License, or
 (at your option) any later version.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
