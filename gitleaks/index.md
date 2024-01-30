---
Title: gitleaks
Homepage: https://github.com/gitleaks/gitleaks
Repository: https://salsa.debian.org/go-team/packages/gitleaks
Architectures: any
Version: 8.16.0-1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gitleaks
 
  Gitleaks is a SAST tool for **detecting** and **preventing** hardcoded
  secrets like passwords, api keys, and tokens in git repos.  Gitleaks is
  an **easy-to-use, all-in-one solution** for detecting secrets, past or
  present, in your code.
 
 **Installed size:** `6.80 MB`  
 **How to install:** `sudo apt install gitleaks`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### gitleaks
 
 
 ```
 root@kali:~# gitleaks -h
 Gitleaks scans code, past or present, for secrets
 
 Usage:
   gitleaks [command]
 
 Available Commands:
   completion  Generate the autocompletion script for the specified shell
   detect      detect secrets in code
   help        Help about any command
   protect     protect secrets in code
   version     display gitleaks version
 
 Flags:
   -b, --baseline-path string       path to baseline with issues that can be ignored
   -c, --config string              config file path
                                    order of precedence:
                                    1. --config/-c
                                    2. env var GITLEAKS_CONFIG
                                    3. (--source/-s)/.gitleaks.toml
                                    If none of the three options are used, then gitleaks will use the default config
       --exit-code int              exit code when leaks have been encountered (default 1)
   -h, --help                       help for gitleaks
   -l, --log-level string           log level (trace, debug, info, warn, error, fatal) (default "info")
       --max-target-megabytes int   files larger than this will be skipped
       --no-banner                  suppress banner
       --redact                     redact secrets from logs and stdout
   -f, --report-format string       output format (json, csv, sarif) (default "json")
   -r, --report-path string         report file
   -s, --source string              path to source (default: $PWD) (default ".")
   -v, --verbose                    show verbose output from scan
 
 Use "gitleaks [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
