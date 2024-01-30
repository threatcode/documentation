---
Title: sigma-cli
Homepage: https://github.com/SigmaHQ/sigma-cli
Repository: https://gitlab.com/kalilinux/packages/sigma-cli
Architectures: all
Version: 0.7.10-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sigma-cli
 
  This package contains the Sigma command line interface using the pySigma
  library to manage, list and convert Sigma rules into query languages.
 
 **Installed size:** `66 KB`  
 **How to install:** `sudo apt install sigma-cli`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-click
 * python3-colorama
 * python3-prettytable
 * python3-sigma 
 {{< /spoiler >}}
 
 ##### sigma-cli
 
 
 ```
 root@kali:~# sigma-cli --help
 Usage: sigma-cli [OPTIONS] COMMAND [ARGS]...
 
 Options:
   --help  Show this message and exit.
 
 Commands:
   analyze  Analyze Sigma rule sets
   check    Check Sigma rules for validity and best practices (not yet...
   convert  Convert Sigma rules into queries.
   list     List available targets or processing pipelines.
   plugin   pySigma plugin management (backends, processing pipelines and...
   version  Print version of Sigma CLI.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
