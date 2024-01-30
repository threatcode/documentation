---
archived: "true"
Title: android-sdk
Homepage: https://developer.android.com/index.html
Repository: https://gitlab.com/kalilinux/packages/android-sdk
Architectures: all
Version: 22.0.1-1kali1
Metapackages: kali-linux-everything 
Icon: images/android-sdk-logo.svg
PackagesInfo: |
 ### android-sdk
 
   The Android SDK provides you the API libraries and
  developer tools necessary to build, test, and debug apps
  for Android.
 
 **Installed size:** `124.87 MB`  
 **How to install:** `sudo apt install android-sdk`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 {{< /spoiler >}}
 
 ##### android
 
 
 ```
 root@kali:~# android -h
 
        Usage:
        android [global options] action [action options]
        Global options:
   -s --silent     : Silent mode, shows errors only.
   -v --verbose    : Verbose mode, shows errors, warnings and all messages.
      --clear-cache: Clear the SDK Manager repository manifest cache.
   -h --help       : Help on a specific command.
 
                                                                     Valid
                                                                     actions
                                                                     are
                                                                     composed
                                                                     of a verb
                                                                     and an
                                                                     optional
                                                                     direct
                                                                     object:
 -    sdk              : Displays the SDK Manager window.
 -    avd              : Displays the AVD Manager window.
 -   list              : Lists existing targets or virtual devices.
 -   list avd          : Lists existing Android Virtual Devices.
 -   list target       : Lists existing targets.
 -   list sdk          : Lists remote SDK repository.
 - create avd          : Creates a new Android Virtual Device.
 -   move avd          : Moves or renames an Android Virtual Device.
 - delete avd          : Deletes an Android Virtual Device.
 - update avd          : Updates an Android Virtual Device to match the folders
                         of a new SDK.
 - create project      : Creates a new Android project.
 - update project      : Updates an Android project (must already have an
                         AndroidManifest.xml).
 - create test-project : Creates a new Android project for a test package.
 - update test-project : Updates the Android project for a test package (must
                         already have an AndroidManifest.xml).
 - create lib-project  : Creates a new Android library project.
 - update lib-project  : Updates an Android library project (must already have
                         an AndroidManifest.xml).
 - create uitest-project: Creates a new UI test project.
 - update adb          : Updates adb to support the USB devices declared in the
                         SDK add-ons.
 - update sdk          : Updates the SDK by suggesting new platforms to install
                         if available.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
android
```

![android-sdk](images/android-sdk.png)
