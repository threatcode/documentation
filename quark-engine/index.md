---
Title: quark-engine
Homepage: https://github.com/quark-engine/quark-engine
Repository: https://gitlab.com/kalilinux/packages/quark-engine
Architectures: all
Version: 23.9.1-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### quark-engine
 
  Quark-Engine is a full-featured Android analysis framework written in
  Python for hunting threat intelligence inside the APK, DEX files.
  Since it is rule-based, you can use the ones built-in or customize as
  needed.
  With ideas decoded from criminal law, Quark-Engine has its unique
  angles for Android analysis. A Dalvik bytecode loader has been developed
  that has tainted analysis inside but also defeats the obfuscation
  techniques used against reverse engineering. And surprisingly,
  the loader matches perfectly the design of the malware scoring
  system.
  Quark-Engine is very easy to use and also provides flexible output
  formats. There are three types of output reports: detail report, call
  graph, and summary report. With these reports in mind, you can get an
  overview of the high-risk behavior inside Android within seconds.
  Also, by integrating with other Android analysis tools such as
  Ghidra, APKLAB, Jadx, Quark-Engine can greatly improve the efficiency
  of reverse engineers.
 
 **Installed size:** `423 KB`  
 **How to install:** `sudo apt install quark-engine`  
 
 {{< spoiler "Dependencies:" >}}
 * androguard
 * python3
 * python3-click
 * python3-colorama
 * python3-graphviz
 * python3-plotly
 * python3-prettytable
 * python3-prompt-toolkit
 * python3-requests
 * python3-rzpipe
 * python3-tqdm
 {{< /spoiler >}}
 
 ##### freshquark
 
 
 ```
 root@kali:~# freshquark -h
 [*] Download the latest rules from https://github.com/quark-engine/quark-rules
 [+] DONE: Complete downloading the latest quark-rules.
 All the rules are saved in /root/.quark-engine/quark-rules/rules.
 To specify one of the rules of Quark-Rule, use /root/.quark-engine/quark-rules/rules/<rule_name>.json as an argument.
 ```
 
 - - -
 
 ##### quark
 
 
 ```
 root@kali:~# quark --help
 
     ________                      __
     \_____  \  __ _______ _______|  | __
      /  / \  \|  |  \__  \_  __ \  |/ /
     /   \_/.  \  |  // __ \|  | \/    <
     \_____\ \_/____/(____  /__|  |__|_ \
            \__>          \/           \/ v23.9.1
     
                 An Obfuscation-Neglect Android Malware Scoring System
                 
 Usage: quark [OPTIONS]
 
   Quark is an Obfuscation-Neglect Android Malware Scoring System
 
 Options:
   -s, --summary TEXT              Show summary report. Optionally specify the
                                   name of a rule/label
   -d, --detail TEXT               Show detail report. Optionally specify the
                                   name of a rule/label
   -o, --output FILE               Output report in JSON
   -w, --webreport FILE            Generate web report
   -a, --apk FILE                  APK file  [required]
   -r, --rule PATH                 Rules directory  [default: /root/.quark-
                                   engine/quark-rules/rules]
   -g, --graph [png|json]          Create call graph to call_graph_image
                                   directory
   -c, --classification            Show rules classification
   -t, --threshold [100|80|60|40|20]
                                   Set the lower limit of the confidence
                                   threshold
   -i, --list [all|native|custom]  List classes, methods and descriptors
   -p, --permission                List Android permissions
   -l, --label [max|detailed]      Show report based on label of rules
   -C, --comparison                Behaviors comparison based on max confidence
                                   of rule labels
   --generate-rule DIRECTORY       Generate rules and output to given directory
   --core-library [androguard|rizin]
                                   Specify the core library used to analyze an
                                   APK
   --multi-process INTEGER RANGE   Allow analyzing APK with N processes, where
                                   N doesn't exceeds the number of usable CPUs
                                   - 1 to avoid memory exhaustion.  [x>=1]
   --version                       Show the version and exit.
   --help                          Show this message and exit.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
