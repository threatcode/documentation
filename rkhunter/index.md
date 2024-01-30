---
Title: rkhunter
Homepage: https://rkhunter.sourceforge.net
Repository: https://salsa.debian.org/pkg-security-team/rkhunter
Architectures: all
Version: 1.4.6-11
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: images/rkhunter-logo.svg
PackagesInfo: |
 ### rkhunter
 
  Rootkit Hunter scans systems for known and unknown rootkits,
  backdoors, sniffers and exploits.
   
  It checks for:
   - SHA256 hash changes;
   - files commonly created by rootkits;
   - executables with anomalous file permissions;
   - suspicious strings in kernel modules;
   - hidden files in system directories;
  and can optionally scan within files.
   
  Using rkhunter alone does not guarantee that a system is not
  compromised. Running additional tests, such as chkrootkit, is
  recommended.
 
 **Installed size:** `1.04 MB`  
 **How to install:** `sudo apt install rkhunter`  
 
 {{< spoiler "Dependencies:" >}}
 * binutils
 * debconf  | debconf-2.0
 * debconf | debconf-2.0
 * file
 * lsof
 * net-tools
 * perl
 * ucf 
 {{< /spoiler >}}
 
 ##### rkhunter
 
 RootKit Hunter
 
 ```
 root@kali:~# rkhunter -h
 
 Usage: rkhunter {--check | --unlock | --update | --versioncheck |
                  --propupd [{filename | directory | package name},...] |
                  --list [{tests | {lang | languages} | rootkits | perl | propfiles}] |
                  --config-check | --version | --help} [options]
 
 Current options are:
          --append-log                  Append to the logfile, do not overwrite
          --bindir <directory>...       Use the specified command directories
      -c, --check                       Check the local system
      -C, --config-check                Check the configuration file(s), then exit
   --cs2, --color-set2                  Use the second color set for output
          --configfile <file>           Use the specified configuration file
          --cronjob                     Run as a cron job
                                        (implies -c, --sk and --nocolors options)
          --dbdir <directory>           Use the specified database directory
          --debug                       Debug mode
                                        (Do not use unless asked to do so)
          --disable <test>[,<test>...]  Disable specific tests
                                        (Default is to disable no tests)
          --display-logfile             Display the logfile at the end
          --enable  <test>[,<test>...]  Enable specific tests
                                        (Default is to enable all tests)
          --hash {MD5 | SHA1 | SHA224 | SHA256 | SHA384 | SHA512 |
                  NONE | <command>}     Use the specified file hash function
                                        (Default is SHA256)
      -h, --help                        Display this help menu, then exit
  --lang, --language <language>         Specify the language to use
                                        (Default is English)
          --list [tests | languages |   List the available test names, languages,
                  rootkits | perl |     rootkit names, perl module status
                  propfiles]            or file properties database, then exit
      -l, --logfile [file]              Write to a logfile
                                        (Default is /var/log/rkhunter.log)
          --noappend-log                Do not append to the logfile, overwrite it
          --nocf                        Do not use the configuration file entries
                                        for disabled tests (only valid with --disable)
          --nocolors                    Use black and white output
          --nolog                       Do not write to a logfile
 --nomow, --no-mail-on-warning          Do not send a message if warnings occur
    --ns, --nosummary                   Do not show the summary of check results
  --novl, --no-verbose-logging          No verbose logging
          --pkgmgr {RPM | DPKG | BSD |  Use the specified package manager to obtain
                    BSDng | SOLARIS |   or verify file property values.
                    NONE}               (Default is NONE)
          --propupd [file | directory | Update the entire file properties database,
                     package]...        or just for the specified entries
      -q, --quiet                       Quiet mode (no output at all)
   --rwo, --report-warnings-only        Show only warning messages
    --sk, --skip-keypress               Don't wait for a keypress after each test
          --summary                     Show the summary of system check results
                                        (This is the default)
          --syslog [facility.priority]  Log the check start and finish times to syslog
                                        (Default level is authpriv.notice)
          --tmpdir <directory>          Use the specified temporary directory
          --unlock                      Unlock (remove) the lock file
          --update                      Check for updates to database files
    --vl, --verbose-logging             Use verbose logging (on by default)
      -V, --version                     Display the version number, then exit
          --versioncheck                Check for latest version of program
      -x, --autox                       Automatically detect if X is in use
      -X, --no-autox                    Do not automatically detect if X is in use
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
