---
Title: uhd
Homepage: https://www.ettus.com/sdr-software/uhd-usrp-hardware-driver/
Repository: https://salsa.debian.org/bottoms/pkg-uhd
Architectures: any all
Version: 4.5.0.0+ds1-3
Metapackages: kali-linux-everything kali-tools-rfid kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libuhd-dev
 
  Host library for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
   
  This package contains the header files for developing with libuhd.
  Doxygen generated documentation is in the uhd-host package.
 
 **Installed size:** `1.13 MB`  
 **How to install:** `sudo apt install libuhd-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libuhd4.5.0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libuhd4.5.0
 
  Host library for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
 
 **Installed size:** `14.93 MB`  
 **How to install:** `sudo apt install libuhd4.5.0`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-chrono1.74.0 
 * libboost-filesystem1.74.0 
 * libboost-serialization1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libgcc-s1 
 * libpython3.11 
 * libstdc++6 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libuhd4.5.0-dpdk
 
  Host library for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
   
  This package is built with the Data Plane Development Kit and has additional
  dependencies and system configuration requirements to use those features.
 
 **Installed size:** `15.13 MB`  
 **How to install:** `sudo apt install libuhd4.5.0-dpdk`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-chrono1.74.0 
 * libboost-filesystem1.74.0 
 * libboost-serialization1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libgcc-s1 
 * libpython3.11 
 * librte-eal23 
 * librte-ethdev23 
 * librte-hash23 
 * librte-mbuf23 
 * librte-mempool23 
 * librte-ring23 
 * libstdc++6 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libuhd4.5.0-dpdk-tests
 
  Network tests for the Universal Hardware Driver for Ettus Research products.
   
  This package is built with the Data Plane Development Kit and has additional
  dependencies and system configuration requirements to use those features.
 
 **Installed size:** `1.08 MB`  
 **How to install:** `sudo apt install libuhd4.5.0-dpdk-tests`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-filesystem1.74.0 
 * libboost-program-options1.74.0 
 * libc6 
 * libgcc-s1 
 * librte-eal23 
 * librte-ethdev23 
 * librte-hash23 
 * librte-mbuf23 
 * librte-mempool23 
 * librte-net23 
 * librte-ring23 
 * libstdc++6 
 * libuhd4.5.0-dpdk 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python3-uhd
 
  Host library for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
   
  This package contains the Python API support for Python3.
 
 **Installed size:** `3.57 MB`  
 **How to install:** `sudo apt install python3-uhd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libpython3.11 
 * libstdc++6 
 * libuhd4.5.0 
 * python3
 * python3 
 * python3-numpy 
 * python3-numpy-abi9
 * python3-ruamel.yaml
 {{< /spoiler >}}
 
 
 - - -
 
 ### uhd-doc
 
  Detailed documentation for the Universal Hardware Driver.
   
  This package includes the Doxygen generated documentation.
 
 **Installed size:** `30.84 MB`  
 **How to install:** `sudo apt install uhd-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-mathjax
 {{< /spoiler >}}
 
 
 - - -
 
 ### uhd-host
 
  Host utilities for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
   
  This package includes the uhd_find_devices application to locate and
  configure attached peripherals, the uhd_usrp_probe application to
  display hardware configuration information and Doxygen generated
  documentation.
 
 **Installed size:** `25.35 MB`  
 **How to install:** `sudo apt install uhd-host`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-filesystem1.74.0 
 * libboost-program-options1.74.0 
 * libboost-test1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libgcc-s1 
 * libncurses6 
 * libstdc++6 
 * libtinfo6 
 * libuhd4.5.0 
 * python3
 * python3-numpy 
 * python3-numpy-abi9
 * python3-requests
 {{< /spoiler >}}
 
 ##### rfnoc_image_builder
 
 Build UHD image using RFNoC blocks.
 
 ```
 root@kali:~# man rfnoc_image_builder
 UHD(1)                           User Commands                          UHD(1)
 
 NAME
        rfnoc_image_builder - Build UHD image using RFNoC blocks.
 
 USAGE
        rfnoc_image_builder [-h] (-y YAML_CONFIG | -r GRC_CONFIG) [-F FPGA_DIR]
 
        [-o IMAGE_CORE_OUTPUT] [-x ROUTER_HEX_OUTPUT]
               [-I   INCLUDE_DIR]  [-b  GRC_BLOCKS]  [-l  LOG_LEVEL]  [--gener-
               ate-only] [-d DEVICE] [-t TARGET] [-g] [-c]
 
    optional arguments:
        -h, --help
               show this help message and exit
 
        -y YAML_CONFIG, --yaml-config YAML_CONFIG
               Path to yml configuration file
 
        -r GRC_CONFIG, --grc-config GRC_CONFIG
               Path to grc file to generate config from
 
        -F FPGA_DIR, --fpga-dir FPGA_DIR
               Path to directory for the FPGA source tree.Defaults to the  FPGA
               source tree of the current repo.
 
        -o IMAGE_CORE_OUTPUT, --image-core-output IMAGE_CORE_OUTPUT
               Path  to  where to save the image core Verilog source.  Defaults
               to the directory of the YAML file,  filename  <DEVICE>_rfnoc_im-
               age_core.v
 
        -x ROUTER_HEX_OUTPUT, --router-hex-output ROUTER_HEX_OUTPUT
               Path  to  where to save the static router hex file.  Defaults to
               the  directory  of  the  YAML   file,   filename   <DEVICE>_sta-
               tic_router.hex
 
        -I INCLUDE_DIR, --include-dir INCLUDE_DIR
               Path directory of the RFNoC Out-of-Tree module
 
        -b GRC_BLOCKS, --grc-blocks GRC_BLOCKS
               Path  directory of GRC block descriptions (needed for --grc-con-
               fig only)
 
        -l LOG_LEVEL, --log-level LOG_LEVEL
               Adjust log level
 
        --generate-only
               Just generate files without building IP
 
        -d DEVICE, --device DEVICE
               Device to be programmed [x300, x310,  e310,  e320,  n300,  n310,
               n320].Needs to be specified either here, or in the configuration
               file.
 
        -t TARGET, --target TARGET
               Build target (e.g. X310_HG, N320_XG, ...). Needs to be specified
               either here, on the configuration file.
 
        -g, --GUI
               Open Vivado GUI during the FPGA building process
 
        -c, --clean-all
               Cleans the IP before a new build
 
        [-o IMAGE_CORE_OUTPUT] [-x ROUTER_HEX_OUTPUT]
               [-I   INCLUDE_DIR]  [-b  GRC_BLOCKS]  [-l  LOG_LEVEL]  [--gener-
               ate-only] [-d DEVICE] [-t TARGET] [-g] [-c]
 
 SEE ALSO
        UHD documentation: https://files.ettus.com/manual/
 
        Other UHD programs:
 
        uhd_cal_tx_dc_offset(1)    uhd_cal_rx_iq_balance(1)    uhd_images_down-
        loader(1) uhd_config_info(1) uhd_find_devices(1)
 
 AUTHOR
        This manual page was written by Maitland Bottoms for the Debian project
        (but may be used by others).
 
 COPYRIGHT
        Copyright (c) 2020 Ettus Research LLC
 
        This program is free software: you can redistribute it and/or modify it
        under  the  terms of the GNU General Public License as published by the
        Free Software Foundation, either version 3 of the License, or (at  your
        option) any later version.
 
        This  program  is  distributed  in the hope that it will be useful, but
        WITHOUT ANY  WARRANTY;  without  even  the  implied  warranty  of  MER-
        CHANTABILITY  or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General
        Public License for more details.
 
 UHD 4                             August 2020                           UHD(1)
 ```
 
 - - -
 
 ##### uhd_adc_self_cal
 
 Invoke calibration in some UHD devices.
 
 ```
 root@kali:~# uhd_adc_self_cal --help
 UHD ADC self calibration Allowed options:
   --help                help message
   --version             print the version string and exit
   --args arg            device address args
 
 ```
 
 - - -
 
 ##### uhd_cal_rx_iq_balance
 
 Generate RX IQ Balance Calibration Table for a UHD Device
 
 ```
 root@kali:~# uhd_cal_rx_iq_balance --help
 USRP Generate RX IQ Balance Calibration Table Allowed options:
   --help                                help message
   --verbose                             enable some verbose
   --args arg                            Device address args [default = ""]
   --subdev arg                          Subdevice specification (default: first
                                         subdevice, often 'A')
   --tx_wave_ampl arg (=0.69999999999999996)
                                         Transmit wave amplitude
   --tx_offset arg (=934400)             TX LO offset from the RX LO in Hz
   --freq_start arg                      Frequency start in Hz (do not specify 
                                         for default)
   --freq_stop arg                       Frequency stop in Hz (do not specify 
                                         for default)
   --freq_step arg (=7300000)            Step size for LO sweep in Hz
   --nsamps arg                          Samples per data capture
   --precision arg (=0.0001)             Correction precision (default=0.0001)
 
 This application measures leakage between RX and TX on a transceiver daughterboard to self-calibrate.
 Note: Not all daughterboards support this feature. Refer to the UHD manual for details.
 
 ```
 
 - - -
 
 ##### uhd_cal_tx_dc_offset
 
 Generate TX DC Offset Calibration Table for a UHD Device
 
 ```
 root@kali:~# uhd_cal_tx_dc_offset --help
 USRP Generate TX DC Offset Calibration Table Allowed options:
   --help                                help message
   --verbose                             enable some verbose
   --args arg                            device address args [default = ""]
   --subdev arg                          Subdevice specification (default: first
                                         subdevice, often 'A')
   --tx_wave_freq arg (=507123)          Transmit wave frequency in Hz
   --tx_wave_ampl arg (=0.69999999999999996)
                                         Transmit wave amplitude
   --rx_offset arg (=934400)             RX LO offset from the TX LO in Hz
   --freq_start arg                      Frequency start in Hz (do not specify 
                                         for default)
   --freq_stop arg                       Frequency stop in Hz (do not specify 
                                         for default)
   --freq_step arg (=7300000)            Step size for LO sweep in Hz
   --nsamps arg                          Samples per data capture
   --precision arg (=0.0001)             Correction precision (default=0.0001)
 
 This application measures leakage between RX and TX on a transceiver daughterboard to self-calibrate.
 Note: Not all daughterboards support this feature. Refer to the UHD manual for details.
 
 ```
 
 - - -
 
 ##### uhd_cal_tx_iq_balance
 
 Generate TX IQ Balance Calibration Table for a UHD Device
 
 ```
 root@kali:~# uhd_cal_tx_iq_balance --help
 USRP Generate TX IQ Balance Calibration Table Allowed options:
   --help                                help message
   --verbose                             enable some verbose
   --args arg                            device address args [default = ""]
   --subdev arg                          Subdevice specification (default: first
                                         subdevice, often 'A')
   --tx_wave_freq arg (=507123)          Transmit wave frequency in Hz
   --tx_wave_ampl arg (=0.69999999999999996)
                                         Transmit wave amplitude
   --rx_offset arg (=934400)             RX LO offset from the TX LO in Hz
   --freq_start arg                      Frequency start in Hz (do not specify 
                                         for default)
   --freq_stop arg                       Frequency stop in Hz (do not specify 
                                         for default)
   --freq_step arg (=7300000)            Step size for LO sweep in Hz
   --nsamps arg                          Samples per data capture
   --precision arg (=0.0001)             Correction precision (default=0.0001)
 
 This application measures leakage between RX and TX on a transceiver daughterboard to self-calibrate.
 Note: Not all daughterboards support this feature. Refer to the UHD manual for details.
 
 ```
 
 - - -
 
 ##### uhd_config_info
 
 USRP Hardware Driver Build Configuration Info
 
 ```
 root@kali:~# uhd_config_info --help
 UHD Config Info - Allowed Options:
   --build-date          Print build date
   --c-compiler          Print C compiler
   --cxx-compiler        Print C++ compiler
   --c-flags             Print C compiler flags
   --cxx-flags           Print C++ compiler flags
   --enabled-components  Print built-time enabled components
   --install-prefix      Print install prefix
   --boost-version       Print Boost version
   --libusb-version      Print libusb version
   --pkg-path            Print pkg path
   --lib-path            Print library path
   --images-dir          Print images dir
   --abi-version         Print ABI version string
   --print-all           Print everything
   --version             Print this UHD build's version
   --help                Print help message
 
 ```
 
 - - -
 
 ##### uhd_find_devices
 
 USRP Hardware Driver Discovery Utility
 
 ```
 root@kali:~# uhd_find_devices --help
 UHD Find Devices Allowed options:
   --help                help message
   --args arg            device address args
 
 ```
 
 - - -
 
 ##### uhd_image_loader
 
 UHD Image Loader
 
 ```
 root@kali:~# uhd_image_loader --help
 UHD Image Loader
 
 Load firmware and/or FPGA images onto an Ettus Research device.
 
 Allowed options:
   --help                help message
   --args arg            Device args, optional loader args
   --fw-path arg         Firmware path (uses default if none specified)
   --fpga-path arg       FPGA path (uses default if none specified)
   --out-path arg        Output path/filename of the downloaded FPGA .bit file
   --no-fw               Don't burn firmware
   --no-fpga             Don't Burn FPGA
   --download            Download an image to a bit/bin file
 
 ```
 
 - - -
 
 ##### uhd_images_downloader
 
 USRP Hardware Driver firmware/FPGA downloader
 
 ```
 root@kali:~# uhd_images_downloader -h
 usage: uhd_images_downloader [-h] [-t TYPES] [-i INSTALL_LOCATION]
                              [-m MANIFEST_LOCATION] [-I INVENTORY_LOCATION]
                              [-l] [--url-only] [--buffer-size BUFFER_SIZE]
                              [--download-limit DOWNLOAD_LIMIT]
                              [--http-proxy HTTP_PROXY] [-b BASE_URL] [-k] [-T]
                              [-y] [-n] [--refetch] [-V] [-q] [-v]
 
 Download image files required for USRPs. Usage: The `uhd_images_downloader`
 should work, "out of the box", with no command line arguments. Assuming your
 computer has an internet connection to [files.ettus.com], simply run the
 utility every time you update UHD, and the installed images for your devices
 should always be up to date. Images will be downloaded on a per-target basis.
 That is, there are image packages for a desired device and configuration.
 Users can specify which image packages they would plan to use. To see a list
 of available targets, run `uhd_images_downloader --list-targets`. The left
 column of the printout will be a list of available image archives. From there,
 you can construct a regular expression which matches to the targets you wish
 to download. For example, in order to download all image packages related to
 the X300 product line, users may run `uhd_images_downloader --types x3.*`. The
 `uhd_images_downloader` uses a manifest to look-up the URLs of image packages
 to download. Downloaded images are recorded in an inventory file that lives in
 the images install location. This allows the downloader to skip images that
 were previously downloaded, and haven't changed since. Manifests are built
 into the downloader, but can also be accessed at uhd/images/manifest.txt.
 Inventory files are JSON files called `inventory.json`, by default. It is
 possible to specify the inventory file in command line arguments, but we don't
 recommend using this functionality unless you're really sure you need it.
 
 options:
   -h, --help            show this help message and exit
   -t TYPES, --types TYPES
                         RegEx to select image sets from the manifest file.
                         (default: None)
   -i INSTALL_LOCATION, --install-location INSTALL_LOCATION
                         Set custom install location for images (default: None)
   -m MANIFEST_LOCATION, --manifest-location MANIFEST_LOCATION
                         Set custom location for the manifest file (default:
                         None)
   -I INVENTORY_LOCATION, --inventory-location INVENTORY_LOCATION
                         Set custom location for the inventory file (default:
                         None)
   -l, --list-targets    Print targets in the manifest file to stdout, and
                         exit. To get relative paths only, specify an empty
                         base URL (-b ''). (default: False)
   --url-only            With -l, only print the URLs, nothing else. (default:
                         False)
   --buffer-size BUFFER_SIZE
                         Set download buffer size (default: 8192)
   --download-limit DOWNLOAD_LIMIT
                         Set threshold for download limits. Any download larger
                         than this will require approval, either interactively,
                         or by providing --yes. (default: 1073741824)
   --http-proxy HTTP_PROXY
                         Specify HTTP(S) proxy in the format
                         http[s]://user:pass@1.2.3.4:port If this this option
                         is not given, the environment variables
                         HTTP_PROXY/HTTPS_PROXY can also be used to specify a
                         proxy. (default: None)
   -b BASE_URL, --base-url BASE_URL
                         Set base URL for images download location. Defaults to
                         $UHD_IMAGES_URL if set, or
                         https://files.ettus.com/binaries/cache/ otherwise.
                         (default: None)
   -k, --keep            Keep the downloaded images archives in the image
                         directory (default: False)
   -T, --test            Verify the downloaded archives before extracting them
                         (default: False)
   -y, --yes             Answer all questions with 'yes' (for scripting
                         purposes). (default: False)
   -n, --dry-run         Print selected target without actually downloading
                         them. (default: False)
   --refetch             Ignore the inventory file and download all images.
                         (default: False)
   -V, --version         show program's version number and exit
   -q, --quiet           Decrease verbosity level (default: 0)
   -v, --verbose         Increase verbosity level (default: 0)
 ```
 
 - - -
 
 ##### uhd_usrp_probe
 
 USRP Hardware Driver Peripheral Report Utility
 
 ```
 root@kali:~# uhd_usrp_probe --help
 UHD USRP Probe Allowed options:
   --help                      help message
   --version                   print the version string and exit
   --args arg                  device address args
   --tree                      specify to print a complete property tree
   --string arg                query a string value from the property tree
   --double arg                query a double precision floating point value 
                               from the property tree
   --int arg                   query a integer value from the property tree
   --sensor arg                query a sensor value from the property tree
   --range arg                 query a range (gain, bandwidth, frequency, ...)  
                               from the property tree
   --vector                    when querying a string, interpret that as 
                               std::vector
   --init-only                 skip all queries, only initialize device
   --interactive-reg-iface arg RFNoC devices only: Spawn a shell to 
                               interactively peek and poke registers on RFNoC 
                               blocks
 
 ```
 
 - - -
 
 ##### usrp2_card_burner
 
 USRP N-Series FPGA/Firmware Burner
 
 ```
 root@kali:~# usrp2_card_burner -h
 Usage: usrp2_card_burner [options]
 
 Options:
   -h, --help   show this help message and exit
   --dev=DEV    raw device path
   --fw=FW      firmware image path (optional)
   --fpga=FPGA  fpga image path (optional)
   --list       list possible raw devices
   --force      override safety check
 ```
 
 - - -
 
 ##### usrpctl
 
 USRP Hardware Driver Peripheral Configuration Tool
 
 ```
 root@kali:~# man usrpctl
 usrpctl(1)                       User Commands                      usrpctl(1)
 
 NAME
        usrpctl - USRP Hardware Driver Peripheral Configuration Tool
 
 DESCRIPTION
        Report detailed information on UHD-supported Software Radio Peripherals
        attached by USB, network, or embedded configuration.  Allows update and
        configuration of attached devices.
 
        The  UHD  package  is  the universal hardware driver for Ettus Research
        products. The goal is to provide a host driver and API for current  and
        future Ettus Research products.  Users will be able to use the UHD dri-
        ver standalone or with 3rd party applications.
 
        Details  include unit names, revision numbers, and available sensors on
        all attached USRP motherboards and daughterboards.
 
 SYNOPSIS
        usrpctl [ID] COMMAND [OPTIONS]
 
 ID
        ID is the optional device argument. It is used to define a set of  USRP
        devices  that COMMAND should be applied to. If ID is omitted COMMAND is
        applied to all reachable devices.
 
        usrpctl understands the device args argument used by  other  UHD  tools
        like uhd_find_devices.
 
 COMMAND
        Is  the action the tool is to take. Every command can be either applied
        to a single device or a group of devices. Commands that run on a  group
        of devices repeat the command for every device.
 
        - Single device commands:
            - config: Read/write configuration variables (e.g., IP address)
            -  probe:  reads extended information about the USRP - Multi device
        commands:
            - update: Update binaries (e.g., FPGA image)
            - reset: Reset the specified subcomponent(s) of the USRP
            - find: finds all available USRPs in this network
 
 OPTIONS
        The options are not always mandatory. It depends on the given COMMAND.
 
 find command
        The find command takes no further options. If ID is not given it  scans
        the  system  for available, supported devices and prints a list of dis-
        covered devices.  The print out is compatible to uhd_find_devices.   ID
        can be used to narrow down the list of discovered devices.
 
 probe command
        Print a complete property tree:
               -tree
 
        The probe command can only be applied to a single device so make sure
        that
               ID  identifies exactly one device. Without arguments it displays
               detailed information about the device such as name, serial,  re-
               vision  numbers, firmware version sensor information on attached
               motherboard and daughterboards.
 
 reset command
        Reset MPM:
               -mpm
 
        The reset command resets specified subcomponents of a device. If ID is
        not
               given, it scans the system for available, supported devices  and
               resets the specified subcomponent of all discovered devices.
 
 EXAMPLES
        usrpctl find
                find all supported devices
 
        usrpctl type=x300,product=X310 find
                find all x310 devices
 
        usrpctl name=my_usrp find
                find a device named my_usrp
 
        usrpctl addr=192.168.10.2 find
                find a device with the given IP.
 
        usrpctl addr=192.168.10.2 probe
                display device information for USRP with the given ID
 
        usprctl name=my_usrp probe -tree
                display property tree of device with the name my_usrp
 
        usrpctl addr=192.168.10.2 reset -mpm
                Resets MPM on the device with the given IP.
 
        SEE ALSO
               UHD documentation: http://files.ettus.com/manual/
 
 COPYRIGHT
        Copyright (c) 2022 Ettus Research, A National Instruments Brand
 
        This program is free software: you can redistribute it and/or modify it
        under  the  terms of the GNU General Public License as published by the
        Free Software Foundation, either version 3 of the License, or (at  your
        option) any later version.
 
        This  program  is  distributed  in the hope that it will be useful, but
        WITHOUT ANY  WARRANTY;  without  even  the  implied  warranty  of  MER-
        CHANTABILITY  or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General
        Public License for more details.
 
 UHD                                  4.0.0                          usrpctl(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
