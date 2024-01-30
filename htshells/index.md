---
Title: htshells
Homepage: https://github.com/wireghoul/htshells
Repository: https://gitlab.com/kalilinux/packages/htshells
Architectures: all
Version: 0.1~git20131205-1kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### htshells
 
  htshells is a series of web based attacks based around the .htaccess files.
  Most of the attacks are centered around two attack categories. Remote code/
  command execution and information disclosure. These attacks are intended for
  use during penetration tests or security assessments. It was created to get
  shell in a CMS that restricted uploads based on extension and placed each
  uploaded file in it's own directory.
 
 **Installed size:** `56 KB`  
 **How to install:** `sudo apt install htshells`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 {{< /spoiler >}}
 
 ##### htshells
 
 
 ```
 root@kali:~# htshells -h
 
 > htshells ~ Self contained htaccess shells and attacks
 
 /usr/share/htshells
 |-- dos
 |-- info
 |-- mod_auth_remote.phish.htaccess
 |-- mod_badge.admin.htaccess
 |-- mod_sendmail.rce.htaccess
 |-- shell
 `-- traversal
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
