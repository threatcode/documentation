---
Title: jsp-file-browser
Homepage: https://www.vonloesch.de/filebrowser.html
Repository: https://gitlab.com/kalilinux/packages/jsp-file-browser
Architectures: all
Version: 1.2-0kali4
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### jsp-file-browser
 
  This package contains an easy to use and easy to install file browser java
  server page. This JSP program allows remote web-based file access and
  manipulation. Features:
     - Create, copy, move, rename and delete files and directories
     - Shortkeys
     - View Files (pictures, movies, pdf, html,...)
     - Javascript filename filter
     - Edit textfiles
     - Upload files to the server (Status via Upload monitor)
     - Download files from the server
     - Download groups of files and folders as a single zip file that is created
       on the fly
     - Execute native commands on the server (e.g ls, tar, chmod,...)
     - View entries and unpack zip, jar, war and gz files on the server
     - Just one file, very easy to install (in fact, just copy it to the server)
     - Customizable layout via css file
     - Restrict file access via black or whitelist
     - Changeable to a read-only (with or without upload) solution
  Jsp file browser should work on any JSP1.1 compatible server (e.g.
  Tomcat>=3.0). It has been tested on Tomcat 4.0 and 5.5, Resin 2.1.7 and Jetty.
 
 **Installed size:** `93 KB`  
 **How to install:** `sudo apt install jsp-file-browser`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 {{< /spoiler >}}
 
 ##### jsp-file-browser
 
 
 ```
 root@kali:~# jsp-file-browser -h
 
 > jsp-file-browser ~ File browser java server page
 
 /usr/share/jsp-file-browser
 |-- Browser.jsp
 `-- example-css.css
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
