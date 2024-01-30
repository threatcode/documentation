---
Title: evil-winrm
Homepage: https://github.com/Hackplayers/evil-winrm
Repository: https://gitlab.com/kalilinux/packages/evil-winrm
Architectures: all
Version: 3.5-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: images/evil-winrm-logo.svg
PackagesInfo: |
 ### evil-winrm
 
  This package contains the ultimate WinRM shell for hacking/pentesting.
   
  WinRM (Windows Remote Management) is the Microsoft implementation of
  WS-Management Protocol. A standard SOAP based protocol that allows hardware
  and operating systems from different vendors to interoperate. Microsoft
  included it in their Operating Systems in order to make life easier to system
  administrators.
   
  This program can be used on any Microsoft Windows Servers with this feature
  enabled (usually at port 5985), of course only if you have credentials and
  permissions to use it. So it could be used in a post-exploitation
  hacking/pentesting phase. The purpose of this program is to provide nice and
  easy-to-use features for hacking. It can be used with legitimate purposes by
  system administrators as well but the most of its features are focused on
  hacking/pentesting stuff.
   
  It is using PSRP (Powershell Remoting Protocol) for initializing runspace
  pools as well as creating and processing pipelines.
 
 **Installed size:** `139 KB`  
 **How to install:** `sudo apt install evil-winrm`  
 
 {{< spoiler "Dependencies:" >}}
 * ruby
 * ruby-fileutils
 * ruby-logger
 * ruby-stringio
 * ruby-winrm
 * ruby-winrm-fs
 {{< /spoiler >}}
 
 ##### evil-winrm
 
 
 ```
 root@kali:~# evil-winrm -h
                                         
 Evil-WinRM shell v3.5
 
 Usage: evil-winrm -i IP -u USER [-s SCRIPTS_PATH] [-e EXES_PATH] [-P PORT] [-p PASS] [-H HASH] [-U URL] [-S] [-c PUBLIC_KEY_PATH ] [-k PRIVATE_KEY_PATH ] [-r REALM] [--spn SPN_PREFIX] [-l]
     -S, --ssl                        Enable ssl
     -c, --pub-key PUBLIC_KEY_PATH    Local path to public key certificate
     -k, --priv-key PRIVATE_KEY_PATH  Local path to private key certificate
     -r, --realm DOMAIN               Kerberos auth, it has to be set also in /etc/krb5.conf file using this format -> CONTOSO.COM = { kdc = fooserver.contoso.com }
     -s, --scripts PS_SCRIPTS_PATH    Powershell scripts local path
         --spn SPN_PREFIX             SPN prefix for Kerberos auth (default HTTP)
     -e, --executables EXES_PATH      C# executables local path
     -i, --ip IP                      Remote host IP or hostname. FQDN for Kerberos auth (required)
     -U, --url URL                    Remote url endpoint (default /wsman)
     -u, --user USER                  Username (required if not using kerberos)
     -p, --password PASS              Password
     -H, --hash HASH                  NTHash
     -P, --port PORT                  Remote host port (default 5985)
     -V, --version                    Show version
     -n, --no-colors                  Disable colors
     -N, --no-rpath-completion        Disable remote path completion
     -l, --log                        Log the WinRM session
     -h, --help                       Display this help message
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
