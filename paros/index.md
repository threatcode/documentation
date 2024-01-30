---
Title: paros
Homepage: http://www.parosproxy.org/index.shtml
Repository: https://gitlab.com/kalilinux/packages/paros
Architectures: all
Version: 3.2.13-1kali6
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: images/paros-logo.svg
PackagesInfo: |
 ### paros
 
  Lightweight web application testing proxy
 
 **Installed size:** `7.99 MB`  
 **How to install:** `sudo apt install paros`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 * java-wrappers
 {{< /spoiler >}}
 
 ##### paros
 
 
 ```
 root@kali:~# paros -h
 file:/usr/share/paros/paros.jar
 file:/usr/share/paros/paros.jar
 GUI usage:
 	javaw paros.jar
 	java -jar paros.jar
 see java -jar paros.jar {-h|-help} for detail.
 
 Command line usage:
 java -jar paros.jar {-h|-help} {-newsession session_file_path} {options}
 options:
 
 -spider : run spider.  See other parameters
 -seed {URL1} {URL2} ... : Add seeds to the spider for crawling.
 -scan : Run vulnerability scan depending on previously saved policy.
 -last_scan_report [file_path]: Generate 'Last Scan Report' into the file_path provided.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
paros
```

![paros](images/paros.png)
