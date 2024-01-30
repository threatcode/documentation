---
Title: bluez
Homepage: http://www.bluez.org
Repository: https://gitlab.com/kalilinux/packages/bluez
Architectures: linux-any all
Version: 5.70-1+kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-bluetooth kali-tools-rfid kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bluetooth
 
  This package provides all of the different plugins supported
  by the Bluez bluetooth stack.
 
 **Installed size:** `66 KB`  
 **How to install:** `sudo apt install bluetooth`  
 
 {{< spoiler "Dependencies:" >}}
 * bluez
 {{< /spoiler >}}
 
 
 - - -
 
 ### bluez
 
  This package contains tools and system daemons for using Bluetooth devices.
   
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `4.26 MB`  
 **How to install:** `sudo apt install bluez`  
 
 {{< spoiler "Dependencies:" >}}
 * default-dbus-system-bus | dbus-system-bus
 * init-system-helpers 
 * kmod
 * libasound2 
 * libc6 
 * libdbus-1-3 
 * libdw1 
 * libglib2.0-0 
 * libreadline8 
 * libudev1 
 * udev
 {{< /spoiler >}}
 
 ##### bluemoon
 
 Bluemoon configuration utility
 
 ```
 root@kali:~# bluemoon -h
 bluemoon - Bluemoon configuration utility
 Usage:
 	bluemoon [options]
 Options:
 	-A, --bdaddr [addr]    Set Bluetooth address
 	-F, --firmware [file]  Load firmware
 	-C, --check <file>     Check firmware image
 	-R, --reset            Reset controller
 	-B, --coldboot         Cold boot controller
 	-E, --exception        Trigger exception
 	-i, --index <num>      Use specified controller
 	-h, --help             Show help options
 ```
 
 - - -
 
 ##### bluetoothctl
 
 Interactive bluetooth control tool
 
 ```
 root@kali:~# man bluetoothctl
 BLUETOOTHCTL(1)             General Commands Manual            BLUETOOTHCTL(1)
 
 NAME
        bluetoothctl: - interactive bluetooth control tool
 
 DESCRIPTION
         bluetoothctl ver 5.49 Usage:
 
                bluetoothctl [options]
 
 OPTIONS
        --agent
               Register agent handler: <capability>
 
        --timeout
               Timeout in seconds for non-interactive mode
 
        --version
               Display version
 
        --help Display help
 
                                   April 2018                   BLUETOOTHCTL(1)
 ```
 
 - - -
 
 ##### bluetoothd
 
 Bluetooth daemon
 
 ```
 root@kali:~# bluetoothd -h
 Usage:
   bluetoothd [OPTION?]
 
 Help Options:
   -h, --help                  Show help options
 
 Application Options:
   -d, --debug=DEBUG           Specify debug options to enable
   -p, --plugin=NAME,..,       Specify plugins to load
   -P, --noplugin=NAME,...     Specify plugins not to load
   -f, --configfile=FILE       Specify an explicit path to the config file
   -C, --compat                Provide deprecated command line interfaces
   -E, --experimental          Enable experimental D-Bus interfaces
   -K, --kernel                Enable kernel experimental features
   -n, --nodetach              Run with logging in foreground
   -v, --version               Show version information and exit
 
 ```
 
 - - -
 
 ##### btattach
 
 Attach serial devices to BlueZ stack
 
 ```
 root@kali:~# btattach -h
 btattach - Bluetooth serial utility
 Usage:
 	btattach [options]
 options:
 	-B, --bredr <device>   Attach Primary controller
 	-A, --amp <device>     Attach AMP controller
 	-P, --protocol <proto> Specify protocol type
 	-S, --speed <baudrate> Specify which baudrate to use
 	-N, --noflowctl        Disable flow control
 	-h, --help             Show help options
 ```
 
 - - -
 
 ##### btmgmt
 
 A command-line interface of BlueZ for management Usage:
 
 ```
 root@kali:~# btmgmt -h
 btmgmt ver 5.70
 Usage:
 	btmgmt [--options] [commands]
 Options:
 	--index 	Specify adapter index
 
 	--monitor 	Enable monitor output
 	--timeout 	Timeout in seconds for non-interactive mode
 	--version 	Display version
 	--init-script 	Init script file
 	--help 		Display help
 Commands:
 	select		Select a different index
 	revision	Get the MGMT Revision
 	commands	List supported commands
 	config		Show configuration info
 	info		Show controller info
 	extinfo		Show extended controller info
 	auto-power	Power all available features
 	power		Toggle powered state
 	discov		Toggle discoverable state
 	connectable	Toggle connectable state
 	fast-conn	Toggle fast connectable state
 	bondable	Toggle bondable state
 	pairable	Toggle bondable state
 	linksec		Toggle link level security
 	ssp		Toggle SSP mode
 	sc		Toggle SC support
 	hs		Toggle HS support
 	le		Toggle LE support
 	advertising	Toggle LE advertising
 	bredr		Toggle BR/EDR support
 	privacy		Toggle privacy support
 	class		Set device major/minor class
 	disconnect	Disconnect device
 	con		List connections
 	find		Discover nearby devices
 	find-service	Discover nearby service
 	stop-find	Stop discovery
 	name		Set local name
 	pair		Pair with a remote device
 	cancelpair	Cancel pairing
 	unpair		Unpair device
 	keys		Load Link Keys
 	ltks		Load Long Term Keys
 	irks		Load Identity Resolving Keys
 	block		Block Device
 	unblock		Unblock Device
 	add-uuid	Add UUID
 	rm-uuid		Remove UUID
 	clr-uuids	Clear UUIDs
 	local-oob	Local OOB data
 	remote-oob	Remote OOB data
 	did		Set Device ID
 	static-addr	Set static address
 	public-addr	Set public address
 	ext-config	External configuration
 	debug-keys	Toggle debug keys
 	conn-info	Get connection information
 	io-cap		Set IO Capability
 	scan-params	Set Scan Parameters
 	get-clock	Get Clock Information
 	add-device	Add Device
 	del-device	Remove Device
 	clr-devices	Clear Devices
 	bredr-oob	Local OOB data (BR/EDR)
 	le-oob		Local OOB data (LE)
 	advinfo		Show advertising features
 	advsize		Show advertising size info
 	add-adv		Add advertising instance
 	rm-adv		Remove advertising instance
 	clr-adv		Clear advertising instances
 	add-ext-adv-params	Add extended advertising params
 	add-ext-adv-data	Add extended advertising data
 	appearance	Set appearance
 	phy		Get/Set PHY Configuration
 	wbs		Toggle Wideband-Speech support
 	secinfo		Show security information
 	expinfo		Show experimental features
 	exp-debug	Set debug feature
 	exp-privacy	Set LL privacy feature
 	exp-quality	Set bluetooth quality report feature
 	exp-offload	Toggle codec support
 	read-sysconfig	Read System Configuration
 	set-sysconfig	Set System Configuration
 	get-flags	Get device flags
 	set-flags	Set device flags
 
 	monitor.:
 		features	Show advertisement monitor features
 		remove		Remove advertisement monitor 
 		add-pattern	Add advertisement monitor pattern
 		add-pattern-rssi	Add advertisement monitor pattern with RSSI options
 ```
 
 - - -
 
 ##### btmon
 
 Bluetooth monitor
 
 ```
 root@kali:~# btmon -h
 btmon - Bluetooth monitor
 Usage:
 	btmon [options]
 options:
 	-r, --read <file>      Read traces in btsnoop format
 	-w, --write <file>     Save traces in btsnoop format
 	-a, --analyze <file>   Analyze traces in btsnoop format
 	                       If gnuplot is installed on the
 	                       system it will also attempt to plot
 	                       packet latency graph.
 	-s, --server <socket>  Start monitor server socket
 	-p, --priority <level> Show only priority or lower
 	-i, --index <num>      Show only specified controller
 	-d, --tty <tty>        Read data from TTY
 	-B, --tty-speed <rate> Set TTY speed (default 115200)
 	-V, --vendor <compid>  Set default company identifier
 	-M, --mgmt             Open channel for mgmt events
 	-t, --time             Show time instead of time offset
 	-T, --date             Show time and date information
 	-S, --sco              Dump SCO traffic
 	-A, --a2dp             Dump A2DP stream traffic
 	-I, --iso              Dump ISO traffic
 	-E, --ellisys [ip]     Send Ellisys HCI Injection
 	-P, --no-pager         Disable pager usage
 	-J  --jlink <device>,[<serialno>],[<interface>],[<speed>]
 	                       Read data from RTT
 	-R  --rtt [<address>],[<area>],[<name>]
 	                       RTT control block parameters
 	-C, --columns [width]  Output width if not a terminal
 	-c, --color [mode]     Output color: auto/always/never
 	-h, --help             Show help options
 ```
 
 - - -
 
 ##### ciptool
 
 Bluetooth Common ISDN Access Profile (CIP)
 
 ```
 root@kali:~# ciptool -h
 ciptool - Bluetooth Common ISDN Access Profile (CIP)
 
 Usage:
 	ciptool [options] [command]
 
 Options:
 	-i [hciX|bdaddr]   Local HCI device or BD Address
 	-h, --help         Display help
 
 Commands:
 	show               	Show remote connections
 	search             	Search for a remote device
 	connect  <bdaddr>  	Connect a remote device
 	release  [bdaddr]  	Disconnect the remote device
 	loopback <bdaddr>  	Loopback test of a device
 
 ```
 
 - - -
 
 ##### gatttool
 
 Tool for Bluetooth Low Energy device
 
 ```
 root@kali:~# gatttool -h
 Usage:
   gatttool [OPTION?]
 
 Help Options:
   -h, --help                                Show help options
   --help-all                                Show all help options
   --help-gatt                               Show all GATT commands
   --help-params                             Show all Primary Services/Characteristics arguments
   --help-char-read-write                    Show all Characteristics Value/Descriptor Read/Write arguments
 
 Application Options:
   -i, --adapter=hciX                        Specify local adapter interface
   -b, --device=MAC                          Specify remote Bluetooth address
   -t, --addr-type=[public | random]         Set LE address type. Default: public
   -m, --mtu=MTU                             Specify the MTU size
   -p, --psm=PSM                             Specify the PSM for GATT/ATT over BR/EDR
   -l, --sec-level=[low | medium | high]     Set security level. Default: low
   -I, --interactive                         Use interactive mode
 
 ```
 
 - - -
 
 ##### hciattach
 
 Attach serial devices via UART HCI to BlueZ stack
 
 ```
 root@kali:~# hciattach -h
 hciattach - HCI UART driver initialization utility
 Usage:
 	hciattach [-n] [-p] [-b] [-r] [-t timeout] [-s initial_speed] <tty> <type | id> [speed] [flow|noflow] [sleep|nosleep] [bdaddr]
 	hciattach -l
 ```
 
 - - -
 
 ##### hciconfig
 
 Configure Bluetooth devices
 
 ```
 root@kali:~# hciconfig -h
 hciconfig - HCI device configuration utility
 Usage:
 	hciconfig
 	hciconfig [-a] hciX [command ...]
 Commands:
 	up                 	Open and initialize HCI device
 	down               	Close HCI device
 	reset              	Reset HCI device
 	rstat              	Reset statistic counters
 	auth               	Enable Authentication
 	noauth             	Disable Authentication
 	encrypt            	Enable Encryption
 	noencrypt          	Disable Encryption
 	piscan             	Enable Page and Inquiry scan
 	noscan             	Disable scan
 	iscan              	Enable Inquiry scan
 	pscan              	Enable Page scan
 	ptype      [type]  	Get/Set default packet type
 	lm         [mode]  	Get/Set default link mode
 	lp         [policy]	Get/Set default link policy
 	name       [name]  	Get/Set local name
 	class      [class] 	Get/Set class of device
 	voice      [voice] 	Get/Set voice setting
 	iac        [iac]   	Get/Set inquiry access code
 	inqtpl     [level] 	Get/Set inquiry transmit power level
 	inqmode    [mode]  	Get/Set inquiry mode
 	inqdata    [data]  	Get/Set inquiry data
 	inqtype    [type]  	Get/Set inquiry scan type
 	inqparms   [win:int]	Get/Set inquiry scan window and interval
 	pageparms  [win:int]	Get/Set page scan window and interval
 	pageto     [to]    	Get/Set page timeout
 	afhmode    [mode]  	Get/Set AFH mode
 	sspmode    [mode]  	Get/Set Simple Pairing Mode
 	aclmtu     <mtu:pkt>	Set ACL MTU and number of packets
 	scomtu     <mtu:pkt>	Set SCO MTU and number of packets
 	delkey     <bdaddr>	Delete link key from the device
 	oobdata            	Get local OOB data
 	commands           	Display supported commands
 	features           	Display device features
 	version            	Display version information
 	revision           	Display revision information
 	block      <bdaddr>	Add a device to the reject list
 	unblock    <bdaddr>	Remove a device from the reject list
 	lerandaddr <bdaddr>	Set LE Random Address
 	leadv      [type]  	Enable LE advertising
 			0 - Connectable undirected advertising (default)
 			3 - Non connectable undirected advertising
 	noleadv            	Disable LE advertising
 	lestates           	Display the supported LE states
 ```
 
 - - -
 
 ##### hcitool
 
 Configure Bluetooth connections
 
 ```
 root@kali:~# hcitool -h
 hcitool - HCI Tool ver 5.70
 Usage:
 	hcitool [options] <command> [command parameters]
 Options:
 	--help	Display help
 	-i dev	HCI device
 Commands:
 	dev 	Display local devices
 	inq 	Inquire remote devices
 	scan	Scan for remote devices
 	name	Get name from remote device
 	info	Get information from remote device
 	spinq	Start periodic inquiry
 	epinq	Exit periodic inquiry
 	cmd 	Submit arbitrary HCI commands
 	con 	Display active connections
 	cc  	Create connection to remote device
 	dc  	Disconnect from remote device
 	sr  	Switch central/peripheral role
 	cpt 	Change connection packet type
 	rssi	Display connection RSSI
 	lq  	Display link quality
 	tpl 	Display transmit power level
 	afh 	Display AFH channel map
 	lp  	Set/display link policy settings
 	lst 	Set/display link supervision timeout
 	auth	Request authentication
 	enc 	Set connection encryption
 	key 	Change connection link key
 	clkoff	Read clock offset
 	clock	Read local or remote clock
 	lescan	Start LE scan
 	leinfo	Get LE remote information
 	lealadd	Add device to LE Accept List
 	lealrm	Remove device from LE Accept List
 	lealsz	Read size of LE Accept List
 	lealclr	Clear LE Accept List
 	lewladd	Deprecated. Use lealadd instead.
 	lewlrm	Deprecated. Use lealrm instead.
 	lewlsz	Deprecated. Use lealsz instead.
 	lewlclr	Deprecated. Use lealclr instead.
 	lerladd	Add device to LE Resolving List
 	lerlrm	Remove device from LE Resolving List
 	lerlclr	Clear LE Resolving List
 	lerlsz	Read size of LE Resolving List
 	lerlon	Enable LE Address Resolution
 	lerloff	Disable LE Address Resolution
 	lecc	Create a LE Connection
 	ledc	Disconnect a LE Connection
 	lecup	LE Connection Update
 
 For more information on the usage of each command use:
 	hcitool <command> --help
 ```
 
 - - -
 
 ##### hex2hcd
 
 Broadcom Bluetooth firmware converter
 
 ```
 root@kali:~# hex2hcd -h
 Broadcom Bluetooth firmware converter
 Usage:
 	hex2hcd [options] <file>
 Options:
 	-o, --output <file>    Provide firmware output file
 	-h, --help             Show help options
 ```
 
 - - -
 
 ##### l2ping
 
 Send L2CAP echo request and receive answer
 
 ```
 root@kali:~# l2ping -h
 l2ping - L2CAP ping
 Usage:
 	l2ping [-i device] [-s size] [-c count] [-t timeout] [-d delay] [-f] [-r] [-v] <bdaddr>
 	-f  Flood ping (delay = 0)
 	-r  Reverse ping
 	-v  Verify request and response payload
 ```
 
 - - -
 
 ##### l2test
 
 L2CAP testing tool
 
 ```
 root@kali:~# l2test -h
 l2test - L2CAP testing
 Usage:
 	l2test <mode> [options] [bdaddr]
 Modes:
 	-r listen and receive
 	-w listen and send
 	-d listen and dump incoming data
 	-x listen, then send, then dump incoming data
 	-t listen, then send and receive at the same time
 	-q connect, then send and receive at the same time
 	-s connect and send
 	-u connect and receive
 	-n connect and be silent
 	-y connect, then send, then dump incoming data
 	-c connect, disconnect, connect, ...
 	-m multiple connects
 	-p trigger dedicated bonding
 	-z information request
 Options:
 	[-b bytes] [-i device] [-P psm] [-J cid]
 	[-I imtu] [-O omtu]
 	[-L seconds] enable SO_LINGER
 	[-W seconds] enable deferred setup
 	[-B filename] use data packets from file
 	[-N num] send num frames (default = infinite)
 	[-C num] send num frames before delay (default = 1)
 	[-D milliseconds] delay after sending num frames (default = 0)
 	[-K milliseconds] delay before receiving (default = 0)
 	[-g milliseconds] delay before disconnecting (default = 0)
 	[-X mode] l2cap mode (help for list, default = basic)
 	[-a policy] chan policy (help for list, default = bredr)
 	[-F fcs] use CRC16 check (default = 1)
 	[-Q num] Max Transmit value (default = 3)
 	[-Z size] Transmission Window size (default = 63)
 	[-Y priority] socket priority
 	[-H size] Maximum receive buffer size
 	[-R] reliable mode
 	[-G] use connectionless channel (datagram)
 	[-U] use sock stream
 	[-A] request authentication
 	[-E] request encryption
 	[-S] secure connection
 	[-M] become central
 	[-T] enable timestamps
 	[-V type] address type (help for list, default = bredr)
 	[-e seq] initial sequence value (default = 0)
 ```
 
 - - -
 
 ##### mpris-proxy
 
 Bluetooth mpris-proxy
 
 ```
 root@kali:~# mpris-proxy -h
 Usage:
   mpris-proxy [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -e, --export      Export remote players
 
 ```
 
 - - -
 
 ##### obexctl
 
 A command-line interface of BlueZ for OBEX (file transfer)
 
 ```
 root@kali:~# man obexctl
 OBEXCTL(1)                  General Commands Manual                 OBEXCTL(1)
 
 NAME
        obexctl - A command-line interface of BlueZ for OBEX (file transfer)
 
        Usage:
 
               obexctl [options]
 
 OPTIONS
        --timeout
               Timeout in seconds for non-interactive mode
 
        --version
               Display version
 
        --help Display help
 
                                   April 2018                        OBEXCTL(1)
 ```
 
 - - -
 
 ##### rctest
 
 RFCOMM testing
 
 ```
 root@kali:~# rctest -h
 rctest - RFCOMM testing
 Usage:
 	rctest <mode> [options] [bdaddr]
 Modes:
 	-r listen and receive
 	-w listen and send
 	-d listen and dump incoming data
 	-s connect and send
 	-u connect and receive
 	-n connect and be silent
 	-c connect, disconnect, connect, ...
 	-m multiple connects
 	-a automated test (receive hcix as parameter)
 Options:
 	[-b bytes] [-i device] [-P channel] [-U uuid]
 	[-L seconds] enabled SO_LINGER option
 	[-W seconds] enable deferred setup
 	[-B filename] use data packets from file
 	[-O filename] save received data to file
 	[-N num] number of frames to send
 	[-C num] send num frames before delay (default = 1)
 	[-D milliseconds] delay after sending num frames (default = 0)
 	[-Y priority] socket priority
 	[-A] request authentication
 	[-E] request encryption
 	[-S] secure connection
 	[-M] become central
 	[-T] enable timestamps
 ```
 
 - - -
 
 ##### rfcomm
 
 RFCOMM configuration utility
 
 ```
 root@kali:~# rfcomm -h
 RFCOMM configuration utility ver 5.70
 Usage:
 	rfcomm [options] <command> <dev>
 
 Options:
 	-i, --device [hciX|bdaddr]     Local HCI device or BD Address
 	-h, --help                     Display help
 	-r, --raw                      Switch TTY into raw mode
 	-A, --auth                     Enable authentication
 	-E, --encrypt                  Enable encryption
 	-S, --secure                   Secure connection
 	-C, --central                  Become the central of a piconet
 	-L, --linger [seconds]         Set linger timeout
 	-a                             Show all devices (default)
 
 Commands:
 	bind     <dev> <bdaddr> [channel]	Bind device
 	release  <dev>                   	Release device
 	show     <dev>                   	Show device
 	connect  <dev> <bdaddr> [channel]	Connect device
 	listen   <dev> [channel [cmd]]   	Listen
 	watch    <dev> [channel [cmd]]   	Watch
 
 ```
 
 - - -
 
 ##### sdptool
 
 Control and interrogate SDP servers
 
 ```
 root@kali:~# sdptool -h
 sdptool - SDP tool v5.70
 Usage:
 	sdptool [options] <command> [command parameters]
 Options:
 	-h		Display help
 	-i		Specify source interface
 Commands:
 	search		Search for a service
 	browse		Browse all available services
 	records		Request all records
 	add 		Add local service
 	del 		Delete local service
 	get 		Get local service
 	setattr		Set/Add attribute to a SDP record
 	setseq		Set/Add attribute sequence to a SDP record
 
 Services:
 	DID SP DUN LAN FAX OPUSH FTP PRINT HS HSAG HF HFAG SAP PBAP MAP 
 	NAP GN PANU HCRP HID KEYB WIIMOTE CIP CTP A2SRC A2SNK AVRCT AVRTG 
 	UDIUE UDITE SEMCHLA SR1 SYNCML SYNCMLSERV ACTIVESYNC HOTSYNC 
 	PALMOS NOKID PCSUITE NFTP NSYNCML NGAGE APPLE IAP ISYNC GATT 
 	
 ```
 
 - - -
 
 ### bluez-cups
 
  This package contains a driver to let CUPS print to Bluetooth-connected
  printers.
   
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `114 KB`  
 **How to install:** `sudo apt install bluez-cups`  
 
 {{< spoiler "Dependencies:" >}}
 * cups
 * libc6 
 * libdbus-1-3 
 * libglib2.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### bluez-hcidump
 
  The hcidump utility allows the monitoring of Bluetooth activity.
  It provides a disassembly of the Bluetooth traffic and can display
  packets from higher level protocols such as RFCOMM, SDP and BNEP.
   
  This was the software that is independent as bluez-hcidump, but this has been
  integrated into BlueZ from BlueZ 5.0.
   
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `432 KB`  
 **How to install:** `sudo apt install bluez-hcidump`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### hcidump
 
 Parse HCI data
 
 ```
 root@kali:~# hcidump -h
 Usage: hcidump [OPTION...] [filter]
   -i, --device=hci_dev       HCI device
   -l, --snap-len=len         Snap len (in bytes)
   -p, --psm=psm              Default PSM
   -m, --manufacturer=compid  Default manufacturer
   -w, --save-dump=file       Save dump to a file
   -r, --read-dump=file       Read dump from a file
   -t, --ts                   Display time stamps
   -a, --ascii                Dump data in ascii
   -x, --hex                  Dump data in hex
   -X, --ext                  Dump data in hex and ascii
   -R, --raw                  Dump raw data
   -C, --cmtp=psm             PSM for CMTP
   -H, --hcrp=psm             PSM for HCRP
   -O, --obex=port            Channel/PSM for OBEX
   -P, --ppp=channel          Channel for PPP
   -S, --sap=channel          Channel for SAP
   -D, --pppdump=file         Extract PPP traffic
   -A, --audio=file           Extract SCO audio data
   -Y, --novendor             No vendor commands or events
   -h, --help                 Give this help list
   -v, --version              Give version information
       --usage                Give a short usage message
 ```
 
 - - -
 
 ### bluez-meshd
 
  The Bluetooth Mesh network is a new Bluetooth feature that extends "Bluetooth
  Low Energy (BLE)".
   
  This package provides daemon (meshd) and tools that provide Bluetooth mesh
  functionality.
   
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `816 KB`  
 **How to install:** `sudo apt install bluez-meshd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libdbus-1-3 
 * libell0 
 * libglib2.0-0 
 * libjson-c5 
 * libreadline8 
 {{< /spoiler >}}
 
 ##### mesh-cfgclient
 
 Generate tool a mesh configuration file in JSON format
 
 ```
 root@kali:~# man mesh-cfgclient
 MESH-CFGCLIENT:(1)          General Commands Manual         MESH-CFGCLIENT:(1)
 
 NAME
        mesh-cfgclient:  - generate tool a mesh configuration file in JSON for-
        mat
 
 DESCRIPTION
        mesh-cfgclient: - generate tool a mesh configuration file in JSON  for-
        mat Usage:
 
               mesh-cfgclient [--options] [commands]
 
 OPTIONS
        --config
               Configuration file
 
        --address-start
               Starting unicast address for remote nodes
 
        --address-range
               Net index for provisioning subnet
 
        --net-index
               (null)
 
        --monitor
               Enable monitor output
 
        --timeout
               Timeout in seconds for non-interactive mode
 
        --version
               Display version
 
        --help Display help
 
    Commands:
        create Create new mesh network with one initial node
 
        discover-unprovisioned
               Look for devices to provision
 
        appkey-create
               Create a new local AppKey
 
        appkey-import
               Import a new local AppKey
 
        appkey-update
               Update local AppKey
 
        appkey-delete
               Delete local AppKey
 
        subnet-create
               Create a new local subnet (NetKey)
 
        subnet-import
               Import a new local subnet (NetKey)
 
        subnet-update
               Update local subnet (NetKey)
 
        subnet-delete
               Delete local subnet (NetKey)
 
        subnet-set-phase
               Set subnet (NetKey) phase
 
        list-unprovisioned
               List unprovisioned devices
 
        provision
               Initiate provisioning
 
        node-import
               Import an externally provisioned remote node
 
        list-nodes
               List remote mesh nodes
 
        keys   List available keys
 
                                 September 2021              MESH-CFGCLIENT:(1)
 ```
 
 - - -
 
 ##### mesh-cfgtest
 
 Mesh configuration file test tool
 
 ```
 root@kali:~# mesh-cfgtest -h
 mesh-cfgtest: invalid option -- 'h'
 Usage:
 (null) [options]
 Options:
 	-v, --version	Show version information and exit
 	-l, --list	Only list the tests to be run
 	-p, --prefix	Run tests matching the provided prefix
 	-s, --string	Run tests matching the provided string
 ```
 
 - - -
 
 ##### meshctl
 
 Bluetooth mesh control tool
 
 ```
 root@kali:~# meshctl -h
 meshctl ver 5.70
 Usage:
 	meshctl [--options] [commands]
 Options:
 	--config 	Read local mesh config JSON files from <directory>
 	--monitor 	Enable monitor output
 	--timeout 	Timeout in seconds for non-interactive mode
 	--version 	Display version
 	--init-script 	Init script file
 	--help 		Display help
 Reading prov_db.json and local_node.json from /root/.config/meshctl directory
 ```
 
 - - -
 
 ### bluez-obexd
 
  This package contains a OBEX(OBject EXchange) daemon.
   
  OBEX is communication protocol to facilitate the exchange of the binary
  object between the devices.
   
  This was the software that is independent as obexd, but this has been
  integrated into BlueZ from BlueZ 5.0.
   
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `707 KB`  
 **How to install:** `sudo apt install bluez-obexd`  
 
 {{< spoiler "Dependencies:" >}}
 * init-system-helpers 
 * libc6 
 * libdbus-1-3 
 * libglib2.0-0 
 * libical3 
 {{< /spoiler >}}
 
 
 - - -
 
 ### bluez-source
 
  This package contains the sources and patches which are needed
  to build bluez.
   
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `91.47 MB`  
 **How to install:** `sudo apt install bluez-source`  
 
 
 - - -
 
 ### bluez-test-scripts
 
  This package contains test scripts for using BlueZ.
   
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `310 KB`  
 **How to install:** `sudo apt install bluez-test-scripts`  
 
 
 - - -
 
 ### bluez-test-tools
 
  This package contains test tools for using BlueZ.
   
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `2.76 MB`  
 **How to install:** `sudo apt install bluez-test-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * bluez 
 * libc6 
 * libdbus-1-3 
 * libglib2.0-0 
 {{< /spoiler >}}
 
 ##### b1ee
 
 Bluetooth device testing tool over internet
 
 ```
 root@kali:~# b1ee -h
 b1ee - Bluetooth device testing tool over internet
 Usage:
 	b1ee [options] <host>
 options:
 	-p, --port <port>          Specify the server port
 	-s, --sniffer-port <port>  Specify the sniffer port
 	-v, --version              Show version information
 	-h, --help                 Show help options
 ```
 
 - - -
 
 ##### bnep-tester
 
 Kernel BNEP test tool
 
 ```
 root@kali:~# bnep-tester -h
 Usage:
   bnep-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### btvirt
 
 Bluetooth emulator
 
 ```
 root@kali:~# btvirt -h
 btvirt - Bluetooth emulator
 Usage:
 	btvirt [options]
 options:
 	-d                    Enable debug
 	-S                    Create local serial port
 	-s                    Create local server sockets
 	-l[num]               Number of local controllers
 	-L                    Create LE only controller
 	-U[num]               Number of test LE controllers
 	-B                    Create BR/EDR only controller
 	-A                    Create AMP controller
 	-T[num]               Number of test AMP controllers
 	-h, --help            Show help options
 ```
 
 - - -
 
 ##### gap-tester
 
 Daemon D-Bus API test tool
 
 ```
 root@kali:~# gap-tester -h
 Usage:
   gap-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### hci-tester
 
 Bluetooth Host-Controller hardware test tool
 
 ```
 root@kali:~# hci-tester -h
 Usage:
   hci-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### hfp
 
 
 
 - - -
 
 ##### ioctl-tester
 
 
 ```
 root@kali:~# ioctl-tester -h
 Usage:
   ioctl-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### iso-tester
 
 
 ```
 root@kali:~# iso-tester -h
 Usage:
   iso-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### isotest
 
 ISO testing
 
 ```
 root@kali:~# isotest -h
 isotest - ISO testing
 Usage:
 	isotest <mode> [options] [bdaddr] [bdaddr1]...
 Modes:
 	-d, --dump [filename]    dump (server)
 	-c, --reconnect          reconnect (client)
 	-m, --multiple           multiple connects (client)
 	-r, --receive [filename] receive (server)
 	-s, --send [filename,...] connect and send (client/broadcaster)
 	-n, --silent             connect and be silent (client)
 Options:
 	[-b, --bytes <value>]
 	[-i, --device <num>]
 	[-j, --jitter <bytes>    socket/jitter buffer]
 	[-h, --help]
 	[-q, --quiet             disable packet logging]
 	[-t, --timeout <usec>    send timeout]
 	[-C, --continue]
 	[-W, --defer <seconds>]  enable deferred setup
 	[-M, --mtu <value>]
 	[-S, --sca/adv-interval <value>]
 	[-P, --packing <value>]
 	[-F, --framing <value>]
 	[-I, --interval <useconds>]
 	[-L, --latency <mseconds>]
 	[-Y, --phy <value>]
 	[-R, --rtn <value>]
 	[-B, --preset <value>]
 	[-G, --CIG/BIG <value>]
 	[-T, --CIS/BIS <value>]
 	[-V, --type <value>] address type (help for list)
 	[-N, --nbis <value>] Number of BISes to create/synchronize to
 ```
 
 - - -
 
 ##### l2cap-tester
 
 Kernel L2CAP implementation test tool
 
 ```
 root@kali:~# l2cap-tester -h
 Usage:
   l2cap-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### mesh-tester
 
 
 ```
 root@kali:~# mesh-tester -h
 Usage:
   mesh-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### mgmt-tester
 
 Kernel management interface test tool
 
 ```
 root@kali:~# mgmt-tester -h
 Usage:
   mgmt-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### rfcomm-tester
 
 Kernel RFCOMM implementation test tool
 
 ```
 root@kali:~# rfcomm-tester -h
 Usage:
   rfcomm-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### sco-tester
 
 Kernel SCO implementation test tool
 
 ```
 root@kali:~# sco-tester -h
 Usage:
   sco-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### smp-tester
 
 Kernel SMP implementation test tool
 
 ```
 root@kali:~# smp-tester -h
 Usage:
   smp-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ##### userchan-tester
 
 Kernel HCI User Channel test tool
 
 ```
 root@kali:~# userchan-tester -h
 Usage:
   userchan-tester [OPTION?]
 
 Help Options:
   -h, --help        Show help options
 
 Application Options:
   -v, --version     Show version information and exit
   -q, --quiet       Run tests without logging
   -d, --debug       Run tests with debug output
   -m, --monitor     Enable monitor output
   -l, --list        Only list the tests to be run
   -p, --prefix      Run tests matching provided prefix
   -s, --string      Run tests matching provided string
 
 ```
 
 - - -
 
 ### libbluetooth-dev
 
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
   
  This package contains the development libraries and header files you need to
  develop your programs using the libbluetooth library.
 
 **Installed size:** `903 KB`  
 **How to install:** `sudo apt install libbluetooth-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libbluetooth3 
 * libc6-dev | libc-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### libbluetooth3
 
  BlueZ is the official Linux Bluetooth protocol stack. It is an Open Source
  project distributed under GNU General Public License (GPL).
 
 **Installed size:** `292 KB`  
 **How to install:** `sudo apt install libbluetooth3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libudev1 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
