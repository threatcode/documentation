---
Title: calico
Homepage: https://github.com/projectcalico/calico
Repository: https://gitlab.com/kalilinux/packages/calico
Architectures: any
Version: 3.26.4+ds-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### calicoctl
 
  This package contains the command line tool for calico. Calico is a widely
  adopted, battle-tested open source networking and network security solution
  for Kubernetes, virtual machines, and bare-metal workloads.
 
 **Installed size:** `42.19 MB`  
 **How to install:** `sudo apt install calicoctl`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### calicoctl
 
 
 ```
 root@kali:~# calicoctl -h
 Usage:
   calicoctl [options] <command> [<args>...]
 
     create       Create a resource by file, directory or stdin.
     replace      Replace a resource by file, directory or stdin.
     apply        Apply a resource by file, directory or stdin.  This creates a resource
                  if it does not exist, and replaces a resource if it does exists.
     patch        Patch a pre-exisiting resource in place.
     delete       Delete a resource identified by file, directory, stdin or resource type and
                  name.
     get          Get a resource identified by file, directory, stdin or resource type and
                  name.
     label        Add or update labels of resources.
     convert      Convert config files between different API versions.
     ipam         IP address management.
     node         Calico node management.
     version      Display the version of this binary.
     datastore    Calico datastore management.
 
 Options:
   -h --help                    Show this screen.
   -l --log-level=<level>       Set the log level (one of panic, fatal, error,
                                warn, info, debug) [default: panic]
      --context=<context>       The name of the kubeconfig context to use.
      --allow-version-mismatch  Allow client and cluster versions mismatch.
 
 Description:
   The calicoctl command line tool is used to manage Calico network and security
   policy, to view and manage endpoint configuration, and to manage a Calico
   node instance.
 
   See 'calicoctl <command> --help' to read about a specific subcommand.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
