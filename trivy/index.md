---
Title: trivy
Homepage: https://github.com/aquasecurity/trivy
Repository: https://gitlab.com/kalilinux/packages/trivy
Architectures: any
Version: 0.46.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### trivy
 
  This package contains a comprehensive and versatile security scanner. Trivy
  has scanners that look for security issues, and targets where it can find
  those issues.
  It can find vulnerabilities, misconfigurations, secrets, SBOM in containers,
  Kubernetes, code repositories, clouds and more.
   
  Targets (what Trivy can scan):
   
   * Container Image
   * Filesystem
   * Git Repository (remote)
   * Virtual Machine Image
   * Kubernetes
   * AWS
   
  Scanners (what Trivy can find there):
   
   * OS packages and software dependencies in use (SBOM)
   * Known vulnerabilities (CVEs)
   * IaC issues and misconfigurations
   * Sensitive information and secrets
   * Software licenses
 
 **Installed size:** `238.71 MB`  
 **How to install:** `sudo apt install trivy`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### trivy
 
 
 ```
 root@kali:~# trivy -h
 Scanner for vulnerabilities in container images, file systems, and Git repositories, as well as for configuration issues and hard-coded secrets
 
 Usage:
   trivy [global flags] command [flags] target
   trivy [command]
 
 Examples:
   # Scan a container image
   $ trivy image python:3.4-alpine
 
   # Scan a container image from a tar archive
   $ trivy image --input ruby-3.1.tar
 
   # Scan local filesystem
   $ trivy fs .
 
   # Run in server mode
   $ trivy server
 
 Scanning Commands
   aws         [EXPERIMENTAL] Scan AWS account
   config      Scan config files for misconfigurations
   filesystem  Scan local filesystem
   image       Scan a container image
   kubernetes  [EXPERIMENTAL] Scan kubernetes cluster
   repository  Scan a repository
   rootfs      Scan rootfs
   sbom        Scan SBOM for vulnerabilities
   vm          [EXPERIMENTAL] Scan a virtual machine image
 
 Management Commands
   module      Manage modules
   plugin      Manage plugins
 
 Utility Commands
   completion  Generate the autocompletion script for the specified shell
   convert     Convert Trivy JSON report into a different format
   help        Help about any command
   server      Server mode
   version     Print the version
 
 Flags:
       --cache-dir string          cache directory (default "/root/.cache/trivy")
   -c, --config string             config path (default "trivy.yaml")
   -d, --debug                     debug mode
   -f, --format string             version format (json)
       --generate-default-config   write the default config to trivy-default.yaml
   -h, --help                      help for trivy
       --insecure                  allow insecure server connections
   -q, --quiet                     suppress progress bar and log output
       --timeout duration          timeout (default 5m0s)
   -v, --version                   show version
 
 Use "trivy [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
