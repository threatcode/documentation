---
archived: "true"
Title: radare2-cutter
Homepage: https://cutter.re
Repository: https://salsa.debian.org/pkg-security-team/radare2-cutter
Architectures: amd64 arm64 armhf i386 mipsel
Version: 1.12.0-1
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-hardware kali-tools-reverse-engineering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### radare2-cutter
 
  Cutter is a Qt based GUI for reverse engineering binaries, which makes
  use of the radare2 framework. Advanced users are expected to use the
  radare2 CLI tools instead, which are much more powerful.
 
 **Installed size:** `3.72 MB`  
 **How to install:** `sudo apt install radare2-cutter`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcgraph6
 * libgcc-s1 
 * libgvc6
 * libkf5syntaxhighlighting5 
 * libpython3.9 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5svg5 
 * libqt5widgets5 
 * libradare2-5.0.0 
 * libstdc++6 
 * python3
 * python3-ipykernel
 * python3-jupyter-client
 * python3-notebook
 * python3-zmq
 {{< /spoiler >}}
 
 ##### Cutter
 
 GUI for radare2 reverse engineering framework
 
 ```
 root@kali:~# man Cutter
 CUTTER(1)                   General Commands Manual                  CUTTER(1)
 
 NAME
        Cutter - GUI for radare2 reverse engineering framework
 
 SYNOPSIS
        Cutter [options] <filename>
 
 DESCRIPTION
        Cutter is a Qt and C++ GUI for radare2 reverse engineering framework.
 
 OPTIONS
        -h, --help
               Displays this help
 
        -v, --version
               Displays version information
 
        -A, --anal=level
               Automatically  open  file  and  optionally start analysis. Needs
               filename to be specified. May be a value between 0 and 2. 0 = no
               analysis, 1 = aaa, 2 = aaaa (experimental)
 
        --pythonhome=PYTHONHOME
               PYTHONHOME to use for Jupyter
 
 AUTHOR
        cutter  was  written  by the Cutter Project <https://github.com/radare-
        org/cutter>.
 
        This manual page was written by Sebastian Reichel <sre@debian.org>.
 
                                 August 20, 2018                      CUTTER(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
