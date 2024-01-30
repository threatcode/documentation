---
Title: tnscmd10g
Homepage: http://www.red-database-security.com/
Repository: https://gitlab.com/kalilinux/packages/tnscmd10g
Architectures: all
Version: 1.3-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-database kali-tools-web 
Icon: images/tnscmd10g-logo.svg
PackagesInfo: |
 ### tnscmd10g
 
  A tool to prod the oracle tnslsnr process
  on port 1521/tcp.
 
 **Installed size:** `18 KB`  
 **How to install:** `sudo apt install tnscmd10g`  
 
 {{< spoiler "Dependencies:" >}}
 * libio-socket-ip-perl
 * perl
 {{< /spoiler >}}
 
 ##### tnscmd10g
 
 
 ```
 root@kali:~# tnscmd10g -h
 usage: /usr/bin/tnscmd10g [command] -h hostname
        where 'command' is something like ping, version, status, etc.  
        (default is ping)
        [-p port] - alternate TCP port to use (default is 1521)
        [--logfile logfile] - write raw packets to specified logfile
        [--indent] - indent & outdent on parens
        [--10G] - make it work against 10G
        [--rawcmd command] - build your own CONNECT_DATA string
        [--cmdsize bytes] - fake TNS command size (reveals packet leakage)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## tnscmd10g Usage Example

Retrieve the version (`version`) from the target server (`-h 192.168.1.205`):

```
root@kali:~# tnscmd10g version -h 192.168.1.205
sending (CONNECT_DATA=(COMMAND=version)) to 192.168.1.205:1521
writing 90 bytes
reading
.M.......6.........-. ..........(DESCRIPTION=(TMP=)(VSNNUM=153092352)(ERR=0)).7........TNSLSNR for 32-bit Windows: Version 9.2.0.1.0 - Production..TNS for 32-bit Windows: Version 9.2.0.1.0 - Production..Windows NT Named Pipes NT Protocol Adapter for 32-bit Windows: Version 9.2.0.1.0 - Production..Windows NT TCP/IP NT Protocol Adapter for 32-bit Windows: Version 9.2.0.1.0 - Production,,.........@
```
