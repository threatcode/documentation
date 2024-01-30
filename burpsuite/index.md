---
Title: burpsuite
Homepage: https://portswigger.net
Repository: https://gitlab.com/kalilinux/packages/burpsuite
Architectures: amd64 arm64
Version: 2023.10.3.5-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-linux-nethunter kali-tools-top10 kali-tools-web 
Icon: images/burpsuite-logo.svg
PackagesInfo: |
 ### burpsuite
 
  Burp Suite is an integrated platform for performing security
  testing of web applications. Its various tools work seamlessly
  together to support the entire testing process, from initial
  mapping and analysis of an application's attack surface,
  through to finding and exploiting security vulnerabilities.
   
  Burp gives you full control, letting you combine advanced
  manual techniques with state-of-the-art automation, to make
  your work faster, more effective, and more fun.
 
 **Installed size:** `251.20 MB`  
 **How to install:** `sudo apt install burpsuite`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 * java-wrappers
 {{< /spoiler >}}
 
 ##### burpsuite
 
 
 ```
 root@kali:~# burpsuite --help
 Usage:
 --help                            Print this message
 --version                         Print version details
 --disable-extensions              Prevent loading of extensions on startup
 --diagnostics                     Print diagnostic information
 --use-defaults                    Start with default settings
 --collaborator-server             Run in Collaborator server mode
 --collaborator-config             Specify Collaborator server configuration file; defaults to collaborator.config
 --data-dir                        Specify data directory
 --project-file                    Open the specified project file; this will be created as a new project if the file does not exist
 --developer-extension-class-name  Fully qualified name of locally-developed extension class; extension will be loaded from the classpath
 --config-file                     Load the specified project configuration file(s); this option may be repeated to load multiple files
 --user-config-file                Load the specified user configuration file(s); this option may be repeated to load multiple files
 --auto-repair                     Automatically repair a corrupted project file specified by the --project-file option
 --unpause-spider-and-scanner      Do not pause the Spider and Scanner when opening an existing project
 --disable-auto-update             Suppress auto update behavior
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
burpsuite
```

![burpsuite](images/burpsuite.png)
