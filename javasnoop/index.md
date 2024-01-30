---
Title: javasnoop
Homepage: 
Repository: https://gitlab.com/kalilinux/packages/javasnoop
Architectures: all
Version: 1.1-rc2-1kali4
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-reverse-engineering 
Icon: images/javasnoop-logo.svg
PackagesInfo: |
 ### javasnoop
 
  Normally, without access to the original source code,
  testing the security of a Java client is unpredictable at
  best and unrealistic at worst. With access the original
  source, you can run a simple Java program and attach a
  debugger to it remotely, stepping through code and changing
  variables where needed. Doing the same with an applet is a
  little bit more difficult.
  JavaSnoop attempts to solve this problem by allowing you
  attach to an existing process (like a debugger) and
  instantly begin tampering with method calls, run custom
  code, or just watch what's happening on the system.
 
 **Installed size:** `13.14 MB`  
 **How to install:** `sudo apt install javasnoop`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jdk
 {{< /spoiler >}}
 
 ##### javasnoop
 
 
 ```
 root@kali:~# javasnoop -h
 [2] Turning off Java security for JavaSnoop usage
 [3] Starting JavaSnoop...
 [4] Turning Java security back on for safe browsing
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
javasnoop
```

![javasnoop](images/javasnoop.png)
