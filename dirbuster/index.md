---
Title: dirbuster
Homepage: https://www.owasp.org/index.php/Category:OWASP_DirBuster_Project
Repository: https://gitlab.com/kalilinux/packages/dirbuster
Architectures: all
Version: 1.0-1kali6
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-vulnerability kali-tools-web 
Icon: images/dirbuster-logo.svg
PackagesInfo: |
 ### dirbuster
 
  DirBuster is a multi threaded java application designed to
  brute force directories and files names on web/application
  servers. Often is the case now of what looks like a web
  server in a state of default installation is actually not,
  and has pages and applications hidden within. DirBuster
  attempts to find these.
   
  However tools of this nature are often as only good as the
  directory and file list they come with. A different
  approach was taken to generating this. The list was
  generated from scratch, by crawling the Internet and
  collecting the directory and files that are actually used
  by developers! DirBuster comes a total of 9 different
  lists, this makes DirBuster extremely effective at finding
  those hidden files and directories. And if that was not
  enough DirBuster also has the option to perform a pure
  brute force, which leaves the hidden directories and files
  nowhere to hide.
 
 **Installed size:** `10.75 MB`  
 **How to install:** `sudo apt install dirbuster`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 {{< /spoiler >}}
 
 ##### dirbuster
 
 
 ```
 root@kali:~# dirbuster -h
 DirBuster - 1.0-RC1
 Usage: java -jar DirBuster-1.0-RC1 -u <URL http://example.com/> [Options]
 
 	Options:
 	 -h : Display this help message
 	 -H : Start DirBuster in headless mode (no gui), report will be auto saved on exit
 	 -l <Word list to use> : The Word list to use for the list based brute force. Default: /home/kali/kali-www/bin/kali-tools/tool-output/dirbuster/directory-list-2.3-small.txt
 	 -g : Only use GET requests. Default Not Set
 	 -e <File Extention list> : File Extention list eg asp,aspx. Default: php
 	 -t <Number of Threads> : Number of connection threads to use. Default: 10
 	 -s <Start point> : Start point of the scan. Default: /
 	 -v : Verbose output, Default: Not set
 	 -P : Don't Parse html, Default: Not Set
 	 -R : Don't be recursive, Default: Not Set
 	 -r <location> : File to save report to. Default: /home/kali/kali-www/bin/kali-tools/tool-output/dirbuster/DirBuster-Report-[hostname]-[port].txt
 
 Examples:
 
 Run DirBuster in headless mode
 java -jar DirBuster-1.0-RC1.jar -H -u https://www.target.com/
 
 Start GUI with target prepopulated
 java -jar DirBuster-1.0-RC1.jar -u https://www.target.com/
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
dirbuster
```

![dirbuster](images/dirbuster.png)
