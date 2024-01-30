---
Title: spire
Homepage: https://github.com/spiffe/spire
Repository: https://gitlab.com/kalilinux/packages/spire
Architectures: any
Version: 1.7.2-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### spire
 
  This package contains SPIRE (the SPIFFE Runtime Environment). It is a
  toolchain of APIs for establishing trust between software systems across a
  wide variety of hosting platforms. SPIRE exposes the SPIFFE Workload API,
  which can attest running software systems and issue SPIFFE IDs and SVIDs to
  them. This in turn allows two workloads to establish trust between each other,
  for example by establishing an mTLS connection or by signing and verifying a
  JWT token. SPIRE can also enable workloads to securely authenticate to a
  secret store, a database, or a cloud provider service.
 
 **Installed size:** `158.09 MB`  
 **How to install:** `sudo apt install spire`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### spire-agent
 
 
 ```
 root@kali:~# spire-agent -h
 Usage: spire-agent [--version] [--help] <command> [<args>]
 
 Available commands are:
     api            
     healthcheck    Determines agent health status
     run            Runs the agent
     validate       Validates a SPIRE agent configuration file
 
 ```
 
 - - -
 
 ##### spire-server
 
 
 ```
 root@kali:~# spire-server -h
 Usage: spire-server [--version] [--help] <command> [<args>]
 
 Available commands are:
     agent          
     bundle         
     entry          
     federation     
     healthcheck    Determines server health status
     jwt            
     run            Runs the server
     token          
     validate       Validates a SPIRE server configuration file
     x509           
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
