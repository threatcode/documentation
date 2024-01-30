---
Title: ophcrack
Homepage: http://ophcrack.sourceforge.net/
Repository: https://salsa.debian.org/pkg-security-team/ophcrack
Architectures: any
Version: 3.8.0-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-passwords 
Icon: images/ophcrack-logo.svg
PackagesInfo: |
 ### ophcrack
 
  Ophcrack is a Windows password cracker based on a time-memory trade-off
  using rainbow tables. This is a new variant of Hellman's original trade-off,
  with better performance. It recovers 99.9% of alphanumeric passwords in
  seconds.
   
  It works for Windows NT/2000/XP/Vista/7.
   
  This package contains ophcrack with QT4 based graphical UI.
  Please note that it can be used in command line as well.
 
 **Installed size:** `479 KB`  
 **How to install:** `sudo apt install ophcrack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libexpat1 
 * libgcc-s1 
 * libqt5charts5 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5widgets5 
 * libssl3 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### ophcrack
 
 A Microsoft Windows password cracker using rainbow tables.
 
 ```
 root@kali:~# ophcrack -h
 ophcrack 3.8.0 by Objectif Securite (http://www.objectif-securite.ch)
 
 Usage: ophcrack [OPTIONS]
 Cracks Windows passwords with Rainbow tables
 
   -a              disable audit mode (default)
   -A              enable audit mode
   -b              disable bruteforce
   -B              enable bruteforce (default)
   -c config_file  specify the config file to use
   -D              display (lots of!) debugging information
   -d dir          specify tables base directory
   -e              do not display empty passwords
   -f file         load hashes from the specified file (pwdump or session)
   -g              disable GUI
   -h              display this information
   -i              hide usernames
   -I              show usernames (default)
   -l file         log all output to the specified file
   -n num          specify the number of threads to use
   -o file         write cracking output to file in pwdump format
   -p num          preload (0 none, 1 index, 2 index+end, 3 all default)
   -q              quiet mode
   -r              launch the cracking when ophcrack starts (GUI only)
   -s              disable session auto-saving
   -S session_file specify the file to use to automatically save the progress of the search
   -u              display statistics when cracking ends
   -t table1[,a[,b,...]][:table2[,a[,b,...]]]
                   specify which table to use in the directory given by -d
   -v              verbose
   -w dir          load hashes from encrypted SAM file in directory dir
   -x file         export data in CSV format to file
 
 
 Example:	ophcrack -g -d /path/to/tables -t xp_free_fast,0,3:vista_free -f in.txt
 
 		Launch ophcrack in command line using tables 0 and 3 in
 		/path/to/tables/xp_free_fast and all tables in /path/to/tables/vista_free
 		and cracks hashes from pwdump file in.txt
 
 ```
 
 - - -
 
 ### ophcrack-cli
 
  Ophcrack is a Windows password cracker based on a time-memory trade-off
  using rainbow tables. This is a new variant of Hellman's original trade-off,
  with better performance. It recovers 99.9% of alphanumeric passwords in
  seconds.
   
  It works for Windows NT/2000/XP/Vista/7.
   
  This package contains ophcrack with command line interface only.
 
 **Installed size:** `182 KB`  
 **How to install:** `sudo apt install ophcrack-cli`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libexpat1 
 * libssl3 
 {{< /spoiler >}}
 
 ##### ophcrack-cli
 
 A Microsoft Windows password cracker using rainbow tables.
 
 ```
 root@kali:~# ophcrack-cli -h
 ophcrack 3.8.0 by Objectif Securite (http://www.objectif-securite.ch)
 
 Usage: ophcrack [OPTIONS]
 Cracks Windows passwords with Rainbow tables
 
   -a              disable audit mode (default)
   -A              enable audit mode
   -b              disable bruteforce
   -B              enable bruteforce (default)
   -c config_file  specify the config file to use
   -D              display (lots of!) debugging information
   -d dir          specify tables base directory
   -e              do not display empty passwords
   -f file         load hashes from the specified file (pwdump or session)
   -g              disable GUI
   -h              display this information
   -i              hide usernames
   -I              show usernames (default)
   -l file         log all output to the specified file
   -n num          specify the number of threads to use
   -o file         write cracking output to file in pwdump format
   -p num          preload (0 none, 1 index, 2 index+end, 3 all default)
   -q              quiet mode
   -r              launch the cracking when ophcrack starts (GUI only)
   -s              disable session auto-saving
   -S session_file specify the file to use to automatically save the progress of the search
   -u              display statistics when cracking ends
   -t table1[,a[,b,...]][:table2[,a[,b,...]]]
                   specify which table to use in the directory given by -d
   -v              verbose
   -w dir          load hashes from encrypted SAM file in directory dir
   -x file         export data in CSV format to file
 
 
 Example:	ophcrack -g -d /path/to/tables -t xp_free_fast,0,3:vista_free -f in.txt
 
 		Launch ophcrack in command line using tables 0 and 3 in
 		/path/to/tables/xp_free_fast and all tables in /path/to/tables/vista_free
 		and cracks hashes from pwdump file in.txt
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

![ophcrack](images/ophcrack.png)
