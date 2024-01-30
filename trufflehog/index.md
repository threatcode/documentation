---
Title: trufflehog
Homepage: https://github.com/trufflesecurity/truffleHog
Repository: https://gitlab.com/kalilinux/packages/trufflehog
Architectures: any
Version: 3.57.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### trufflehog
 
  This package contains a utitlity to search through git repositories for
  secrets, digging deep into commit history and branches. This is effective at
  finding secrets accidentally committed.
 
 **Installed size:** `154.62 MB`  
 **How to install:** `sudo apt install trufflehog`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libsqlite3-0 
 {{< /spoiler >}}
 
 ##### snifftest
 
 
 ```
 root@kali:~# snifftest --help
 usage: Snifftest [<flags>] <command> [<args> ...]
 
 Test secret detectors against data sets.
 
 Flags:
   --help  Show context-sensitive help (also try --help-long and --help-man).
 
 Commands:
 help [<command>...]
     Show help.
 
 show-detectors
     Shows the available detectors.
 
 scan --repo=REPO [<flags>]
     Scans data.
 
 
 ```
 
 - - -
 
 ##### trufflehog
 
 
 ```
 root@kali:~# trufflehog --help
 usage: TruffleHog [<flags>] <command> [<args> ...]
 
 TruffleHog is a tool for finding credentials.
 
 Flags:
       --help                     Show context-sensitive help (also try
                                  --help-long and --help-man).
       --debug                    Run in debug mode.
       --trace                    Run in trace mode.
       --profile                  Enables profiling and sets a pprof and fgprof
                                  server on :18066.
   -j, --json                     Output in JSON format.
       --json-legacy              Use the pre-v3.0 JSON format. Only works with
                                  git, gitlab, and github sources.
       --github-actions           Output in GitHub Actions format.
       --concurrency=8            Number of concurrent workers.
       --no-verification          Don't verify the results.
       --only-verified            Only output verified results.
       --filter-unverified        Only output first unverified result per
                                  chunk per detector if there are more than one
                                  results.
       --config=CONFIG            Path to configuration file.
       --print-avg-detector-time  Print the average time spent on each detector.
       --no-update                Don't check for updates.
       --fail                     Exit with code 183 if results are found.
       --verifier=VERIFIER ...    Set custom verification endpoints.
       --archive-max-size=ARCHIVE-MAX-SIZE  
                                  Maximum size of archive to scan. (Byte units
                                  eg. 512B, 2KB, 4MB)
       --archive-max-depth=ARCHIVE-MAX-DEPTH  
                                  Maximum depth of archive to scan.
       --archive-timeout=ARCHIVE-TIMEOUT  
                                  Maximum time to spend extracting an archive.
       --include-detectors="all"  Comma separated list of detector types to
                                  include. Protobuf name or IDs may be used,
                                  as well as ranges.
       --exclude-detectors=EXCLUDE-DETECTORS  
                                  Comma separated list of detector types to
                                  exclude. Protobuf name or IDs may be used,
                                  as well as ranges. IDs defined here take
                                  precedence over the include list.
       --version                  Show application version.
 
 Commands:
 help [<command>...]
     Show help.
 
 git [<flags>] <uri>
     Find credentials in git repositories.
 
 github [<flags>]
     Find credentials in GitHub repositories.
 
 gitlab --token=TOKEN [<flags>]
     Find credentials in GitLab repositories.
 
 filesystem [<flags>] [<path>...]
     Find credentials in a filesystem.
 
 s3 [<flags>]
     Find credentials in S3 buckets.
 
 gcs [<flags>]
     Find credentials in GCS buckets.
 
 syslog [<flags>]
     Scan syslog
 
 circleci --token=TOKEN
     Scan CircleCI
 
 docker --image=IMAGE
     Scan Docker Image
 
 
 ```
 
 - - -
 
 ##### trufflehog-generate
 
 
 ```
 root@kali:~# trufflehog-generate --help
 usage: generate [<flags>] <kind> <name>
 
 Generate is used to write new features.
 
 Flags:
   --help  Show context-sensitive help (also try --help-long and --help-man).
 
 Args:
   <kind>  Kind of thing to generate.
   <name>  Name of the Source/Detector to generate.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
