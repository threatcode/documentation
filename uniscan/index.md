---
Title: uniscan
Homepage: https://sourceforge.net/projects/uniscan/
Repository: https://gitlab.com/kalilinux/packages/uniscan
Architectures: all
Version: 6.3-0kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### uniscan
 
  Uniscan is a simple Remote File Include, Local File Include and Remote
  Command Execution vulnerability scanner.
 
 **Installed size:** `1.19 MB`  
 **How to install:** `sudo apt install uniscan`  
 
 {{< spoiler "Dependencies:" >}}
 * libmoose-perl
 * perl
 * perl-tk
 {{< /spoiler >}}
 
 ##### uniscan
 
 
 ```
 root@kali:~# uniscan -h
 ####################################
 # Uniscan project                  #
 # http://uniscan.sourceforge.net/  #
 ####################################
 V. 6.3
 
 
 OPTIONS:
 	-h 	help
 	-u 	<url> example: https://www.example.com/
 	-f 	<file> list of url's
 	-b 	Uniscan go to background
 	-q 	Enable Directory checks
 	-w 	Enable File checks
 	-e 	Enable robots.txt and sitemap.xml check
 	-d 	Enable Dynamic checks
 	-s 	Enable Static checks
 	-r 	Enable Stress checks
 	-i 	<dork> Bing search
 	-o 	<dork> Google search
 	-g 	Web fingerprint
 	-j 	Server fingerprint
 
 usage: 
 [1] perl ./uniscan.pl -u http://www.example.com/ -qweds
 [2] perl ./uniscan.pl -f sites.txt -bqweds
 [3] perl ./uniscan.pl -i uniscan
 [4] perl ./uniscan.pl -i "ip:xxx.xxx.xxx.xxx"
 [5] perl ./uniscan.pl -o "inurl:test"
 [6] perl ./uniscan.pl -u https://www.example.com/ -r
 
 
 ```
 
 - - -
 
 ##### uniscan-gui
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
uniscan-gui
```

![uniscan](images/uniscan.png)

## uniscan Usage Example

Scan the given URL (`-u http://192.168.1.202/`) for vulnerabilities, enabling directory and dynamic checks (`-qd`):

```
root@kali:~# uniscan -u http://192.168.1.202/ -qd
####################################
# Uniscan project                  #
# http://uniscan.sourceforge.net/  #
####################################
V. 6.2


Scan date: 16-5-2014 16:29:48
===================================================================================================
| Domain: http://192.168.1.202/
| Server: Apache/2.2.22 (Debian)
| IP: 192.168.1.202
===================================================================================================
|
| Directory check:
| [+] CODE: 200 URL: http://192.168.1.202/joomla/
| [+] CODE: 200 URL: http://192.168.1.202/wordpress/
===================================================================================================
|
| Crawler Started:
| Plugin name: FCKeditor upload test v.1 Loaded.
| Plugin name: Web Backdoor Disclosure v.1.1 Loaded.
| Plugin name: phpinfo() Disclosure v.1 Loaded.
| Plugin name: E-mail Detection v.1.1 Loaded.
| Plugin name: Timthumb <= 1.32 vulnerability v.1 Loaded.
| Plugin name: Code Disclosure v.1.1 Loaded.
| Plugin name: Upload Form Detect v.1.1 Loaded.
| Plugin name: External Host Detect v.1.2 Loaded.
| [+] Crawling finished, 27 URL's found!
```
