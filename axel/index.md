---
Title: axel
Homepage: https://github.com/axel-download-accelerator/axel
Repository: https://salsa.debian.org/debian/axel
Architectures: any
Version: 2.17.11-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### axel
 
  Axel tries to accelerate the downloading process by using multiple
  connections for one file, similar to DownThemAll and other famous
  programs. It can also use multiple mirrors for one download.
   
  Using Axel, you will get files faster from Internet. So, Axel can
  speed up a download up to 60% (approximately, according to some tests).
   
  Axel supports HTTP, HTTPS, FTP and FTPS protocols.
   
  Axel tries to be as light as possible, so it might be useful as a
  wget clone (and other console based programs) on byte-critical systems.
 
 **Installed size:** `201 KB`  
 **How to install:** `sudo apt install axel`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libssl3 
 {{< /spoiler >}}
 
 ##### axel
 
 Light command line download accelerator
 
 ```
 root@kali:~# axel -h
 Axel 2.17.11 (linux-gnu)
 Usage: axel [options] url1 [url2] [url...]
 
 --max-speed=x		-s x	Specify maximum speed (bytes per second)
 --num-connections=x	-n x	Specify maximum number of connections
 --max-redirect=x		Specify maximum number of redirections
 --output=f		-o f	Specify local output file
 --search[=n]		-S[n]	Search for mirrors and download from n servers
 --ipv4			-4	Use the IPv4 protocol
 --ipv6			-6	Use the IPv6 protocol
 --header=x		-H x	Add HTTP header string
 --user-agent=x		-U x	Set user agent
 --no-proxy		-N	Just don't use any proxy server
 --insecure		-k	Don't verify the SSL certificate
 --no-clobber		-c	Skip download if file already exists
 --quiet			-q	Leave stdout alone
 --verbose		-v	More status information
 --alternate		-a	Alternate progress indicator
 --percentage		-p	Print simple percentages instead of progress bar (0-100)
 --help			-h	This information
 --timeout=x		-T x	Set I/O and connection timeout
 --version		-V	Version information
 
 Visit https://github.com/axel-download-accelerator/axel/issues to report bugs
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
