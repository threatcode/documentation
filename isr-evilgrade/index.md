---
Title: isr-evilgrade
Homepage: https://github.com/infobyte/evilgrade
Repository: https://gitlab.com/kalilinux/packages/isr-evilgrade
Architectures: all
Version: 2.0.9-0kali2
Metapackages: kali-linux-everything kali-tools-sniffing-spoofing 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### isr-evilgrade
 
  Evilgrade is a modular framework that allows the user to
  take advantage of poor upgrade implementations by injecting
  fake updates. It comes with pre-made binaries (agents), a
  working default configuration for fast pentests, and has
  it's own WebServer and DNSServer modules. Easy to set up
  new settings, and has an autoconfiguration when new binary
  agents are set.
 
 **Installed size:** `13.14 MB`  
 **How to install:** `sudo apt install isr-evilgrade`  
 
 {{< spoiler "Dependencies:" >}}
 * libdata-dump-perl
 * libdigest-md5-file-perl
 * librpc-xml-perl
 * perl
 {{< /spoiler >}}
 
 ##### evilgrade
 
 
 ```
 root@kali:~# evilgrade -h
 [DEBUG] - Loading module: modules/ccleaner.pm
 [DEBUG] - Loading module: modules/filezilla.pm
 [DEBUG] - Loading module: modules/soapui.pm
 [DEBUG] - Loading module: modules/lenovo.pm
 [DEBUG] - Loading module: modules/notepadplus.pm
 [DEBUG] - Loading module: modules/apptapp.pm
 [DEBUG] - Loading module: modules/osx.pm
 [DEBUG] - Loading module: modules/teamviewer.pm
 [DEBUG] - Loading module: modules/nokiasoftware.pm
 [DEBUG] - Loading module: modules/sparkle.pm
 [DEBUG] - Loading module: modules/winupdate.pm
 [DEBUG] - Loading module: modules/appleupdate.pm
 [DEBUG] - Loading module: modules/port.pm
 [DEBUG] - Loading module: modules/cpan.pm
 [DEBUG] - Loading module: modules/bsplayer.pm
 [DEBUG] - Loading module: modules/panda_antirootkit.pm
 [DEBUG] - Loading module: modules/express_talk.pm
 [DEBUG] - Loading module: modules/blackberry.pm
 [DEBUG] - Loading module: modules/miranda.pm
 [DEBUG] - Loading module: modules/sunjava.pm
 [DEBUG] - Loading module: modules/techtracker.pm
 [DEBUG] - Loading module: modules/winzip.pm
 [DEBUG] - Loading module: modules/vidbox.pm
 [DEBUG] - Loading module: modules/lenovoapk.pm
 [DEBUG] - Loading module: modules/virtualbox.pm
 [DEBUG] - Loading module: modules/ubertwitter.pm
 [DEBUG] - Loading module: modules/fcleaner.pm
 [DEBUG] - Loading module: modules/openbazaar.pm
 [DEBUG] - Loading module: modules/winamp.pm
 [DEBUG] - Loading module: modules/jet.pm
 [DEBUG] - Loading module: modules/apt.pm
 [DEBUG] - Loading module: modules/winscp.pm
 [DEBUG] - Loading module: modules/fsecure_client.pm
 [DEBUG] - Loading module: modules/acer.pm
 [DEBUG] - Loading module: modules/safari.pm
 [DEBUG] - Loading module: modules/getjar.pm
 [DEBUG] - Loading module: modules/dap.pm
 [DEBUG] - Loading module: modules/sparkle2.pm
 [DEBUG] - Loading module: modules/appstore.pm
 [DEBUG] - Loading module: modules/inteldriver.pm
 [DEBUG] - Loading module: modules/asus.pm
 [DEBUG] - Loading module: modules/lenovofirmware.pm
 [DEBUG] - Loading module: modules/atube.pm
 [DEBUG] - Loading module: modules/itunes.pm
 [DEBUG] - Loading module: modules/googleanalytics.pm
 [DEBUG] - Loading module: modules/superantispyware.pm
 [DEBUG] - Loading module: modules/bbappworld.pm
 [DEBUG] - Loading module: modules/keepass.pm
 [DEBUG] - Loading module: modules/clamwin.pm
 [DEBUG] - Loading module: modules/freerip.pm
 [DEBUG] - Loading module: modules/amsn.pm
 [DEBUG] - Loading module: modules/jetphoto.pm
 [DEBUG] - Loading module: modules/flashget.pm
 [DEBUG] - Loading module: modules/vmware.pm
 [DEBUG] - Loading module: modules/quicktime.pm
 [DEBUG] - Loading module: modules/nokia.pm
 [DEBUG] - Loading module: modules/mirc.pm
 [DEBUG] - Loading module: modules/timedoctor.pm
 [DEBUG] - Loading module: modules/opera.pm
 [DEBUG] - Loading module: modules/istat.pm
 [DEBUG] - Loading module: modules/linkedin.pm
 [DEBUG] - Loading module: modules/openoffice.pm
 [DEBUG] - Loading module: modules/paintnet.pm
 [DEBUG] - Loading module: modules/autoit3.pm
 [DEBUG] - Loading module: modules/divxsuite.pm
 [DEBUG] - Loading module: modules/cygwin.pm
 [DEBUG] - Loading module: modules/growl.pm
 [DEBUG] - Loading module: modules/jdtoolkit.pm
 [DEBUG] - Loading module: modules/orbit.pm
 [DEBUG] - Loading module: modules/sunbelt.pm
 [DEBUG] - Loading module: modules/skype.pm
 [DEBUG] - Loading module: modules/gom.pm
 [DEBUG] - Loading module: modules/photoscape.pm
 [DEBUG] - Loading module: modules/flip4mac.pm
 [DEBUG] - Loading module: modules/yahoomsn.pm
 [DEBUG] - Loading module: modules/speedbit.pm
 [DEBUG] - Loading module: modules/trillian.pm
 [DEBUG] - Loading module: modules/allmynotes.pm
 [DEBUG] - Loading module: modules/samsung.pm
 [DEBUG] - Loading module: modules/isopen.pm
             _ _                     _      
            (_) |                   | |     
   _____   ___| | __ _ _ __ __ _  __| | ___ 
  / _ \ \ / / | |/ _` | '__/ _` |/ _` |/ _ \ 
 |  __/\ V /| | | (_| | | | (_| | (_| |  __/ 
  \___| \_/ |_|_|\__, |_|  \__,_|\__,_|\___| 
                 __/ |                      
                 |___/ 
 -------------------------------------------
 ---------------------  www.infobytesec.com 
 - 80 modules available.
 
 evilgrade>
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## evilgrade Usage Example

```
root@kali:~# evilgrade
[DEBUG] - Loading module: modules/allmynotes.pm
[DEBUG] - Loading module: modules/notepadplus.pm
[DEBUG] - Loading module: modules/nokia.pm
[DEBUG] - Loading module: modules/winscp.pm
[DEBUG] - Loading module: modules/jet.pm
[DEBUG] - Loading module: modules/sunjava.pm
[DEBUG] - Loading module: modules/bbappworld.pm
[DEBUG] - Loading module: modules/gom.pm
[DEBUG] - Loading module: modules/ccleaner.pm
[DEBUG] - Loading module: modules/superantispyware.pm
[DEBUG] - Loading module: modules/winupdate.pm
[DEBUG] - Loading module: modules/vidbox.pm
[DEBUG] - Loading module: modules/atube.pm
[DEBUG] - Loading module: modules/winzip.pm
[DEBUG] - Loading module: modules/apt.pm
[DEBUG] - Loading module: modules/mirc.pm
[DEBUG] - Loading module: modules/filezilla.pm
[DEBUG] - Loading module: modules/dap.pm
[DEBUG] - Loading module: modules/flip4mac.pm
[DEBUG] - Loading module: modules/divxsuite.pm
[DEBUG] - Loading module: modules/opera.pm
[DEBUG] - Loading module: modules/yahoomsn.pm
[DEBUG] - Loading module: modules/linkedin.pm
[DEBUG] - Loading module: modules/techtracker.pm
[DEBUG] - Loading module: modules/fcleaner.pm
[DEBUG] - Loading module: modules/appleupdate.pm
[DEBUG] - Loading module: modules/trillian.pm
[DEBUG] - Loading module: modules/sunbelt.pm
[DEBUG] - Loading module: modules/growl.pm
[DEBUG] - Loading module: modules/vmware.pm
[DEBUG] - Loading module: modules/panda_antirootkit.pm
[DEBUG] - Loading module: modules/orbit.pm
[DEBUG] - Loading module: modules/teamviewer.pm
[DEBUG] - Loading module: modules/blackberry.pm
[DEBUG] - Loading module: modules/miranda.pm
[DEBUG] - Loading module: modules/clamwin.pm
[DEBUG] - Loading module: modules/jetphoto.pm
[DEBUG] - Loading module: modules/istat.pm
[DEBUG] - Loading module: modules/nokiasoftware.pm
[DEBUG] - Loading module: modules/getjar.pm
[DEBUG] - Loading module: modules/sparkle.pm
[DEBUG] - Loading module: modules/cpan.pm
[DEBUG] - Loading module: modules/cygwin.pm
[DEBUG] - Loading module: modules/express_talk.pm
[DEBUG] - Loading module: modules/openoffice.pm
[DEBUG] - Loading module: modules/osx.pm
[DEBUG] - Loading module: modules/flashget.pm
[DEBUG] - Loading module: modules/amsn.pm
[DEBUG] - Loading module: modules/isopen.pm
[DEBUG] - Loading module: modules/apptapp.pm
[DEBUG] - Loading module: modules/googleanalytics.pm
[DEBUG] - Loading module: modules/autoit3.pm
[DEBUG] - Loading module: modules/ubertwitter.pm
[DEBUG] - Loading module: modules/photoscape.pm
[DEBUG] - Loading module: modules/quicktime.pm
[DEBUG] - Loading module: modules/itunes.pm
[DEBUG] - Loading module: modules/winamp.pm
[DEBUG] - Loading module: modules/skype.pm
[DEBUG] - Loading module: modules/virtualbox.pm
[DEBUG] - Loading module: modules/bsplayer.pm
[DEBUG] - Loading module: modules/freerip.pm
[DEBUG] - Loading module: modules/paintnet.pm
[DEBUG] - Loading module: modules/speedbit.pm
            _ _                     _
           (_) |                   | |
  _____   ___| | __ _ _ __ __ _  __| | ___
 / _ \ \ / / | |/ _` | '__/ _` |/ _` |/ _ \
|  __/\ V /| | | (_| | | | (_| | (_| |  __/
 \___| \_/ |_|_|\__, |_|  \__,_|\__,_|\___|
                __/ |
                |___/
-------------------------------------------
---------------------  www.infobytesec.com
- 63 modules available.

evilgrade>config skype
evilgrade(skype)>start
evilgrade(skype)>
[17/5/2014:12:52:11] - [WEBSERVER] - Webserver ready. Waiting for connections ...

evilgrade(skype)>
[17/5/2014:12:52:11] - [DNSSERVER] - DNS Server Ready. Waiting for Connections ...

evilgrade(skype)>
```
