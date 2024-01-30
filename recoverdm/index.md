---
Title: recoverdm
Homepage: https://www.vanheusden.com/recoverdm
Repository: https://salsa.debian.org/pkg-security-team/recoverdm
Architectures: any
Version: 0.20-8
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-recover kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### recoverdm
 
  recoverdm recover disks with bad sectors. You can recover files as well
  complete devices. In case it finds sectors which simply cannot be recovered,
  it writes an empty sector to the output file and continues.
   
  When recovering a CD or a DVD and the program cannot read the sector in
  "normal mode", then the program will try to read the sector in "RAW mode"
  (without error-checking etc.). This toolkit also has a utility called
  'mergebad' which merges multiple images into one.
   
  This package is useful in forensics investigations.
 
 **Installed size:** `65 KB`  
 **How to install:** `sudo apt install recoverdm`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### mergebad
 
 Merge multiple images into one
 
 ```
 root@kali:~# mergebad -h
 -i <mapfile> <imagefile>
 		With -i one selects a mapfile+imagefile to read.
 -o <outputfile>
 		File to write output to.
 -l <mapfile>	In case all inputimages had a badblock on the same
 		place, this file will list those blocks.
 -s <size>	Limit or extend the size of the outputimage.
 -v		Be verbose.
 -h		This help.
 ```
 
 - - -
 
 ##### recoverdm
 
 Recover files on disks with damaged sectors
 
 ```
 root@kali:~# recoverdm --help
 recoverdm: invalid option -- '-'
 Usage: recoverdm -t <type> -i <file/device-in> -o <fileout> [-l <sectorsfile>] [-n # retries]
                  [-s rotation speed (CD-ROM etc.)] [-r # CD/DVD RAW read retries]
                  [-b start offset] [-p skip blocks count]
 Number of retries defaults to 6. For CD-ROMs it's advised to use 1.
 Number of CD/DVD RAW read retries defaults to 6. It is advised to use at least 3.
 CD-ROM (and DVD) speed defaults to 1.
 Skip blocks count is how many sectors are skipped after non-read one. Use
 more to speed-up the recover process. Default is 1.
 Type can be:
 	FILE		1
 	FLOPPY		10
 	FLOPPY_IDE	11
 	FLOPPY_SCSI	12
 	CDROM_IDE	20
 	CDROM_SCSI	21
 	DVD_IDE		30
 	DVD_SCSI	31
 	DISK_IDE	40
 	DISK_SCSI	41
 -l generates a mapfile containing checksums and a list of badsectors. This map-
    file can then be used with `mergebad' to create one correct image from
    several damaged images
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
