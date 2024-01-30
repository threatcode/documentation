---
Title: vboot-utils
Homepage: https://chromium.googlesource.com/chromiumos/platform/vboot_reference
Repository: https://salsa.debian.org/debian/vboot-utils
Architectures: amd64 arm64 armel armhf i386
Version: 0~R106-15054.B-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cgpt
 
  Cgpt is a tool to manipulate GUID Partition Table from command line. It also
  supports Chromium OS extensions enabling you to change priority for kernel
  partitions.
 
 **Installed size:** `77 KB`  
 **How to install:** `sudo apt install cgpt`  
 
 {{< spoiler "Dependencies:" >}}
 * flashrom
 * libc6 
 * libuuid1 
 {{< /spoiler >}}
 
 ##### cgpt
 
 Utility to manipulate GPT partitions with Chromium OS extensions
 
 ```
 root@kali:~# cgpt -h
 
 Usage: cgpt COMMAND [OPTIONS] DRIVE
 
 Supported COMMANDs:
 
     create           Create or reset GPT headers and tables
     add              Add, edit or remove a partition entry
     show             Show partition table and entries
     repair           Repair damaged GPT headers and tables
     boot             Edit the PMBR sector for legacy BIOSes
     find             Locate a partition by its GUID
     edit             Edit a drive entry
     prioritize       Reorder the priority of all kernel partitions
     legacy           Switch between GPT and Legacy GPT
 
 For more detailed usage, use cgpt COMMAND -h
 
 ```
 
 - - -
 
 ### vboot-kernel-utils
 
  This package provides the futility program (including the vbutil_kernel
  program required to sign custom kernels in order to get them booted by Chrome
  OS devices (i.e. Chromebooks)).
 
 **Installed size:** `1014 KB`  
 **How to install:** `sudo apt install vboot-kernel-utils`  
 
 {{< spoiler "Dependencies:" >}}
 * coreboot-utils
 * flashrom
 * libc6 
 * libflashrom1
 * libssl3 
 {{< /spoiler >}}
 
 ##### futility
 
 Unified firmware utility
 
 ```
 root@kali:~# futility --help
 
 Usage: futility [options] COMMAND [args...]
 
 This is the unified firmware utility, which will eventually replace
 most of the distinct verified boot tools formerly produced by the
 vboot_reference package.
 
 When symlinked under the name of one of those previous tools, it should
 fully implement the original behavior. It can also be invoked directly
 as futility, followed by the original name as the first argument.
 
 Global options:
 
   --vb1        Use only vboot v1.0 binary formats
   --vb21       Use only vboot v2.1 binary formats
   --debug      Be noisy about what's going on
 
 The following commands are built-in:
 
   create               Create a keypair from an RSA .pem file
   dump_fmap            Display FMAP contents from a firmware image
   dump_kernel_config   Prints the kernel command line
   gbb                  Manipulate the Google Binary Block (GBB)
   gbb_utility          Legacy name for `gbb` command
   gscvd                Create RO verification structure
   help                 Show a bit of help (you're looking at it)
   load_fmap            Replace the contents of specified FMAP areas
   pcr                  Simulate a TPM PCR extension operation
   show                 Display the content of various binary components
   sign                 Sign / resign various binary components
   update               Update system firmware
   validate_rec_mrc     Validates content of Recovery MRC cache
   vbutil_firmware      Verified boot firmware utility
   vbutil_kernel        Creates, signs, and verifies the kernel partition
   vbutil_key           Wraps RSA keys with vboot headers
   vbutil_keyblock      Creates, signs, and verifies a keyblock
   verify               Verify the signatures of various binary components. This does not verify GSCVD contents.
   version              Show the futility source revision and build date
 
 Use "futility help COMMAND" for more information.
 
 ```
 
 - - -
 
 ##### vbutil_kernel
 
 Utility to sign custom kernels to boot with Chrome OS devices
 
 ```
 root@kali:~# vbutil_kernel --help
 
 Usage:  futility vbutil_kernel --pack <file> [PARAMETERS]
 
   Required parameters:
     --keyblock <file>         Keyblock in .keyblock format
     --signprivate <file>      Private key to sign kernel data,
                                 in .vbprivk format
     --version <number>        Kernel version
     --vmlinuz <file>          Linux kernel bzImage file
     --bootloader <file>       Bootloader stub
     --config <file>           Command line file
     --arch <arch>             Cpu architecture (default x86)
 
   Optional:
     --kloadaddr <address>     Assign kernel body load address
     --pad <number>            Verification padding size in bytes
     --vblockonly              Emit just the verification blob
     --flags NUM               Flags to be passed in the header
 
 OR
 
 Usage:  futility vbutil_kernel --repack <file> [PARAMETERS]
 
   Required parameters:
     --signprivate <file>      Private key to sign kernel data,
                                 in .vbprivk format
     --oldblob <file>          Previously packed kernel blob
                                 (including verification blob)
 
   Optional:
     --keyblock <file>         Keyblock in .keyblock format
     --config <file>           New command line file
     --version <number>        Kernel version
     --kloadaddr <address>     Assign kernel body load address
     --pad <number>            Verification blob size in bytes
     --vblockonly              Emit just the verification blob
 
 OR
 
 Usage:  futility vbutil_kernel --verify <file> [PARAMETERS]
 
   Optional:
     --signpubkey <file>       Public key to verify kernel keyblock,
                                 in .vbpubk format
     --verbose                 Print a more detailed report
     --keyblock <file>         Outputs the verified keyblock,
                                 in .keyblock format
     --pad <number>            Verification padding size in bytes
     --minversion <number>     Minimum combined kernel key version
 
 OR
 
 Usage:  futility vbutil_kernel --get-vmlinuz <file> [PARAMETERS]
 
   Required parameters:
     --vmlinuz-out <file>      vmlinuz image output file
 
 ```
 
 - - -
 
 ### vboot-utils
 
  This package contains a set of tools to deal with Chromebook internals,
  and the verified version of u-boot. Namely:
  bmpblk_font bmpblk_utility chromeos-tpm-recovery crossystem dev_debug_vboot
  dev_make_keypair dumpRSAPublicKey eficompress efidecompress enable_dev_usb_boot
  load_kernel_test pad_digest_utility signature_digest_utility tpm-nvsize
  tpm_init_temp_fix tpmc vbutil_what_key verify_data.
   
  The programs previously included in this package: dump_fmap dump_kernel_config
  futility gbb_utility  vbutil_firmware vbutil_key vbutil_keyblock, are now
  grouped in the futility program in the package vboot-kernel-utils.
   
  Most users don't need this package, and should look for the cgpt and
  vboot-kernel-utils packages instead.
 
 **Installed size:** `278 KB`  
 **How to install:** `sudo apt install vboot-utils`  
 
 {{< spoiler "Dependencies:" >}}
 * flashrom
 * libc6 
 * libssl3 
 * vboot-kernel-utils
 {{< /spoiler >}}
 
 ##### chromeos-tpm-recovery
 
 
 ```
 root@kali:~# chromeos-tpm-recovery -h
 ERROR: You must put a test image on a USB stick and boot it in recovery mode (this means Esc+Refresh+Power, *not* Ctrl-U!) to run this
 exiting
 ```
 
 - - -
 
 ##### crossystem
 
 Chrome OS firmware/system interface utility
 
 ```
 root@kali:~# crossystem -h
 Usage:
   crossystem [--all]
     Prints all parameters with descriptions and current values.
     If --all is specified, prints even normally hidden fields.
   crossystem [param1 [param2 [...]]]
     Prints the current value(s) of the parameter(s).
   crossystem [param1=value1] [param2=value2 [...]]]
     Sets the parameter(s) to the specified value(s).
   crossystem [param1?value1] [param2?value2 [...]]]
     Checks if the parameter(s) all contain the specified value(s).
     Stops at the first error.
 
 Valid parameters:
   arch                     [RO/str] Platform architecture
   backup_nvram_request     [RW/int] Backup the nvram somewhere at the next boot. Cleared on success.
   battery_cutoff_request   [RW/int] Cut off battery and shutdown on next boot
   block_devmode            [RW/int] Block all use of developer mode
   clear_tpm_owner_done     [RW/int] Clear TPM owner done
   clear_tpm_owner_request  [RW/int] Clear TPM owner on next boot
   cros_debug               [RO/int] OS should allow debug features
   dbg_reset                [RW/int] Debug reset mode request
   debug_build              [RO/int] OS image built for debug features
   dev_boot_altfw           [RW/int] Enable developer mode alternate bootloader
   dev_boot_signed_only     [RW/int] Enable developer mode boot only from official kernels
   dev_boot_usb             [RW/int] Enable developer mode boot from external disk (USB/SD)
   dev_default_boot         [RW/str] Default boot from disk, altfw or usb
   dev_enable_udc           [RW/int] Enable USB Device Controller
   devsw_boot               [RO/int] Developer switch position at boot
   devsw_cur                [RO/int] Developer switch current position
   diagnostic_request       [RW/int] Request diagnostic rom run on next boot
   disable_dev_request      [RW/int] Disable virtual dev-mode on next boot
   ecfw_act                 [RO/str] Active EC firmware
   post_ec_sync_delay       [RW/int] Short delay after EC software sync (persistent, writable, eve only)
   fw_prev_result           [RO/str] Firmware result of previous boot
   fw_prev_tried            [RO/str] Firmware tried on previous boot (A or B)
   fw_result                [RW/str] Firmware result this boot
   fw_tried                 [RO/str] Firmware tried this boot (A or B)
   fw_try_count             [RW/int] Number of times to try fw_try_next
   fw_try_next              [RW/str] Firmware to try next (A or B)
   fw_vboot2                [RO/int] 1 if firmware was selected by vboot2 or 0 otherwise
   fwb_tries                [RW/int] Try firmware B count
   fwid                     [RO/str] Active firmware ID
   fwupdate_tries           [RW/int] Times to try OS firmware update (inside kern_nv)
   hwid                     [RO/str] Hardware ID
   inside_vm                [RO/int] Running in a VM?
   kern_nv                  [RO/int] Non-volatile field for kernel use
   kernel_max_rollforward   [RW/int] Max kernel version to store into TPM
   kernkey_vfy              [RO/str] Type of verification done on kernel keyblock
   loc_idx                  [RW/int] Localization index for firmware screens
   mainfw_act               [RO/str] Active main firmware
   mainfw_type              [RO/str] Active main firmware type
   minios_priority          [RW/str] miniOS image to try first (A or B)
   nvram_cleared            [RW/int] Have NV settings been lost?  Write 0 to clear
   display_request          [RW/int] Should we initialize the display at boot?
   phase_enforcement        [RO/int] Board should have full security settings applied
   recovery_reason          [RO/int] Recovery mode reason for current boot
   recovery_request         [RW/int] Recovery mode request
   recovery_subcode         [RW/int] Recovery reason subcode
   recoverysw_boot          [RO/int] Recovery switch position at boot
   recoverysw_cur           [RO/int] Recovery switch current position
   recoverysw_ec_boot       [RO/int] Recovery switch position at EC boot
   ro_fwid                  [RO/str] Read-only firmware ID
   tpm_attack               [RW/int] TPM was interrupted since this flag was cleared
   tpm_fwver                [RO/int] Firmware version stored in TPM
   tpm_kernver              [RO/int] Kernel version stored in TPM
   tpm_rebooted             [RO/int] TPM requesting repeated reboot
   tried_fwb                [RO/int] Tried firmware B before A this boot
   try_ro_sync              [RO/int] try read only software sync
   vdat_flags               [RO/int] Flags from VbSharedData
   vdat_lfdebug             [RO/str] LoadFirmware() debug data (not in print-all)
   wipeout_request          [RW/int] Firmware requested factory reset (wipeout)
   wpsw_cur                 [RO/int] Firmware write protect hardware switch current position
 
 For more information, please see:
 https://chromium.googlesource.com/chromiumos/docs/+/HEAD/os_config.md#crossystem
 ```
 
 - - -
 
 ##### dev_debug_vboot
 
 
 ```
 root@kali:~# dev_debug_vboot -h
 
 Usage: dev_debug_vboot [options] [DIRECTORY]
 
 This logs as much as it can about the verified boot process. With no arguments
 it will attempt to read the current BIOS, extract the firmware keys, and use
 those keys to validate all the ChromeOS kernel partitions it can find. A
 summary output is printed on stdout, and the detailed log is copied to
 /var/log/debug_vboot_noisy.log afterwards.
 
 If a directory is given, it will attempt to use the components from that
 directory and will leave the detailed log in that directory.
 
 Options:
 
    -b FILE, --bios FILE        Specify the BIOS image to use
    -i FILE, --image FILE       Specify the disk image to use
    -k FILE, --kernel FILE      Specify the kernel partition image to use
    -v                          Spew the detailed log to stdout
 
    -c, --cleanup               Delete the DIRECTORY when done
 
    -h, --help                  Print this help message and exit
 
 ```
 
 - - -
 
 ##### dumpRSAPublicKey
 
 
 ```
 root@kali:~# dumpRSAPublicKey -h
 Usage: dumpRSAPublicKey <-cert | -pub> <file>
 ```
 
 - - -
 
 ##### dump_fmap
 
 
 ```
 root@kali:~# dump_fmap --help
 
 Usage:  futility dump_fmap [OPTIONS] FLASHIMAGE [NAME...]
 
 Display (and extract) the FMAP components from a BIOS image.
 
 Options:
   -x             Extract the named sections from the file
   -h             Use a human-readable format
   -H             With -h, display any gaps
   -p             Use a format easy to parse by scripts
   -F             Use the format expected by flashrom
 
 Specify one or more NAMEs to dump only those sections.
 
 ```
 
 - - -
 
 ##### dump_kernel_config
 
 
 ```
 root@kali:~# dump_kernel_config --help
 
 Usage:  futility dump_kernel_config [--kloadaddr ADDRESS] KERNEL_PARTITION
 
 ```
 
 - - -
 
 ##### enable_dev_usb_boot
 
 
 
 - - -
 
 ##### gbb_utility
 
 
 ```
 root@kali:~# gbb_utility --help
 
 Usage:  futility gbb_utility [-g|-s|-c] [OPTIONS] bios_file [output_file]
 
 GET MODE:
 -g, --get   (default)	Get (read) from bios_file, with following options:
      --hwid          	Report hardware id (default).
      --flags         	Report header flags.
      --digest        	Report digest of hwid (>= v1.2)
  -k, --rootkey=FILE  	File name to export Root Key.
  -b, --bmpfv=FILE    	File name to export Bitmap FV.
  -r  --recoverykey=FILE	File name to export Recovery Key.
 
 SET MODE:
 -s, --set            	Set (write) to bios_file, with following options:
  -o, --output=FILE   	New file name for ouptput.
      --hwid=HWID     	The new hardware id to be changed.
      --flags=FLAGS   	The new (numeric) flags value.
  -k, --rootkey=FILE  	File name of new Root Key.
  -b, --bmpfv=FILE    	File name of new Bitmap FV.
  -r  --recoverykey=FILE	File name of new Recovery Key.
 
 CREATE MODE:
 -c, --create=hwid_size,rootkey_size,bmpfv_size,recoverykey_size
                      	Create a GBB blob by given size list.
 SAMPLE:
   gbb_utility -g bios.bin
   gbb_utility --set --hwid='New Model' -k key.bin bios.bin newbios.bin
   gbb_utility -c 0x100,0x1000,0x03DE80,0x1000 gbb.blob
 
 ```
 
 - - -
 
 ##### tpm-nvsize
 
 
 ```
 root@kali:~# tpm-nvsize -h
 running tpmc definespace 0xf004 0x1 0x1
 ```
 
 - - -
 
 ##### tpmc
 
 
 
 - - -
 
 ##### vbutil_firmware
 
 
 ```
 root@kali:~# vbutil_firmware --help
 
 Usage:  futility vbutil_firmware <--vblock|--verify> <file> [OPTIONS]
 
 For '--vblock <file>', required OPTIONS are:
 
   --keyblock <file>           Keyblock in .keyblock format
   --signprivate <file>        Signing private key in .vbprivk format
   --version <number>          Firmware version
   --fv <file>                 Firmware volume to sign
   --kernelkey <file>          Kernel subkey in .vbpubk format
 
 optional OPTIONS are:
   --flags <number>            Preamble flags (defaults to 0)
 
 For '--verify <file>', required OPTIONS are:
 
   --signpubkey <file>         Signing public key in .vbpubk format
   --fv <file>                 Firmware volume to verify
 
 For '--verify <file>', optional OPTIONS are:
   --kernelkey <file>          Write the kernel subkey to this file
 
 ```
 
 - - -
 
 ##### vbutil_key
 
 
 ```
 root@kali:~# vbutil_key --help
 
 Usage:  futility vbutil_key --pack <outfile> [PARAMETERS]
 
   Required parameters:
     --key <infile>              RSA key file (.keyb or .pem)
     --version <number>          Key version number (required for .keyb,
                                   ignored for .pem)
     --algorithm <number>        Signing algorithm to use with key:
                                   0 = (RSA1024 SHA1)
                                   1 = (RSA1024 SHA256)
                                   2 = (RSA1024 SHA512)
                                   3 = (RSA2048 SHA1)
                                   4 = (RSA2048 SHA256)
                                   5 = (RSA2048 SHA512)
                                   6 = (RSA4096 SHA1)
                                   7 = (RSA4096 SHA256)
                                   8 = (RSA4096 SHA512)
                                   9 = (RSA8192 SHA1)
                                   10 = (RSA8192 SHA256)
                                   11 = (RSA8192 SHA512)
                                   12 = (RSA2048 EXP3 SHA1)
                                   13 = (RSA2048 EXP3 SHA256)
                                   14 = (RSA2048 EXP3 SHA512)
                                   15 = (RSA3072 EXP3 SHA1)
                                   16 = (RSA3072 EXP3 SHA256)
                                   17 = (RSA3072 EXP3 SHA512)
 
 OR
 
 Usage:  futility vbutil_key --unpack <infile>
 
   Optional parameters:
     --copyto <file>             Write a copy of the key to this file.
 
 ```
 
 - - -
 
 ##### vbutil_keyblock
 
 
 ```
 root@kali:~# vbutil_keyblock --help
 
 Usage:  futility vbutil_keyblock <--pack|--unpack> <file> [OPTIONS]
 
 For '--pack <file>', required OPTIONS are:
   --datapubkey <file>         Data public key in .vbpubk format
 
 Optional OPTIONS are:
   --signprivate <file>        Signing private key in .vbprivk format.
 OR
   --signprivate_pem <file>
   --pem_algorithm <algo>
         Signing private key in .pem format and algorithm id.
 (If one of the above arguments is not specified, the keyblock will
 not be signed.)
 
   --flags <number>            Specifies allowed use conditions.
   --externalsigner "cmd"        Use an external program cmd to calculate the signatures.
 
 For '--unpack <file>', optional OPTIONS are:
   --signpubkey <file>        Signing public key in .vbpubk format. This is required to
                                 verify a signed keyblock.
   --datapubkey <file>        Write the data public key to this file.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
