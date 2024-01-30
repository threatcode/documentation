---
Title: maltego
Homepage: https://www.maltego.com
Repository: https://gitlab.com/kalilinux/packages/maltego
Architectures: all
Version: 4.4.1-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-identify kali-tools-information-gathering kali-tools-reporting kali-tools-social-engineering kali-tools-web 
Icon: images/maltego-logo.svg
PackagesInfo: |
 ### maltego
 
  Maltego is an open source intelligence and forensics
  application. It will offer you timous mining and gathering
  of information as well as the representation of this
  information in a easy to understand format.
   
  This package replaces previous packages matlegoce and casefile.
 
 **Installed size:** `231.26 MB`  
 **How to install:** `sudo apt install maltego`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 * java-wrappers
 {{< /spoiler >}}
 
 ##### maltego
 
 
 ```
 root@kali:~# maltego -h
 ./../platform/lib/nbexec: WARNING: environment variable DISPLAY is not set
 Module reload options:
   --reload /path/to/module.jar  install or reinstall a module JAR file
 
 Additional module options:
   -o, --open <arg1>...<argN> 
   -p, --automationPort <arg> 
   -m, --machine <arg>        
   -i, --import <arg>         
   -u, --updates <arg>        
   -z, --cloudDebug <arg>     
   -c, --cloud <arg>          
   -s, --serverHttpAllowed    
   -h, --hub <arg>            
 
 Core options:
   --laf <LaF classname> use given LookAndFeel class instead of the default
   --fontsize <size>     set the base font size of the user interface, in points
   --locale <language[:country[:variant]]> use specified locale
   --userdir <path>      use specified directory to store user settings
   --cachedir <path>     use specified directory to store user cache, must be different from userdir
   --nosplash            do not show the splash screen
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
