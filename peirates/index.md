---
Title: peirates
Homepage: https://github.com/inguardians/peirates
Repository: https://gitlab.com/kalilinux/packages/peirates
Architectures: any
Version: 1.1.14-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### peirates
 
  This package contains a Kubernetes penetration tool, enables an attacker to
  escalate privilege and pivot through a Kubernetes cluster. It automates known
  techniques to steal and collect service accounts, obtain further code
  execution, and gain control of the cluster.
 
 **Installed size:** `41.79 MB`  
 **How to install:** `sudo apt install peirates`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### peirates
 
 
 ```
 root@kali:~# peirates -h
 Usage of peirates:
   -L string
     	List of comma-seperated Pods: ex pod1,pod2,pod3
   -c string
     	Command to run in pods (default "hostname")
   -t string
     	Token (JWT)
   -u string
     	API Server URL: ex. https://10.96.0.1:6443 (default "https://:")
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
