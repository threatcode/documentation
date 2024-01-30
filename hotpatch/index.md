---
Title: hotpatch
Homepage: https://github.com/vikasnkumar/hotpatch
Repository: https://gitlab.com/kalilinux/packages/hotpatch
Architectures: i386 amd64
Version: 0.2-1kali4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hotpatch
 
  Hotpatch is a library that can be used to dynamically load a
  shared library (.so) file on Linux from one process into
  another already running process, without affecting the
  execution of the target process. The API is a C API, but
  also supported in C++.
 
 **Installed size:** `221 KB`  
 **How to install:** `sudo apt install hotpatch`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### hotpatcher
 
 
 ```
 root@kali:~# hotpatcher -h
 
 Usage: hotpatcher [options] <PID of process to patch>
 
 Options:
 -h           This help message
 -V           Version number.
 -v[vvvv]     Enable verbose logging. Add more 'v's for more
 -N           Dry run. Do not modify anything in process
 -l <.so>     Path or name of the .so file to load. Switches off execution pointer reset
 -s <name>    Symbol to invoke during the dll inject. Optional.
 -x <name>    Set execution pointer to symbol. Cannot be set with -s option
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
