---
Title: sqldict
Homepage: https://ntsecurity.nu/toolbox/sqldict/
Repository: https://gitlab.com/kalilinux/packages/sqldict
Architectures: all
Version: 2.1-1kali5
Metapackages: kali-linux-everything kali-linux-large kali-tools-database kali-tools-passwords kali-tools-web 
Icon: images/sqldict-logo.svg
PackagesInfo: |
 ### sqldict
 
  SQLdict is a dictionary attack tool for SQL Server.
 
 **Installed size:** `145 KB`  
 **How to install:** `sudo apt install sqldict`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 * wine
 {{< /spoiler >}}
 
 ##### sqldict
 
 
 ```
 root@kali:~# sqldict -h
 ┏━(Message from Kali developers)
 ┃
 ┃ You may need to install the wine32 package first:
 ┃  # dpkg --add-architecture i386 && apt update && apt -y install wine32
 ┃
 ┗━
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
sqldict
```

![sqldict](images/sqldict.png)
