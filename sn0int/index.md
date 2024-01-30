---
Title: sn0int
Homepage: https://github.com/kpcyrd/sn0int
Repository: https://gitlab.com/kalilinux/packages/sn0int
Architectures: any
Version: 0.26.0-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sn0int
 
  sn0int is a semi-automatic OSINT framework and package manager. It was built
  for IT security professionals and bug hunters to gather intelligence about a
  given target or about yourself. sn0int is enumerating attack surface by
  semi-automatically processing public information and mapping the results in
  a unified format for followup investigations.
 
 **Installed size:** `18.19 MB`  
 **How to install:** `sudo apt install sn0int`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libseccomp2 
 * libsodium23 
 * libsqlite3-0 
 * publicsuffix
 {{< /spoiler >}}
 
 ##### sn0int
 
 Semi-automatic OSINT framework and package manager
 
 ```
 root@kali:~# sn0int -h
 Usage: sn0int [OPTIONS] [COMMAND]
 
 Commands:
   run          Run a module directly
   sandbox      For internal use
   login        Login to the registry for publishing
   new          Create a new module
   publish      Publish a script to the registry
   install      Install a module from the registry
   search       Search in the registry
   pkg          The sn0int package manager
   add          Insert into the database
   select       Select from the database
   delete       Delete from the database
   activity     Query logged activity
   scope        Include entities in the scope
   noscope      Exclude entities from scope
   autoscope    Manage autoscope rules
   autonoscope  Manage autonoscope rules
   rescope      Rescope all entities based on autonoscope rules
   workspace    Manage workspaces
   cal          Calendar
   notify       Notify
   fsck         Verify blob storage for corrupt and dangling blobs
   export       Export a workspace for external processing
   stats        Show statistics about your current workspace
   repl         Run a lua repl
   paths        Show paths of various file system locations
   completions  Generate shell completions
   help         Print this message or the help of the given subcommand(s)
 
 Options:
   -w, --workspace <WORKSPACE>  Select a different workspace instead of the default [env: SN0INT_WORKSPACE=]
   -h, --help                   Print help
   -V, --version                Print version
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
