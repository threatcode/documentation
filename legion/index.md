---
Title: legion
Homepage: https://govanguard.com/legion/
Repository: https://gitlab.com/kalilinux/packages/legion
Architectures: any
Version: 0.4.3-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-vulnerability 
Icon: images/legion-logo.svg
PackagesInfo: |
 ### legion
 
  This package contains an open source, easy-to-use, super-extensible and
  semi-automated network penetration testing tool that aids in discovery,
  reconnaissance and exploitation of information systems.
   
  Legion is a fork of SECFORCE's Sparta.
 
 **Installed size:** `3.23 MB`  
 **How to install:** `sudo apt install legion`  
 
 {{< spoiler "Dependencies:" >}}
 * dirbuster
 * dnsmap
 * enum4linux
 * eyewitness | cutycapt
 * finger
 * graphicsmagick-imagemagick-compat
 * hping3
 * hydra
 * impacket-scripts
 * ldap-utils
 * mariadb-client-core
 * medusa
 * metasploit-framework
 * nbtscan
 * netcat-traditional
 * nfs-common
 * nikto
 * nmap
 * perl
 * polenum
 * postgresql-client
 * python3
 * python3-colorama
 * python3-pandas
 * python3-pyexploitdb
 * python3-pyfiglet
 * python3-pyqt6
 * python3-pyshodan
 * python3-qasync
 * python3-requests
 * python3-rich
 * python3-serial-asyncio
 * python3-service-identity
 * python3-six
 * python3-sqlalchemy
 * python3-termcolor
 * python3-urllib3
 * rdesktop
 * rpcbind
 * rsh-client
 * ruby
 * rwho
 * smbclient
 * smtp-user-enum
 * snmp
 * sparta-scripts
 * sqlmap
 * sslscan
 * sslyze
 * telnet
 * theharvester
 * unicornscan
 * urlscan
 * vncviewer
 * wafw00f
 * wapiti
 * whatweb
 * wordlists
 * wpscan
 * x11-apps
 * xserver-xephyr
 * xsltproc
 * xvfb
 {{< /spoiler >}}
 
 ##### legion
 
 
 ```
 root@kali:~# legion -h
 [09:46:56] INFO     Non-WSL The AppData Temp directory path is   auxiliary.py:84
                     /root/.local/share/legion/tmp                               
            INFO     Using Qt Implementation: PyQt6                __init__.py:83
            INFO     NumExpr defaulting to 8 threads.                utils.py:160
                                                                                                                                                                                     
     Xt:.                                                                                                                                                                            
    ;@t                                                                                                                                                                              
    8 S:                                                                                                                                                                             
    S X@.                            :%8888XXXXSS8@X%:.                                                                                                                              
    :X@%                         .%88XX888@888@@8888@@@8%:.                                                                                                                          
    .8 @:                       ;88@@88XSX%SX%XSXX%tSX888:.                                                                                                                          
   .:8:Xt.                    :X8@X88XX8S%XS%%%%%X%%%@XSt.                                                                                                                           
   t.@@:8                   .88X8@SSXXS%S%t%%%SS%tS%XS%;..                                                                                                                           
  .8.88:8                   8@S@XXX%%%S%tS%%%%Xt%%%XX;..                                                                                                                             
   X.888;;                 X@XXXSSSS%%tS%t%%S%t%%SX%;:.                                                                                                                              
  .8t8S8@8;.              ;8X@XXX%XtSt%tS%%%%S%SS@t:..                                                                                                                               
  .@%8X 8t.               888XSX%@%%%S%%%S%SS%%%@;:..                                                                                                                                
  :8S88;XSt.             .8@@X@SS%S%%%S%S@SX%X@Xt:.                                                                                                                                  
  .X@;S% 88              ;88@@SX%S%S%@X%%ttt%%%;:.                                                                                                                                   
  ;@8StS.@:.             %88X8X%S@S@St%S;%Xt%8t;..                                                                                                                                   
   ;X@@8@:.             .S888SS@S%%%SSS@S%88X8t:. .tt..                                                                                                                              
   .t@8@..              .%888XX%X%%X88  t88888@8@8%88.                                                                                                                               
    :%@8:               .;88@SX%%%X t888%tStt%SS8X %@%:                                                                                                                              
    .;X8.                :88X@%XSX8t88%%t%XtXtt@;@ .SX                                                                                                                               
    .;X%;.               .@888@%8@t;8S@S@;%@%@Stt@@@;8                                                                                                                               
    :t%8X.                t8@@S@@8SXX;t%t%X;tt%t%t8tS%                                                                                                                               
   .%St%t.               .;888@888S88tS;t%;%%%tXSXSXt8.                                                  ... ...                            ..                                       
   .%tSt%:.               :@8@X8S@:X8@%St%%%%%%;%S@:@ t. .%@%X;t;8S8t:.    ;8%;@tt;8 .tXX t8.     t%S:; t888X;:@:S. ;8X ;t;S;@@:.    tS . %88X::@tS:.    @X.%t;t@8.      .X@%8tSS8t. 
   .;StX::                 t@8888t..8S;tSt%%%Xt%t%S@%@:. ..  @.  @: ..     .   .  .S;    X8X:   8tS;S 8: .    ;%@@;..  88  @8. .  .8;S; S;    :88X.tS:    ..8S   S @:       .. S ... 
   .:tS%:.                .t@88Xt.  ;%S;tStX;;%X;X;X@t:.    .t   .%.          .8. ;@.    .S ;. 88  :S:.       .@%8.    8%  SS.    X@ .8%      . :S@.:8t    .tX %.  ;S.      :@ @.    
    :t%X;.                .:8888t  .;S;t%ttt%Xtt%%X8St:.    .S.. 8t.          .8. %8      :t. X8  t8;.         .;:.   .X8  :S.   @8: tX.          8S ;:S.   :%.: S  88.     :X:@     
    .%SS;.                 :88XS. ...%X%tSXt%%StX;88t;.     .8%  .t.          .8  ;8    @:@: :   S8                    8S .SS.  @8. @8;           t.   8    ;8;X:t8S:;:8    :8.@     
    .;tX:.                  88;.    .t@tS%%X%St%%%88t:.     .@%  %t           :S  :@@8@S.t8: 88  88:                  .@8  :%  .S;  SS:           .8  .8;   :@:X.. X8  %S.  :X:@     
    .;;;:.                 .;S8888SXS8XSXStt%St @tX@S.       @%  %t           ::  :@@888%X8  8   S@;                   @S  SX.  S;  tS.           :8.  8;   :8:@   .@ ;.t%@::8.X.    
     ;tt.                .X8X888@X888888StS@X8:8   :@;.     .St  %t           :8: t8.  .@%t..%S  ;S;.    .8SSX%tt8t@: .@8  .S   8S. @8;           ;X  ;X:   :@:X   .: @ : ;8S@ @     
    .tt;:.              t8888888888@888888%@8tX@S8 8;t.     .t;  %t           .   t@   .::.  ;8. .@8:        %;t %;.   8S  %t  .:.   t;.          8X  :8    ;8;X       :8:. 8t.@     
    .tt%.             .888@@@XS%S@88888@88@88t8:t%88X8.     ..   tt      :  ;.;X  :8      8S..X:.  8X       .SSt :%.  .8@  .X   :8 ..%8          %   S8.    :S:X       .;88  .;8.    
    .;t:..           tX888%%tttS%%t;@%S8@88:88.SS:Xt8@      ;@.  8;      % :;.t.  :S:    X8t:..;8:;:t%;8;:  ;  ;.%t    X%. @8:  .::8;SS%@:.   .88S.S t:     ;S 8          t ; .S.    
     ;;t.           :X@8@SXS;%%%%St;%88888S;888SX:S@.X:    .X%   X.8:tS:8@:X..88   ;@ tXSX  %.   :8.S   @:;.8;8;tS.  ..X.  X8:       8%X:88:; ;%t.;:.:     :8@.8t:        :;S@;8     
     :t:.           S888t8ttt%t%St%%St8@X8.X 888@@;tSS@  .S@St.     ..:.  .t@8St.     .;;; S.       X@::    X@;: .  ;8@%.  ;X8@;.    ::t@;    :XX:       :8@Xt..%8@.      .. 8X8.    
     :;;.          S@X8@@;t%%%%St%X;;%tXX8%t 8@%;8S8;8X8:     ::::::.  .:....   :::::.   .              ...   .    ...  ...  . .      ..    ...              .               ..      
     :;:.         @88S Xtt%%%XtStttt%t%S%S8X8X8t.;%SS@88%.      ...               ...                                                                                                
     .;:.        .X8t@@%Xtt%%tt;ttt%%%%tSXt@8:t;@;888;@;8:                                                                                                                           
     .;;..       8S%@88@%%SS@;%t%%%%%%%%%tt%%888.:S8X:%88:.                                                                                                                          
     .;;:.      8t8.8SStX%@%tSt%%%%t%X;%%%%%%S8888888%88S:.                                                                                                                          
     :t;.      ::88@%%%t%X%SX%S;%ttXt;t%SS%Xt8X888.S@@@t%...                                                                                                                         
     .;;..   .XXSt8t%S;XtXS@%%%%X%%t;t%Sttt%Xt88; 8%X@8%%S%%t%;::.                                                                                                                   
     .t;.. ;::8:8@8Xtt%XSX@@X8XSX%t%t%t;t%%%t%tX@tSX8tSS%8S%@tX%St;;.                                                                                                                
     .;;: :8@8@S8888tSSX8888@SS8%%%%%tt%%Xt%@tXt88S@:@8@StXtXSXt%XtSt;.                                                                                                              
     .;t.; @8X%t8888X@88888@88888t%St%%tttXt%@tX@%:t8@SSSStS%X%@t8%tSX;:.                                                                                                            
     .;;@.;88t@@X8@t888888888@XS@SXttttt%%tS@%XSS X%8 @@tSXS%StSSttXSSX%t;.                                                                                                          
     .;; @8@SXS88@S8X8888888@X8@88SX%%%%%%tt@8%S@S @8:@%Xt%SStSS%X%XtXtSX;:.                                                                                                         
     .;%@%8@t%X8@@8888888@88@XSS888X%t%%%St%@S@SX8S8888@XX@tSX%@tt%%S%Xt%St:.                                                                                                        
     .;%;88S%8@@8@X88888888XX8@X88X%Stt%t%%%X8X 8;: ::8SX@@8888%X%X%%%S%%%Xt;:                                                                                                       
     .;SX88tX@8S8X88@@88@@X@88S8888S%%S;%%St%t8%@X88@8@%XXSttX8@tX%XSStSXt%Xt:.                                                                                                      
     .;t8%%X88@8@X@888XXX@8X8X88%@X%XtttS;tX%@8@t%8@SS@8SXX%@%tt@8SStSXtSX%Xtt;.                                                                                                     
     .t%S@@88@;XX8X8XXX88888X88%XSSSX%t%t%%tSX@@X8t88 8SXt%S%X%%%t%S%%SXtt88SS;.                                                                                                     
     .;t8888@;.XSS88@8@S8@@S8888XXX%Stt%X%XXS8@8X8888:8Xt%SX%%S%%Xt%S%StX%%%StS:.                                                                                                    
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
