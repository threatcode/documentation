---
Title: bloodhound
Homepage: https://github.com/BloodHoundAD/BloodHound
Repository: https://gitlab.com/kalilinux/packages/bloodhound
Architectures: amd64 arm64
Version: 4.3.1-0kali2
Metapackages: kali-linux-everything 
Icon: images/bloodhound-logo.svg
PackagesInfo: |
 ### bloodhound
 
  This package contains BloodHound, a single page Javascript web application.
  BloodHound uses graph theory to reveal the hidden and often unintended
  relationships within an Active Directory environment. Attackers can use
  BloodHound to easily identify highly complex attack paths that would otherwise
  be impossible to quickly identify. Defenders can use BloodHound to identify and
  eliminate those same attack paths. Both blue and red teams can use BloodHound
  to easily gain a deeper understanding of privilege relationships in an Active
  Directory environment.
 
 **Installed size:** `261.45 MB`  
 **How to install:** `sudo apt install bloodhound`  
 
 {{< spoiler "Dependencies:" >}}
 * neo4j
 {{< /spoiler >}}
 
 ##### bloodhound
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## How to install and run Bloodhound

Install Bloodhound from the apt repository with:

```console
┌──(kali㉿kali)-[~]
└─$ sudo apt update && sudo apt install -y bloodhound
```

After installation completes, start neo4j with the following command:

```console
┌──(kali㉿kali)-[~]
└─$ sudo neo4j console
```

![](images/start-neo4j.png)

Now we need to change the default credentials for neo4j. Navigate to `http://localhost:7474/` and login with the default credentials

```plain
username: neo4j
password: neo4j
```

![](images/login-neo4j.png)

After logging in, you will be asked to change the default password with a new one. You need this password to later login in the Bloodhound interface.

![](images/neo4j-change-password.png)

Now that the password has been successfully modified you can finally launch Bloodhound with the new credentials.

![](images/bloodhound-login.png)
