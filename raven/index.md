---
Title: raven
Homepage: https://github.com/gh0x0st/raven
Repository: https://gitlab.com/kalilinux/packages/raven
Architectures: all
Version: 1.0.1-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### raven
 
  This package contains a Python tool that extends the capabilities of the
  http.server Python module by offering a self-contained file upload web server.
  While the common practice is to use python3 -m http.server 80 to serve files
  for remote client downloads, Raven addresses the need for a similar solution
  when you need the ability to receive files from remote clients. This becomes
  especially valuable in scenarios such as penetration testing and incident
  response procedures when protocols such as SMB may not be a viable option.
 
 **Installed size:** `39 KB`  
 **How to install:** `sudo apt install raven`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### raven
 
 
 ```
 root@kali:~# raven -h
 usage: python3 raven.py <listening_ip> <listening_port> [--allowed-ip <allowed_client_ip>] [--upload-folder <upload_directory>] [--organize-uploads]
 
 A lightweight file upload service used for penetration testing and incident
 response.
 
 positional arguments:
   host                  The IP address for our http handler to listen on
   port                  The port for our http handler to listen on
 
 options:
   -h, --help            show this help message and exit
   --allowed-ip ALLOWED_IP
                         Restrict access to our http handler by IP address
                         (optional)
   --upload-folder UPLOAD_FOLDER
                         Designate the directory to save uploaded files to
                         (default: current working directory)
   --organize-uploads    Organize file uploads into subfolders by remote client
                         IP
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
