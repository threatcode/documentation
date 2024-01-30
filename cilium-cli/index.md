---
Title: cilium-cli
Homepage: https://github.com/cilium/cilium-cli
Repository: https://gitlab.com/kalilinux/packages/cilium-cli
Architectures: any
Version: 0.15.14-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cilium-cli
 
  This package contains a CLI to install, manage & troubleshoot Kubernetes
  clusters running Cilium.
 
 **Installed size:** `124.75 MB`  
 **How to install:** `sudo apt install cilium-cli`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### cilium
 
 
 ```
 root@kali:~# cilium -h
 CLI to install, manage, & troubleshooting Cilium clusters running Kubernetes.
 
 Cilium is a CNI for Kubernetes to provide secure network connectivity and
 load-balancing with excellent visibility using eBPF
 
 Examples:
 # Install Cilium in current Kubernetes context
 cilium install
 
 # Check status of Cilium
 cilium status
 
 # Enable the Hubble observability layer
 cilium hubble enable
 
 # Perform a connectivity test
 cilium connectivity test
 
 Usage:
   cilium [flags]
   cilium [command]
 
 Available Commands:
   bgp          Access to BGP control plane
   clustermesh  Multi Cluster Management
   completion   Generate the autocompletion script for the specified shell
   config       Manage Configuration
   connectivity Connectivity troubleshooting
   context      Display the configuration context
   help         Help about any command
   hubble       Hubble observability
   install      Install Cilium in a Kubernetes cluster using Helm
   status       Display status
   sysdump      Collects information required to troubleshoot issues with Cilium and Hubble
   uninstall    Uninstall Cilium using Helm
   upgrade      Upgrade a Cilium installation a Kubernetes cluster using Helm
   version      Display detailed version information
 
 Flags:
       --context string     Kubernetes configuration context
   -h, --help               help for cilium
   -n, --namespace string   Namespace Cilium is running in (default "kube-system")
 
 Use "cilium [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
