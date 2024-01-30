---
Title: spray
Homepage: https://github.com/Greenwolf/Spray
Repository: https://gitlab.com/kalilinux/packages/spray
Architectures: all
Version: 2.1+git20190226-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### spray
 
  This package contains a Password Spraying tool for Active Directory
  Credentials. The script will password spray a target over a period of time. It
  requires password policy as input so accounts are not locked out.
   
  The package also provides a series of hand crafted password files for
  multiple languages. These have been crafted from the most common active
  directory passwords in various languages and all fit in the complex (1 Upper, 1
  lower, 1 digit) category.
 
 **Installed size:** `39.01 MB`  
 **How to install:** `sudo apt install spray`  
 
 {{< spoiler "Dependencies:" >}}
 * curl
 * smbclient
 {{< /spoiler >}}
 
 ##### spray
 
 
 ```
 root@kali:~# spray -h
 
 Spray 2.1 the Password Sprayer by Jacob Wilkin(Greenwolf)
 
 This script will password spray a target over a period of time
 It requires password policy as input so accounts are not locked out
 Usage: spray -smb <targetIP> <usernameList> <passwordList> <AttemptsPerLockoutPeriod> <LockoutPeriodInMinutes> <Domain>
 Example: spray -smb 192.168.0.1 users.txt passwords.txt 1 35 CORPORATION
 
 To password spray an OWA portal, a file must be created of the POST request with Username: sprayuser@domain.com, and Password: spraypassword
 Usage: spray -owa <targetIP> <usernameList> <passwordList> <AttemptsPerLockoutPeriod> <LockoutPeriodInMinutes> <RequestFile>
 Example: spray -owa 192.168.0.1 usernames.txt passwords.txt 1 35 post-request.txt
 
 To password spray an lync service, a lync autodiscover url or a url that returns the www-authenticate header must be provided along with a list of email addresses
 Usage: spray -lync <lyncDiscoverOrAutodiscoverUrl> <emailAddressList> <passwordList> <AttemptsPerLockoutPeriod> <LockoutPeriodInMinutes>
 Example: spray -lync https://lyncdiscover.company.com/ emails.txt passwords.txt 1 35\n
 Example: spray -lync https://lyncweb.company.com/Autodiscover/AutodiscoverService.svc/root/oauth/user emails.txt passwords.txt 1 35
 
 To password spray an CISCO Web VPN a target portal or server hosting a portal must be provided
 Usage: spray -cisco <targetURL> <usernameList> <passwordList> <AttemptsPerLockoutPeriod> <LockoutPeriodInMinutes>
 Example: spray -cicso 192.168.0.1 usernames.txt passwords.txt 1 35
 
 
 It is also possible to update the supplied 2016/2017 password list to the current year
 Usage: spray -passupdate <passwordList>
 Example: spray -passupdate passwords.txt
 
 An optional company name can also be provided to add to the list:
 Usage: spray -passupdate <passwordList> <CompanyName>
 Example: spray -passupdate passwords.txt Company
 
 A username list can also be generated from a list of common names:
 Usage: spray -genusers <firstnames> <lastnames> "<<fi><li><fn><ln>>"
 Example: spray -genusers english-first-1000.txt english-last-1000.txt "<fi><ln>"
 Example: spray -genusers english-first-1000.txt english-last-1000.txt "<fn>.<ln>"
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
