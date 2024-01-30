---
Title: tcpick
Homepage: http://tcpick.sourceforge.net
Repository: https://salsa.debian.org/pkg-security-team/tcpick
Architectures: any
Version: 0.2.1-11
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tcpick
 
  This libpcap-based textmode sniffer can:
   * track, reassemble and reorder TCP streams
   * save the captured flows in different files or display them in the terminal
   * display all the stream on the terminal with different display modes like
     hexdump, hexdump + ascii, only printable characters, raw mode, colorized
     mode ...
   * handle several network interface types, including ethernet cards and PPP
     interfaces
 
 **Installed size:** `88 KB`  
 **How to install:** `sudo apt install tcpick`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### tcpick
 
 Tcp stream sniffer and connection tracker
 
 ```
 root@kali:~# tcpick --help
 	tcpick 0.2.1 is a sniffer tool written using libpcap.
 tcpick can keep track of tcp connection, sniff all tcp streams
 and store them to files, to show you what is happening on a network interface
 
 Usage: tcpick [ -a ] [ -n ] [ -C ]				
        [ -i interface ]					
        [ -yH ] [ -yP ] [ -yR ] [ -yU ] [ -yx ] [ -yX ]	
        [ -bH ] [ -bP ] [ -bR ] [ -bU ] [ -bx ] [ -bX ]	
        [ -wH ] [ -wP ] [ -wR ] [ -wU ]			
        [ -v  [ verbosity ]]				
        [ -S ] [ -h ] [ --separator ]			
        [  "filter" ] [ -r  file ]			
        [ --help ] [ --version ]                         
 Example: tcpick -i ppp0 -yP -C -h "not port 22"
 
 for an updated list of options see tcpick(1) manpage
 to see version and license information try `tcpick --version'
 or read the `COPYING' file, released with the package
 
 tcpick homepage: http://tcpick.sourceforge.net
 
 mailing-list address:
 	<tcpick-project@lists.sourceforge.net>
 Archive:
 	http://sourceforge.net/mailarchive/forum.php?forum=tcpick-project
 Subscribe:
 	http://lists.sourceforge.net/lists/listinfo/tcpick-project
 thank you for using tcpick!
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
