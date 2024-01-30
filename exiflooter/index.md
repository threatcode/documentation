---
Title: exiflooter
Homepage: https://github.com/aydinnyunus/exiflooter
Repository: https://gitlab.com/kalilinux/packages/exiflooter
Architectures: any
Version: 0.0~git20220916.a92e697-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### exiflooter
 
  ExifLooter finds geolocation on all image urls and directories also integrates
  with OpenStreetMap.
 
 **Installed size:** `6.61 MB`  
 **How to install:** `sudo apt install exiflooter`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libimage-exiftool-perl
 {{< /spoiler >}}
 
 ##### exiflooter
 
 
 ```
 root@kali:~# exiflooter -h
 ExifLooter finds GeoLocation Metadata and display. You can use with pipe and flags
 
 Usage:
   exifLooter [flags]
 
 Flags:
   -d, --directory string   Specify a directory for Analyzing
   -h, --help               help for exifLooter
   -i, --image string       Specify a image for Analyzing
   -m, --open-street-map    Get Open Street Map Link
   -p, --pipe               Pipe with other scripts
   -r, --remove             Remove metadata from Image
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
