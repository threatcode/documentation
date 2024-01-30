---
Title: gpp-decrypt
Homepage: http://carnal0wnage.attackresearch.com/2012/10/group-policy-preferences-and-getting.html
Repository: https://gitlab.com/kalilinux/packages/gpp-decrypt
Architectures: all
Version: 0.1-1kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gpp-decrypt
 
  A simple ruby script that will decrypt a given
  GPP encrypted string.
 
 **Installed size:** `11 KB`  
 **How to install:** `sudo apt install gpp-decrypt`  
 
 {{< spoiler "Dependencies:" >}}
 * ruby
 * rubygems
 {{< /spoiler >}}
 
 ##### gpp-decrypt
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## gpp-decrypt Usage Example

Decrypt the given Group Policy Preferences string (`j1Uyj3Vx8TY9LtLZil2uAuZkFQA/4latT76ZwgdHdhw`):

```
root@kali:~# gpp-decrypt j1Uyj3Vx8TY9LtLZil2uAuZkFQA/4latT76ZwgdHdhw
Local*P4ssword!
```
