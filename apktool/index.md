---
Title: apktool
Homepage: https://ibotpeaches.github.io/Apktool/
Repository: https://salsa.debian.org/android-tools-team/apktool
Architectures: any
Version: 2.7.0+dfsg-6
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-reverse-engineering 
Icon: images/apktool-logo.svg
PackagesInfo: |
 ### apktool
 
  A tool for reverse engineering 3rd party, closed, binary Android apps. It can
  decode resources to nearly original form and rebuild them after making some
  modifications; it makes possible to debug smali code step by step. Also it
  makes working with an app easier because of project-like file structure and
  automation of some repetitive tasks like building apk.
 
 **Installed size:** `269 KB`  
 **How to install:** `sudo apt install apktool`  
 
 {{< spoiler "Dependencies:" >}}
 * aapt
 * android-framework-res
 * default-jre-headless | java8-runtime-headless
 * libantlr3-runtime-java
 * libcommons-cli-java
 * libcommons-io-java
 * libcommons-lang3-java
 * libcommons-text-java
 * libguava-java
 * libsmali-java 
 * libstringtemplate-java
 * libxmlunit-java
 * libxpp3-java
 * libyaml-snake-java
 {{< /spoiler >}}
 
 ##### apktool
 
 Tool for reverse engineering Android apk files
 
 ```
 root@kali:~# apktool -h
 Apktool v2.7.0-dirty - a tool for reengineering Android apk files
 with smali v2.5.2.git2771eae-debian and baksmali v2.5.2.git2771eae-debian
 Copyright 2010 Ryszard Wiśniewski <brut.alll@gmail.com>
 Copyright 2010 Connor Tumbleson <connor.tumbleson@gmail.com>
 
 usage: apktool
  -advance,--advanced   prints advance information.
  -version,--version    prints the version then exits
 usage: apktool if|install-framework [options] <framework.apk>
  -p,--frame-path <dir>   Stores framework files into <dir>.
  -t,--tag <tag>          Tag frameworks using <tag>.
 usage: apktool d[ecode] [options] <file_apk>
  -f,--force              Force delete destination directory.
  -o,--output <dir>       The name of folder that gets written. Default is apk.out
  -p,--frame-path <dir>   Uses framework files located in <dir>.
  -r,--no-res             Do not decode resources.
  -s,--no-src             Do not decode sources.
  -t,--frame-tag <tag>    Uses framework files tagged by <tag>.
 usage: apktool b[uild] [options] <app_path>
  -f,--force-all          Skip changes detection and build all files.
  -o,--output <dir>       The name of apk that gets written. Default is dist/name.apk
  -p,--frame-path <dir>   Uses framework files located in <dir>.
 
 For additional info, see: https://ibotpeaches.github.io/Apktool/ 
 For smali/baksmali info, see: https://github.com/JesusFreke/smali
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## apktool Usage Example

Use debug mode (`d`) to decode the given apk file (`/root/SdkControllerApp.apk)`:

```
root@kali:~# apktool d Facebook\ Lite_v121.0.0.8.97_apkpure.com.apk
I: Using Apktool 2.3.4-dirty on Facebook Lite_v121.0.0.8.97_apkpure.com.apk
I: Loading resource table...
I: Decoding AndroidManifest.xml with resources...
I: Loading resource table from file: /root/.local/share/apktool/framework/1.apk
I: Regular manifest package...
I: Decoding file-resources...
I: Decoding values */* XMLs...
I: Baksmaling classes.dex...
I: Copying assets and libs...
I: Copying unknown files...
I: Copying original files...
```
