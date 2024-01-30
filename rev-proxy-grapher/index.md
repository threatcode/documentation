---
Title: rev-proxy-grapher
Homepage: https://github.com/mricon/rev-proxy-grapher
Repository: https://gitlab.com/kalilinux/packages/rev-proxy-grapher
Architectures: all
Version: 0~git20180301-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rev-proxy-grapher
 
  This package contains a useful little tool that will generate a nice graphviz
  graph illustrating your reverse proxy flow. It takes a manually curated YAML
  file describing the topology of your network, proxy definitions, and
  optionally a collection of nmap output files for additional port/service
  information and output a graph in any format supported by graphviz.
 
 **Installed size:** `207 KB`  
 **How to install:** `sudo apt install rev-proxy-grapher`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-netaddr
 * python3-nmap
 * python3-pydotplus
 * python3-yaml
 {{< /spoiler >}}
 
 ##### rev-proxy-grapher
 
 
 ```
 root@kali:~# rev-proxy-grapher -h
 usage: rev-proxy-grapher [-h] --topology TOPOLOGY [--resolve-dns]
                          [--nmap-xml NMAP_XML [NMAP_XML ...]]
                          [--limit-ext LIMIT_EXT [LIMIT_EXT ...]] [--font FONT]
                          [--fontsize FONTSIZE] [--ranksep RANKSEP] [--out OUT]
                          [--verbose]
 
 Draw a nice graph of your external to internal proxies
 
 options:
   -h, --help            show this help message and exit
   --topology TOPOLOGY   File describing the proxies and the topology of your
                         networks (default: topology.yaml)
   --resolve-dns         Attempt to resolve DNS for all IPs (default: False)
   --nmap-xml NMAP_XML [NMAP_XML ...]
                         Get additional node details from these nmap XML scan
                         files (default: ())
   --limit-ext LIMIT_EXT [LIMIT_EXT ...]
                         Only include these source IPs or networks (default:
                         ())
   --font FONT           Font to use in the graph (default: droid sans,dejavu
                         sans,helvetica)
   --fontsize FONTSIZE   Font size to use in the graph (default: 11)
   --ranksep RANKSEP     Node separation between columns (default: 1)
   --out OUT             Write graph into this file, guessing the output format
                         by extension (default: graph.png)
   --verbose             Be more verbose (default: False)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
