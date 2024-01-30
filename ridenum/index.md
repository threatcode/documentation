---
Title: ridenum
Homepage: https://github.com/trustedsec/ridenum
Repository: https://gitlab.com/kalilinux/packages/ridenum
Architectures: all
Version: 1.7-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ridenum
 
  Rid Enum is a RID cycling attack that attempts to enumerate user accounts
  through null sessions and the SID to RID enum. If you specify a password file,
  it will automatically attempt to brute force the user accounts when its
  finished enumerating.
 
 **Installed size:** `32 KB`  
 **How to install:** `sudo apt install ridenum`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-pexpect
 {{< /spoiler >}}
 
 ##### ridenum
 
 
 ```
 root@kali:~# ridenum -h
 
 .______       __   _______         _______ .__   __.  __    __  .___  ___.
 |   _  \     |  | |       \       |   ____||  \ |  | |  |  |  | |   \/   |
 |  |_)  |    |  | |  .--.  |      |  |__   |   \|  | |  |  |  | |  \  /  |
 |      /     |  | |  |  |  |      |   __|  |  . `  | |  |  |  | |  |\/|  |
 |  |\  \----.|  | |  '--'  |      |  |____ |  |\   | |  `--'  | |  |  |  |
 | _| `._____||__| |_______/  _____|_______||__| \__|  \______/  |__|  |__|
                             |______|
 
 Written by: David Kennedy (ReL1K)
 Company: https://www.trustedsec.com
 Twitter: @TrustedSec
 Twitter: @HackingDave
 
 Rid Enum is a RID cycling attack that attempts to enumerate user accounts through
 null sessions and the SID to RID enum. If you specify a password file, it will
 automatically attempt to brute force the user accounts when its finished enumerating.
 
 - RIDENUM is open source and uses all standard python libraries minus python-pexpect. -
 
 You can also specify an already dumped username file, it needs to be in the DOMAINNAME\USERNAME
 format.
 
 Example: ./ridenum.py 192.168.1.50 500 50000 /root/dict.txt /root/user.txt
 
 Usage: ./ridenum.py <server_ip> <start_rid> <end_rid> <optional_username> <optional_password> <optional_password_file> <optional_username_filename>
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## ridenum Usage Example

Connect to the remote server (`192.168.1.236`) and cycle from RID 500 to 50000 (`500 50000`), using the given password file (`/tmp/passes.txt`):

```
root@kali:~# ridenum 192.168.1.236 500 50000 /tmp/passes.txt
[*] Attempting lsaquery first...This will enumerate the base domain SID
[*] Successfully enumerated base domain SID.. Moving on to extract via RID
[*] Enumerating user accounts.. This could take a little while.
```
