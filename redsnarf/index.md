---
Title: redsnarf
Homepage: https://github.com/nccgroup/redsnarf
Repository: https://gitlab.com/kalilinux/packages/redsnarf
Architectures: all
Version: 0~git20170822-0kali5
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### redsnarf
 
  This package contains a pentesting / redteaming tool by Ed Williams for
  retrieving hashes and credentials from Windows workstations, servers and domain
  controllers using OpSec Safe Techniques.  RedSnarf functionality includes:
    * Retrieval of local SAM hashes
    * Enumeration of user/s running with elevated system privileges and their
      corresponding lsa secrets password;
    * Retrieval of MS cached credentials;
    * Pass-the-hash;
    * Quickly identify weak and guessable username/password combinations
      (default of administrator/Password01);
    * The ability to retrieve hashes across a range;
    * Hash spraying
 
 **Installed size:** `12.00 MB`  
 **How to install:** `sudo apt install redsnarf`  
 
 {{< spoiler "Dependencies:" >}}
 * creddump7
 * passing-the-hash
 * python3-docopt
 * python3-impacket
 * python3-ipy
 * python3-ldap
 * python3-libnmap
 * python3-netaddr
 * python3-pycryptodome
 * python3-pyuserinput
 * python3-smb
 * python3-termcolor
 * python3-wget
 {{< /spoiler >}}
 
 ##### redsnarf
 
 
 ```
 root@kali:~# redsnarf -h
 
     ______           .____________                     _____
 \______   \ ____   __| _/   _____/ ____ _____ ________/ ____\
  |       _// __ \ / __ |\_____  \ /    \__  \_  __ \   __\
  |    |   \  ___// /_/ |/        \   |  \/ __ \|  | \/|  |
  |____|_  /\___  >____ /_______  /___|  (____  /__|   |__|
         \/     \/     \/       \/     \/     \/
                                   redsnarf.ff0000@gmail.com
                                                   @redsnarf
 
 
 E D Williams - NCCGroup
 usage: ./redsnarf -H ip=192.168.0.1 -u administrator -p Password1 [-h] [-H HOST] [-u USERNAME] [-p PASSWORD] [-d DOMAIN_NAME] [-cC CREDPATH]
                                                                   [-cM MERGEPF] [-cO OUTPUTPATH] [-cQ QUICK_VALIDATE] [-cS SKIPLSACACHE]
                                                                   [-uA AUTO_COMPLETE] [-uC CLEAR_EVENT] [-uCP CUSTOM_POWERSHELL] [-uCIDR CIDR]
                                                                   [-uD DROPSHELL] [-uE EMPIRE_LAUNCHER] [-uFT FILE_TRANSCRIBE] [-uG C_PASSWORD]
                                                                   [-uMC MCAFEE_SITES] [-uJ JOHN_TO_PIPAL] [-uJW SENDTOJOHN] [-uJS SENDSPNTOJOHN]
                                                                   [-uL LOCKDESKTOP] [-uLP LIVEIPS] [-uM MSSQLSHELL] [-uMT METERPRETER_REVHTTPS]
                                                                   [-uO DELEGATED_PRIVS] [-uP POLICIESSCRIPTS_DUMP] [-uR MULTI_RDP] [-uRP RDP_CONNECT]
                                                                   [-uRS SNARF_SHELL] [-uS GET_SPN] [-uSS SPLIT_SPN] [-uSCF SCF_CREATOR]
                                                                   [-uSG SESSION_GOPHER] [-uU UNATTEND] [-uX XCOMMAND] [-uXS XSCRIPT]
                                                                   [-uW WIFI_CREDENTIALS] [-uWU WINDOWS_UPDATES] [-hI DRSUAPI] [-hN NTDS_UTIL]
                                                                   [-hQ QLDAP] [-hS CREDSFILE] [-hP PASS_ON_BLANK] [-hK MIMIKITTENZ] [-hL LSASS_DUMP]
                                                                   [-hM MASSMIMI_DUMP] [-hR STEALTH_MIMI] [-hT GOLDEN_TICKET] [-hW WIN_SCP]
                                                                   [-eA SERVICE_ACCOUNTS] [-eD USER_DESC] [-eL FIND_USER] [-eO OFIND_USER]
                                                                   [-eP PASSWORD_POLICY] [--protocols [PROTOCOLS ...]] [-eR RECORDDESKTOP]
                                                                   [-eS SCREENSHOT] [-eT SYSTEM_TASKLIST] [-rA EDQ_AUTOLOGON] [-rB EDQ_BACKDOOR]
                                                                   [-rC EDQ_SCFORCEOPTION] [-rF FAT] [-rL LAT] [-rM EDQ_SINGLESESSIONPERUSER]
                                                                   [-rN EDQ_NLA] [-rR EDQ_RDP] [-rS EDQ_ALLOWTGTSESSIONKEY] [-rT EDQ_TRDP]
                                                                   [-rU EDQ_UAC] [-rW EDQ_WDIGEST]
 
 RedSnarf Version 0.5p: Offers a rich set of features to help Pentest Servers and Workstations
 
 options:
   -h, --help        show this help message and exit
   -H HOST, --host HOST
                     Specify a hostname -H ip= / range -H range= / targets file -H file= to grab hashes from
   -u USERNAME, --username USERNAME
                     Enter a username
   -p PASSWORD, --password PASSWORD
                     Enter a password or hash
   -d DOMAIN_NAME, --domain_name DOMAIN_NAME
                     <Optional> Enter domain name
 
 Configurational:
   -cC CREDPATH, --credpath CREDPATH
                     <Optional> Enter path to creddump7 default /usr/share/creddump7/
   -cM MERGEPF, --mergepf MERGEPF
                     <Optional> Enter output path and filename to merge multiple pwdump files default /tmp/merged.txt
   -cO OUTPUTPATH, --outputpath OUTPUTPATH
                     <Optional> Enter output path default /tmp/
   -cQ QUICK_VALIDATE, --quick_validate QUICK_VALIDATE
                     <Optional> Quickly Validate Credentials
   -cS SKIPLSACACHE, --skiplsacache SKIPLSACACHE
                     <Optional> Enter y to skip dumping lsa and cache and go straight to hashes!!
 
 Utilities:
   -uA AUTO_COMPLETE, --auto_complete AUTO_COMPLETE
                     <Optional> Copy autocomplete file to /etc/bash_completion.d
   -uC CLEAR_EVENT, --clear_event CLEAR_EVENT
                     <Optional> Clear event log - application, security, setup or system
   -uCP CUSTOM_POWERSHELL, --custom_powershell CUSTOM_POWERSHELL
                     <Optional> Run Custom Powershell Scripts found in the RedSnarf folder
   -uCIDR CIDR, --cidr CIDR
                     <Optional> Convert CIDR representation to ip, hostmask, broadcast
   -uD DROPSHELL, --dropshell DROPSHELL
                     <Optional> Enter y to Open up a shell on the remote machine
   -uE EMPIRE_LAUNCHER, --empire_launcher EMPIRE_LAUNCHER
                     <Optional> Start Empire Launcher
   -uFT FILE_TRANSCRIBE, --file_transcribe FILE_TRANSCRIBE
                     <Optional> Converts a file to base64 then sends via SendKeys
   -uG C_PASSWORD, --c_password C_PASSWORD
                     <Optional> Decrypt GPP Cpassword
   -uMC MCAFEE_SITES, --mcafee_sites MCAFEE_SITES
                     <Optional> Decrypt Mcafee Sites Password
   -uJ JOHN_TO_PIPAL, --john_to_pipal JOHN_TO_PIPAL
                     <Optional> Send passwords cracked with JtR to Pipal for Auditing
   -uJW SENDTOJOHN, --sendtojohn SENDTOJOHN
                     <Optional> Enter path to NT Hash file to send to JtR
   -uJS SENDSPNTOJOHN, --sendspntojohn SENDSPNTOJOHN
                     <Optional> Enter path of SPN Hash file to send to JtR Jumbo
   -uL LOCKDESKTOP, --lockdesktop LOCKDESKTOP
                     <Optional> Lock remote users Desktop
   -uLP LIVEIPS, --liveips LIVEIPS
                     <Optional> Ping scan to generate a list of live IP's
   -uM MSSQLSHELL, --mssqlshell MSSQLSHELL
                     <Optional> Start MSSQL Shell use WIN for Windows Auth, DB for MSSQL Auth
   -uMT METERPRETER_REVHTTPS, --meterpreter_revhttps METERPRETER_REVHTTPS
                     <Optional> Launch Reverse Meterpreter HTTPS
   -uO DELEGATED_PRIVS, --delegated_privs DELEGATED_PRIVS
                     <Optional> Delegated Privilege Checker
   -uP POLICIESSCRIPTS_DUMP, --policiesscripts_dump POLICIESSCRIPTS_DUMP
                     <Optional> Enter y to Dump Policies and Scripts folder from a Domain Controller
   -uR MULTI_RDP, --multi_rdp MULTI_RDP
                     <Optional> Enable Multi-RDP with Mimikatz
   -uRP RDP_CONNECT, --rdp_connect RDP_CONNECT
                     <Optional> Connect to existing RDP sessions without password
   -uRS SNARF_SHELL, --snarf_shell SNARF_SHELL
                     <Optional> Start Reverse Listening Snarf Shell
   -uS GET_SPN, --get_spn GET_SPN
                     <Optional> Get SPN's from DC
   -uSS SPLIT_SPN, --split_spn SPLIT_SPN
                     <Optional> Split SPN File
   -uSCF SCF_CREATOR, --scf_creator SCF_CREATOR
                     <Optional> Create an SCF file for some SMB hash capturing fun
   -uSG SESSION_GOPHER, --session_gopher SESSION_GOPHER
                     <Optional> Run Session Gopher on Remote Machine
   -uU UNATTEND, --unattend UNATTEND
                     <Optional> Enter y to look for and grep unattended installation files
   -uX XCOMMAND, --xcommand XCOMMAND
                     <Optional> Run custom command
   -uXS XSCRIPT, --xscript XSCRIPT
                     <Optional> Run custom script
   -uW WIFI_CREDENTIALS, --wifi_credentials WIFI_CREDENTIALS
                     <Optional> Grab Wifi Credentials
   -uWU WINDOWS_UPDATES, --windows_updates WINDOWS_UPDATES
                     <Optional> Get Windows Update Status
 
 Hash related:
   -hI DRSUAPI, --drsuapi DRSUAPI
                     <Optional> Extract NTDS.dit hashes using drsuapi method - accepts machine name as username
   -hN NTDS_UTIL, --ntds_util NTDS_UTIL
                     <Optional> Extract NTDS.dit using NTDSUtil
   -hQ QLDAP, --qldap QLDAP
                     <Optional> In conjunction with the -i and -n option - Query LDAP for Account Status when dumping Domain Hashes
   -hS CREDSFILE, --credsfile CREDSFILE
                     Spray multiple hashes at a target range
   -hP PASS_ON_BLANK, --pass_on_blank PASS_ON_BLANK
                     Password to use when only username found in Creds File
   -hK MIMIKITTENZ, --mimikittenz MIMIKITTENZ
                     <Optional> Run Mimikittenz
   -hL LSASS_DUMP, --lsass_dump LSASS_DUMP
                     <Optional> Dump lsass for offline use with mimikatz
   -hM MASSMIMI_DUMP, --massmimi_dump MASSMIMI_DUMP
                     <Optional> Mimikatz Dump Credentaisl from the remote machine(s)
   -hR STEALTH_MIMI, --stealth_mimi STEALTH_MIMI
                     <Optional> stealth version of mass-mimikatz
   -hT GOLDEN_TICKET, --golden_ticket GOLDEN_TICKET
                     <Optional> Create a Golden Ticket
   -hW WIN_SCP, --win_scp WIN_SCP
                     <Optional> Check for, and decrypt WinSCP hashes
 
 Enumeration related:
   -eA SERVICE_ACCOUNTS, --service_accounts SERVICE_ACCOUNTS
                     <Optional> Enum service accounts, if any
   -eD USER_DESC, --user_desc USER_DESC
                     <Optional> Save AD User Description Field to file, check for password
   -eL FIND_USER, --find_user FIND_USER
                     <Optional> Find user - Live
   -eO OFIND_USER, --ofind_user OFIND_USER
                     <Optional> Find user - Offline
   -eP PASSWORD_POLICY, --password_policy PASSWORD_POLICY
                     <Optional> Display Password Policy
   --protocols [PROTOCOLS ...]
                     ['139/SMB', '445/SMB']
   -eR RECORDDESKTOP, --recorddesktop RECORDDESKTOP
                     <Optional> Record a desktop using Windows Problem Steps Recorder
   -eS SCREENSHOT, --screenshot SCREENSHOT
                     <Optional> Take a screenshot of remote machine desktop
   -eT SYSTEM_TASKLIST, --system_tasklist SYSTEM_TASKLIST
                     <Optional> Display NT AUTHORITY\SYSTEM Tasklist
 
 Registry related:
   -rA EDQ_AUTOLOGON, --edq_autologon EDQ_AUTOLOGON
                     <Optional> (e)nable/(d)isable/(q)uery AutoLogon Registry Setting
   -rB EDQ_BACKDOOR, --edq_backdoor EDQ_BACKDOOR
                     <Optional> (e)nable/(d)isable/(q)uery Backdoor Registry Setting
   -rC EDQ_SCFORCEOPTION, --edq_scforceoption EDQ_SCFORCEOPTION
                     <Optional> (e)nable/(d)isable/(q)uery Smart Card scforceoption Registry Setting
   -rF FAT, --fat FAT
                     <Optional> Write batch file for turning on/off FilterAdministratorToken Policy
   -rL LAT, --lat LAT
                     <Optional> Write batch file for turning on/off Local Account Token Filter Policy
   -rM EDQ_SINGLESESSIONPERUSER, --edq_SingleSessionPerUser EDQ_SINGLESESSIONPERUSER
                     <Optional> (E)nable/(D)isable/(Q)uery RDP SingleSessionPerUser Registry Setting
   -rN EDQ_NLA, --edq_nla EDQ_NLA
                     <Optional> (e)nable/(d)isable/(q)uery NLA Status
   -rR EDQ_RDP, --edq_rdp EDQ_RDP
                     <Optional> (e)nable/(d)isable/(q)uery RDP Status
   -rS EDQ_ALLOWTGTSESSIONKEY, --edq_allowtgtsessionkey EDQ_ALLOWTGTSESSIONKEY
                     <Optional> (E)nable/(D)isable/(Q)uery allowtgtsessionkey Registry Setting
   -rT EDQ_TRDP, --edq_trdp EDQ_TRDP
                     <Optional> (e)nable/(d)isable/(q)uery Tunnel RDP out of port 443
   -rU EDQ_UAC, --edq_uac EDQ_UAC
                     <Optional> (e)nable/(d)isable/(q)uery UAC Registry Setting
   -rW EDQ_WDIGEST, --edq_wdigest EDQ_WDIGEST
                     <Optional> (e)nable/(d)isable/(q)uery Wdigest UseLogonCredential Registry Setting
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
