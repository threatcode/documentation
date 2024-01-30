---
Title: tzdata
Homepage: https://www.iana.org/time-zones
Repository: https://salsa.debian.org/glibc-team/tzdata
Architectures: all
Version: 2023c-10
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-labs kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-802-11 kali-tools-bluetooth kali-tools-exploitation kali-tools-forensics kali-tools-fuzzing kali-tools-hardware kali-tools-identify kali-tools-information-gathering kali-tools-passwords kali-tools-post-exploitation kali-tools-recover kali-tools-reporting kali-tools-respond kali-tools-reverse-engineering kali-tools-rfid kali-tools-sdr kali-tools-sniffing-spoofing kali-tools-social-engineering kali-tools-top10 kali-tools-vulnerability kali-tools-web kali-tools-windows-resources kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tzdata
 
  This package contains data required for the implementation of
  standard local time for many representative locations around the
  globe. It is updated periodically to reflect changes made by
  political bodies to time zone boundaries, UTC offsets, and
  daylight-saving rules.
 
 **Installed size:** `1.33 MB`  
 **How to install:** `sudo apt install tzdata`  
 
 {{< spoiler "Dependencies:" >}}
 * debconf  | debconf-2.0
 {{< /spoiler >}}
 
 
 - - -
 
 ### tzdata-legacy
 
  This package contains data required for the implementation of
  standard local time for many representative locations around the
  globe. It is updated periodically to reflect changes made by
  political bodies to time zone boundaries, UTC offsets, and
  daylight-saving rules.
   
  This package contains timezones counted in International Atomic Time with a
  -10 second offset (TAI-10s) in /usr/share/zoneinfo/right. This is the current
  IBM recommended setting of hardware clocks on IBM mainframes, which ran on
  GMT until the inception of UTC in 1972 when TAI was 10 seconds ahead of UTC.
  IBM switched to running clocks at the atomic rate and introduced the
  10-second offset in order to avoid a discontinuity.
   
  This package also contains legacy timezone symlinks that are not following
  the current rule of using the geographical region (continent or ocean) and
  city name.
   
  You do not need this package if you are unsure.
 
 **Installed size:** `1.16 MB`  
 **How to install:** `sudo apt install tzdata-legacy`  
 
 {{< spoiler "Dependencies:" >}}
 * tzdata
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
