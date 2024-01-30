---
Title: merlin
Homepage: https://github.com/Ne0nd0g/merlin
Repository: https://gitlab.com/kalilinux/packages/merlin
Architectures: any all
Version: 1.5.1+ds-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### golang-github-ne0nd0g-merlin-dev
 
  This package contains a cross-platform post-exploitation HTTP/2 Command &
  Control server written in golang.
   
  This package contains the source go files.
 
 **Installed size:** `516 KB`  
 **How to install:** `sudo apt install golang-github-ne0nd0g-merlin-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * golang-github-binject-go-donut-dev
 * golang-github-cheekybits-genny-dev
 * golang-github-chzyer-readline-dev
 * golang-github-cretz-gopaque-dev
 * golang-github-fatih-color-dev
 * golang-github-francoispqt-gojay-dev
 * golang-github-mattn-go-shellwords-dev
 * golang-github-ne0nd0g-ja3transport-dev
 * golang-github-olekukonko-tablewriter-dev
 * golang-github-quic-go-qpack-dev
 * golang-github-satori-go.uuid-dev
 * golang-go.dedis-kyber-dev
 * golang-golang-x-crypto-dev
 * golang-golang-x-exp-dev
 * golang-golang-x-net-dev
 * golang-golang-x-sync-dev
 * golang-golang-x-sys-dev
 * golang-gopkg-square-go-jose.v2-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### merlin
 
  This package contains a cross-platform post-exploitation HTTP/2 Command &
  Control server and agent written in golang as well as an
  identification tool.
 
 **Installed size:** `22 KB`  
 **How to install:** `sudo apt install merlin`  
 
 {{< spoiler "Dependencies:" >}}
 * merlin-agent
 * merlin-server
 {{< /spoiler >}}
 
 
 - - -
 
 ### merlin-server
 
  This package contains a cross-platform post-exploitation HTTP/2 Command &
  Control server written in golang.
 
 **Installed size:** `11.03 MB`  
 **How to install:** `sudo apt install merlin-server`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libjs-sphinxdoc 
 * sphinx-rtd-theme-common 
 {{< /spoiler >}}
 
 ##### merlinserver
 
 
 ```
 root@kali:~# merlinserver -h
 #################################################
 #		MERLIN SERVER			#
 #################################################
 Version: 1.5.1
 Build: nonRelease
 Merlin Server does not take any command line arguments
 Visit the Merlin wiki for additional information: https://merlin-c2.readthedocs.io/en/latest/
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
