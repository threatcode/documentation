---
Title: s3scanner
Homepage: https://github.com/sa7mon/s3scanner
Repository: https://gitlab.com/kalilinux/packages/s3scanner
Architectures: any
Version: 3.0.0-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### s3scanner
 
  This package contains a tool to find open S3 buckets and dump their contents.
  The features are:
    * zap Multi-threaded scanning
    * telescope Supports tons of S3-compatible APIs
    * female_detective Scans all bucket permissions to find misconfigurations
    * floppy_disk Dump bucket contents to a local folder
    * whale Docker support
 
 **Installed size:** `17.85 MB`  
 **How to install:** `sudo apt install s3scanner`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### s3scanner
 
 
 ```
 root@kali:~# s3scanner -h
 INPUT: (1 required)
   -bucket        string  Name of bucket to check.
   -bucket-file   string  File of bucket names to check.
   -mq                    Connect to RabbitMQ to get buckets. Requires config file key "mq". Default: "false"
 
 OUTPUT:
   -db       Save results to a Postgres database. Requires config file key "db.uri". Default: "false"
   -json     Print logs to stdout in JSON format instead of human-readable. Default: "false"
 
 OPTIONS:
   -enumerate           Enumerate bucket objects (can be time-consuming). Default: "false"
   -provider    string  Object storage provider: aws, custom, digitalocean, dreamhost, gcp, linode - custom requires config file. Default: "aws"
   -threads     int     Number of threads to scan with. Default: "4"
 
 DEBUG:
   -verbose     Enable verbose logging. Default: "false"
   -version     Print version Default: "false"
 
 If config file is required these locations will be searched for config.yml: "." "/etc/s3scanner/" "$HOME/.s3scanner/"
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
