---
Title: bytecode-viewer
Homepage: https://github.com/Konloch/bytecode-viewer
Repository: https://gitlab.com/kalilinux/packages/bytecode-viewer
Architectures: all
Version: 2.10.16-0kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-reverse-engineering 
Icon: images/bytecode-viewer-logo.svg
PackagesInfo: |
 ### bytecode-viewer
 
  This package contains Bytecode Viewer (BCV). It is an Advanced Lightweight
  Java Bytecode Viewer, GUI Java Decompiler, GUI Bytecode Editor, GUI Smali, GUI
  Baksmali, GUI APK Editor, GUI Dex Editor, GUI APK Decompiler, GUI DEX
  Decompiler, GUI Procyon Java Decompiler, GUI Krakatau, GUI CFR Java
  Decompiler, GUI FernFlower Java Decompiler, GUI DEX2Jar, GUI Jar2DEX, GUI
  Jar-Jar, Hex Viewer, Code Searcher, Debugger and more.
   
  There is also a plugin system that will allow you to interact with the loaded
  classfiles, for example you can write a String deobfuscator, a malicious code
  searcher, or something else you can think of. You can either use one of the
  pre-written plugins, or write your own. It supports groovy scripting. Once a
  plugin is activated, it will execute the plugin with a ClassNode ArrayList of
  every single class loaded in BCV, this allows the user to handle it completely
  using ASM.
   
  It's currently being maintained and developed by Konloch.
 
 **Installed size:** `40.88 MB`  
 **How to install:** `sudo apt install bytecode-viewer`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 * java-wrappers
 {{< /spoiler >}}
 
 ##### bytecode-viewer
 
 
 ```
 root@kali:~# bytecode-viewer -h
 Bytecode Viewer 2.10.16 [Fat Jar] - Created by @Konloch
 https://bytecodeviewer.com - https://the.bytecode.club
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
