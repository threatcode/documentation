---
Title: dufflebag
Homepage: https://github.com/BishopFox/dufflebag
Repository: https://gitlab.com/kalilinux/packages/dufflebag
Architectures: all
Version: 0.0~git20200205.9a01942-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dufflebag
 
  Dufflebag is a tool that searches through public Elastic Block Storage (EBS)
  snapshots for secrets that may have been accidentally left in.
   
  The tool is organized as an Elastic Beanstalk ("EB", not to be confused
  with EBS) application, and definitely won't work if you try to run it
  on your own machine.
   
  Dufflebag has a lot of moving pieces because it's fairly nontrivial
  to actually read EBS volumes in practice. You have to be in an AWS
  environment, clone the snapshot, make a volume from the snapshot, attach
  the volume, mount the volume, etc... This is why it's made as an Elastic
  Beanstalk app, so it can automagically scale up or down however much you
  like, and so that the whole thing can be easily torn down when you're
  done with it.
 
 **Installed size:** `5.90 MB`  
 **How to install:** `sudo apt install dufflebag`  
 
 {{< spoiler "Dependencies:" >}}
 * golang-any
 * golang-github-aws-aws-sdk-go-dev
 * golang-github-deckarep-golang-set-dev
 * golang-lukechampine-blake3-dev 
 * make
 * sensible-utils
 * zip
 {{< /spoiler >}}
 
 ##### dufflebag
 
 
 ```
 root@kali:~# dufflebag -h
 Usage: dufflebag AWS_REGION
 Example: dufflebag us-east-1
 Dufflebag can only operate in one AWS region at a time
 If you want to search every region, you'll have to deploy several instances.
 See also /usr/share/doc/dufflebag/README.md
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
