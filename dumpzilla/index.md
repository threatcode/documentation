---
Title: dumpzilla
Homepage: http://www.dumpzilla.org/
Repository: https://gitlab.com/kalilinux/packages/dumpzilla
Architectures: all
Version: 20210311-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dumpzilla
 
  Dumpzilla application is developed in Python 3.x and has as purpose extract all
  forensic interesting information of Firefox, Iceweasel and Seamonkey browsers
  to be analyzed. Due to its Python 3.x development, might not work properly in
  old Python versions, mainly with certain characters. Works under Unix and
  Windows 32/64 bits systems. Works in command line interface, so information
  dumps could be redirected by pipes with tools such as grep, awk, cut, sed...
  Dumpzilla allows one to visualize following sections, search customization and
  extract certain content.
 
 **Installed size:** `136 KB`  
 **How to install:** `sudo apt install dumpzilla`  
 
 {{< spoiler "Dependencies:" >}}
 * libnss3
 * python3
 * python3-lz4
 * python3-magic-ahupp
 {{< /spoiler >}}
 
 ##### dumpzilla
 
 
 ```
 root@kali:~# dumpzilla -h
 usage: python dumpzilla.py PROFILE_DIR [OPTIONS]
 
 Options:
 
  --Addons
  --Search
  --Bookmarks [-bm_create_range <start> <end>][-bm_last_range <start> <end>]
  --Certoverride
  --Cookies [-showdom] [-domain <string>] [-name <string>] [-hostcookie <string>] [-access <date>] [-create <date>]
            [-secure <0|1>] [-httponly <0|1>] [-last_range <start> <end>] [-create_range <start> <end>]
  --Downloads [-range <start> <end>]
  --Export <directory> (export data as json)
  --Forms [-value <string>] [-forms_range <start> <end>]
  --Help (shows this help message and exit)
  --History [-url <string>] [-title <string>] [-date <date>] [-history_range <start> <end>] [-frequency]
  --Keypinning [-entry_type <HPKP|HSTS>]
  --OfflineCache [-cache_range <start> <end> -extract <directory>]
  --Preferences
  --Passwords
  --Permissions [-host <string>] [-modif <date>] [-modif_range <start> <end>]
  --RegExp (use Regular Expresions for string type filters instead of Wildcards)
  --Session
  --Summary (no data extraction, only summary report)
  --Thumbnails [-extract_thumb <directory>]
  --Verbosity (DEBUG|INFO|WARNING|ERROR|CRITICAL)
  --Watch [-text <string>] (shows in daemon mode the URLs and text form in real time; Unix only)
 
 Wildcards (without RegExp option):
 
  '%'  Any string of any length (including zero length)
  '_'  Single character
  '\'  Escape character
 
 Regular Expresions: https://docs.python.org/3/library/re.html
 
 Date syntax:
 
  YYYY-MM-DD hh:mi:ss (wildcards allowed)
 
 Profile location:
 
  WinXP profile -> 'C:\Documents and Settings\%USERNAME%\Application Data\Mozilla\Firefox\Profiles\xxxx.default'
  Win7 profile  -> 'C:\Users\%USERNAME%\AppData\Roaming\Mozilla\Firefox\Profiles\xxxx.default'
  MacOS profile -> '/Users/$USER/Library/Application\ Support/Firefox/Profiles/xxxx.default'
  Unix profile  -> '/home/$USER/.mozilla/firefox/xxxx.default'
    
 dumpzilla: error: ambiguous option: -h could match -hostcookie, -httponly, -host, -history_range
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## dumpzilla Usage Example

Analyze the Mozilla profile folder (`/root/.mozilla/firefox/k780shir.default/`) and dump everything except the DOM data (`–All`):

```
root@kali:~# dumpzilla '/root/.mozilla/firefox/k780shir.default/' --All

====================================================================================================
Cookies              [SHA256 hash: 18d35b51ec9865ea3dd21e9bc69dc3d286d4e20373bbb0b350a0e41c8bf2da42]
====================================================================================================


Domain: google.com
Host: .google.com
Name: PREF
Value: ID=ddcc3d04cf65b33f:TM=1400253352:LM=1400253352:S=LrFq_HXVbaconjt0l
Path: /
Expiry: 2016-05-15 11:15:52
Last acess: 2014-05-16 11:15:52
Creation Time: 2014-05-16 11:15:52
Secure: No
HttpOnly: No


Domain: kali.org
Host: .kali.org
Name: __utma
Value: 24402336.1888242215.144BAC0N56.1400253356.14322255.1
Path: /
Expiry: 2016-05-15 11:15:55
Last acess: 2014-05-16 11:15:55
Creation Time: 2014-05-16 11:15:55
```
