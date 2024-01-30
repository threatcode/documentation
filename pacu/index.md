---
Title: pacu
Homepage: https://rhinosecuritylabs.com/aws/pacu-open-source-aws-exploitation-framework/
Repository: https://gitlab.com/kalilinux/packages/pacu
Architectures: all
Version: 1.1.5-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pacu
 
  This package contains an open-source AWS exploitation framework, designed for
  offensive security testing against cloud environments. Created and maintained
  by Rhino Security Labs, Pacu allows penetration testers to exploit
  configuration flaws within an AWS account, using modules to easily expand its
  functionality. Current modules enable a range of attacks, including user
  privilege escalation, backdooring of IAM users, attacking vulnerable Lambda
  functions, and much more.
 
 **Installed size:** `13.08 MB`  
 **How to install:** `sudo apt install pacu`  
 
 {{< spoiler "Dependencies:" >}}
 * awscli
 * python3
 * python3-boto3
 * python3-botocore
 * python3-dsnap
 * python3-freezegun
 * python3-requests
 * python3-sqlalchemy 
 * python3-sqlalchemy-utils
 * python3-typing-extensions
 * python3-urllib3
 {{< /spoiler >}}
 
 ##### pacu
 
 
 ```
 root@kali:~# pacu -h
 usage: pacu [-h] [--session] [--activate-session] [--new-session] [--set-keys]
             [--module-name] [--data] [--module-args] [--list-modules]
             [--pacu-help] [--module-info] [--exec] [--set-regions  [...]]
             [--whoami]
 
 options:
   -h, --help            show this help message and exit
   --session             <session name>
   --activate-session    activate session, use session arg to set session name
   --new-session         <session name>
   --set-keys            alias, access id, secrect key, token
   --module-name         <module name>
   --data                <service name/all>
   --module-args         <--module-args='--regions us-east-1,us-east-1'>
   --list-modules        List arguments
   --pacu-help           List the Pacu help window
   --module-info         Get information on a specific module, use --module-
                         name
   --exec                exec module
   --set-regions  [ ...]
                         <region1 region2 ...> or <all> for all
   --whoami              Display information on current IAM user
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
