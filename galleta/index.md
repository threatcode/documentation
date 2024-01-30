---
Title: galleta
Homepage: https://odessa.sourceforge.net/
Repository: https://salsa.debian.org/pkg-security-team/galleta
Architectures: any
Version: 1.0+20040505-12
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/galleta-logo.svg
PackagesInfo: |
 ### galleta
 
  Galleta is a forensics tool that examines the content of cookie files
  produced by Microsoft Internet Explorer (MSIE). It parses the file and
  outputs a field separated that can be loaded in a spreadsheet.
 
 **Installed size:** `31 KB`  
 **How to install:** `sudo apt install galleta`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### galleta
 
 Tool to extract information from MSIE cookie files
 
 ```
 root@kali:~# galleta -h
 Cookie File: -h
 
 ERROR - The cookie file cannot be opened!
 
 
 Usage:  galleta [options] <filename>
 	-d Field Delimiter (TAB by default)
 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## galleta Usage Example

Read `file.txt` and output the content using ; as Field Delimiter (`d`).

```
root@kali:~# galleta -d";" file.txt
```
