---
Title: android-sdk-meta
Homepage: 
Repository: https://salsa.debian.org/android-tools-team/android-sdk-meta
Architectures: amd64 i386 armel armhf arm64 mipsel mips64el all ppc64el
Version: 28.0.2+9
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### android-sdk
 
  The Android SDK includes a variety of tools that help you develop mobile
  applications for the Android platform. The tools are classified into 3 groups:
  SDK Tools, Platform-tools and Build-tools.
   
  SDK Tools are platform independent and are required no matter which Android
  platform you are developing on. It is the base toolset of Android SDK.
   
  This metapackage pulls the entire Android SDK.
 
 **Installed size:** `29 KB`  
 **How to install:** `sudo apt install android-sdk`  
 
 {{< spoiler "Dependencies:" >}}
 * android-sdk-build-tools
 * android-sdk-common 
 * android-sdk-platform-tools
 * proguard-cli
 {{< /spoiler >}}
 
 
 - - -
 
 ### android-sdk-build-tools
 
  The Android SDK includes a variety of tools that help you develop mobile
  applications for the Android platform. The tools are classified into 3 groups:
  SDK Tools, Platform-tools and Build-tools.
   
  Build-tools is a component of the Android SDK required for building Android
  application code.
   
  This package pulls Android SDK Build-tool.
 
 **Installed size:** `15 KB`  
 **How to install:** `sudo apt install android-sdk-build-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * aapt 
 * aidl 
 * android-sdk-build-tools-common 
 * apksigner
 * split-select 
 * zipalign 
 {{< /spoiler >}}
 
 
 - - -
 
 ### android-sdk-build-tools-common
 
  The Android SDK includes a variety of tools that help you develop mobile
  applications for the Android platform. The tools are classified into 3 groups:
  SDK Tools, Platform-tools and Build-tools.
   
  Build-tools is a component of the Android SDK required for building Android
  application code.
   
  This package provides common files of Android SDK Build-tools.
 
 **Installed size:** `20 KB`  
 **How to install:** `sudo apt install android-sdk-build-tools-common`  
 
 
 - - -
 
 ### android-sdk-common
 
  The Android SDK includes a variety of tools that help you develop mobile
  applications for the Android platform. The tools are classified into 3 groups:
  SDK Tools, Platform-tools and Build-tools.
   
  SDK Tools are platform independent and are required no matter which Android
  platform you are developing on. It is the base toolset of Android SDK.
   
  This package provides common files of Android SDK Tools.
 
 **Installed size:** `25 KB`  
 **How to install:** `sudo apt install android-sdk-common`  
 
 
 - - -
 
 ### android-sdk-platform-tools
 
  The Android SDK includes a variety of tools that help you develop mobile
  applications for the Android platform. The tools are classified into 3 groups:
  SDK Tools, Platform-tools and Build-tools.
   
  Platform-tools are customized to support the features of the latest Android
  platform.
   
  This package pulls Android SDK Platform-tools.
 
 **Installed size:** `19 KB`  
 **How to install:** `sudo apt install android-sdk-platform-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * android-sdk-platform-tools-common 
 * dmtracedump 
 * e2fsprogs
 * etc1tool 
 * f2fs-tools
 * hprof-conv 
 * sqlite3
 {{< /spoiler >}}
 
 
 - - -
 
 ### android-sdk-platform-tools-common
 
  The Android SDK includes a variety of tools that help you develop mobile
  applications for the Android platform. The tools are classified into 3 groups:
  SDK Tools, Platform-tools and Build-tools.
   
  Platform-tools are customized to support the features of the latest Android
  platform.
   
  This package provides common files of Android SDK Platform-tools. It also
  provides UDEV rules enabling adb and fastboot to work without root access to
  the host machine.
 
 **Installed size:** `38 KB`  
 **How to install:** `sudo apt install android-sdk-platform-tools-common`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
