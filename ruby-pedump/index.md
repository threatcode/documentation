---
Title: ruby-pedump
Homepage: http://github.com/zed-0xff/pedump
Repository: https://gitlab.com/kalilinux/packages/ruby-pedump
Architectures: all
Version: 0.6.5-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ruby-pedump
 
  This package contains a script to dump headers, sections, extract resources of
  win32 PE exe,dll,etc
 
 **Installed size:** `2.41 MB`  
 **How to install:** `sudo apt install ruby-pedump`  
 
 {{< spoiler "Dependencies:" >}}
 * ruby
 * ruby-awesome-print
 * ruby-iostruct 
 * ruby-multipart-post 
 * ruby-rainbow
 * ruby-zhexdump 
 {{< /spoiler >}}
 
 ##### pedump-ruby
 
 
 ```
 root@kali:~# pedump-ruby -h
 Usage: pedump [options]
         --version                    Print version information and exit
     -v, --verbose                    Run verbosely
                                      (can be used multiple times)
     -q, --quiet                      Silent any warnings
                                      (can be used multiple times)
     -F, --force                      Try to dump by all means
                                      (can cause exceptions & heavy wounds)
     -f, --format FORMAT              Output format: bin,c,dump,hex,inspect,json,table,yaml
                                      (default: table)
         --mz
         --dos-stub
         --rich
         --pe
         --ne
         --te
         --data-directory
     -S, --sections
         --tls
         --security
     -s, --strings
     -R, --resources
         --resource-directory
     -I, --imports
     -E, --exports
     -V, --version-info
         --packer
         --deep                       packer deep scan, significantly slower
     -P, --packer-only                packer/compiler detect only,
                                      mimics 'file' command output
     -r, --recursive                  recurse dirs in packer detect
         --all                        Dump all but resource-directory (default)
 
         --extract ID                 Extract a resource/section/data_dir
                                      ID: datadir:EXPORT     - datadir by type
                                      ID: resource:0x98478   - resource by offset
                                      ID: resource:ICON/#1   - resource by type & name
                                      ID: section:.text      - section by name
                                      ID: section:rva/0x1000 - section by RVA
                                      ID: section:raw/0x400  - section by RAW_PTR
         --va2file VA                 Convert RVA to file offset
 
     -W, --web                        Uploads files to a https://pedump.me
                                      for a nice HTML tables with image previews,
                                      candies & stuff
     -C, --console                    opens IRB console with specified file loaded
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
