---
Title: hubble
Homepage: https://github.com/cilium/hubble
Repository: https://gitlab.com/kalilinux/packages/hubble
Architectures: any
Version: 0.12.2-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hubble
 
  Hubble is a fully distributed networking and security observability
  platform for cloud native workloads. It is built on top of Cilium
  (https://github.com/cilium/cilium) and eBPF (https://ebpf.io) to enable
  deep visibility into the communication and behavior of services as well
  as the networking infrastructure in a completely transparent manner.
 
 **Installed size:** `19.87 MB`  
 **How to install:** `sudo apt install hubble`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### hubble
 
 
 ```
 root@kali:~# hubble -h
 Hubble is a utility to observe and inspect recent Cilium routed traffic in a cluster.
 
 Usage:
   hubble [command]
 
 Available Commands:
   completion  Generate the autocompletion script for the specified shell
   config      Modify or view hubble config
   help        Help about any command
   list        List Hubble objects
   observe     Observe flows and events of a Hubble server
   status      Display status of Hubble server
   version     Display detailed version information
 
 Global Flags:
       --config string   Optional config file (default "/root/.config/hubble/config.yaml")
   -D, --debug           Enable debug messages
 
 Get help:
   -h, --help	Help for any command or subcommand
 
 Use "hubble [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
