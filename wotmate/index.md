---
Title: wotmate
Homepage: https://github.com/mricon/wotmate
Repository: https://gitlab.com/kalilinux/packages/wotmate
Architectures: all
Version: 0.1+git20210512-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wotmate
 
  This package contains a reimplementation the defunct PGP pathfinder without
  needing anything other than your own keyring.
   
  Currently, the following tools are available:
   * graph-paths.py: Draws the shortest path between each key you have
     personally signed and the target key. For simpler setups, it exactly
     mirrors the web of trust, but the resulting graph is not necessarily
     one-to-one (because you can assign ownertrust to a key you did not directly
     sign).
   * graph-to-full.py: Very similar, but finds shortest paths to each
     fully-trusted key in your keyring. Handy for open-source projects where
     someone maintains a "web of trust."
 
 **Installed size:** `201 KB`  
 **How to install:** `sudo apt install wotmate`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * python3
 * python3-pydotplus
 {{< /spoiler >}}
 
 ##### wotmate
 
 
 ```
 root@kali:~# wotmate -h
 
 > wotmate ~ reimplement the defunct PGP pathfinder with only your own keyring
 
 /usr/share/wotmate
 |-- export-keyring.py
 |-- graph-paths.py
 |-- graph-to-full.py
 |-- make-sqlitedb.py
 `-- wotmate
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
