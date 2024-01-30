---
Title: kustomize
Homepage: https://github.com/kubernetes-sigs/kustomize
Repository: https://gitlab.com/kalilinux/packages/kustomize
Architectures: any
Version: 5.2.1-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### kustomize
 
  kustomize lets you customize raw, template-free YAML files for multiple
  purposes, leaving the original YAML untouched and usable as is.
   
  kustomize targets kubernetes; it understands and can patch kubernetes style
  API objects.  It's like make in that what it does is declared in a file, and
  it's like sed (https://www.gnu.org/software/sed), in that it emits edited
  text.
 
 **Installed size:** `19.01 MB`  
 **How to install:** `sudo apt install kustomize`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### kustomize
 
 
 ```
 root@kali:~# kustomize -h
 
 Manages declarative configuration of Kubernetes.
 See https://sigs.k8s.io/kustomize
 
 Usage:
   kustomize [command]
 
 Available Commands:
   build                     Build a kustomization target from a directory or URL
   cfg                       Commands for reading and writing configuration
   completion                Generate shell completion script
   create                    Create a new kustomization in the current directory
   edit                      Edits a kustomization file
   fn                        Commands for running functions against configuration
   help                      Help about any command
   localize                  [Alpha] Creates localized copy of target kustomization root at destination
   version                   Prints the kustomize version
 
 Flags:
   -h, --help          help for kustomize
       --stack-trace   print a stack-trace on error
 
 Additional help topics:
   kustomize docs-fn                   [Alpha] Documentation for developing and invoking Configuration Functions.
   kustomize docs-fn-spec              [Alpha] Documentation for Configuration Functions Specification.
   kustomize docs-io-annotations       [Alpha] Documentation for annotations used by io.
   kustomize docs-merge                [Alpha] Documentation for merging Resources (2-way merge).
   kustomize docs-merge3               [Alpha] Documentation for merging Resources (3-way merge).
   kustomize tutorials-command-basics  [Alpha] Tutorials for using basic config commands.
   kustomize tutorials-function-basics [Alpha] Tutorials for using functions.
 
 Use "kustomize [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
