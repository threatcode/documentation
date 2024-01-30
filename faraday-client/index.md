---
archived: "true"
Title: faraday-client
Homepage: https://github.com/infobyte/faraday-client
Repository: https://gitlab.com/kalilinux/packages/faraday-client
Architectures: all
Version: 1.1.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### faraday-client
 
  This package contains the GTK client for Faraday.
 
 **Installed size:** `1.12 MB`  
 **How to install:** `sudo apt install faraday-client`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-sphinxdoc 
 * python3
 * python3-cairo
 * python3-cairocffi
 * python3-colorama
 * python3-dateutil
 * python3-deprecation
 * python3-faraday-plugins
 * python3-flask
 * python3-future
 * python3-gi
 * python3-html2text
 * python3-requests
 * python3-tornado
 * python3-tqdm
 * python3-websocket
 * python3-xlsxwriter
 * zsh
 {{< /spoiler >}}
 
 ##### faraday-client
 
 
 ```
 root@kali:~# faraday-client -h
 usage: faraday-client [-h] [-n HOST] [-px PORT_XMLRPC] [-pr PORT_REST]
                       [--disable-excepthook] [--login] [--cert CERT_PATH]
                       [--gui GUI] [--cli] [-w WORKSPACE] [-r FILENAME] [-d]
                       [--nodeps] [-v]
 
 Faraday's launcher parser.
 
 options:
   -h, --help            show this help message and exit
   --disable-excepthook  Disable the application exception hook that allows to
                         send error reports to developers.
   --login               Force to ask for credentials
   --cert CERT_PATH      Path to the valid Faraday server certificate
   --gui GUI             Select interface to start faraday. Supported values
                         are gtk and 'no' (no GUI at all). Defaults to GTK
   --cli                 Set this flag to avoid GUI and use Faraday as a CLI.
   -w WORKSPACE, --workspace WORKSPACE
                         Workspace to be opened
   -r FILENAME, --report FILENAME
                         Report to be parsed by the CLI
   -d, --debug           Enables debug mode. Default = disabled
   --nodeps              Skip dependency check
   -v, --version         show program's version number and exit
 
 connection:
   -n HOST, --hostname HOST
                         The hostname where both server APIs will listen
                         (XMLRPC and RESTful). Default = localhost
   -px PORT_XMLRPC, --port-xmlrpc PORT_XMLRPC
                         Sets the port where the API XMLRPC Server will listen.
                         Default = 9876
   -pr PORT_REST, --port-rest PORT_REST
                         Sets the port where the API RESTful Server will
                         listen. Default = 9977
 ```
 
 - - -
 
 ##### fplugin
 
 
 ```
 root@kali:~# fplugin -h
 usage: fplugin [-h] [-i] [-w WORKSPACE] [-u URL] [--username USERNAME]
                [--password PASSWORD] [--cert CERT_PATH]
                [command]
 
 Using our plugin you can do different actions in the command line
 and interact with Faraday. Faraday comes with some presets for bulk
 actions such as object removal, get object information, etc.
 Any parameter not recognized by fplugin, or everything after -- will be passed on 
 to the called script.
 
 positional arguments:
   command               Command to execute. Example: ./fplugin getAllIps
                         (default: None)
 
 options:
   -h, --help            show this help message and exit
   -i, --interactive     Run in interactive mode (default: False)
   -w WORKSPACE, --workspace WORKSPACE
                         Workspace to use (default: untitled)
   -u URL, --url URL     Faraday Server URL. Example: http://localhost:5985
                         (default: http://localhost:5985)
   --username USERNAME
   --password PASSWORD
   --cert CERT_PATH      Path to the valid Faraday server certificate (default:
                         None)
 
 Available scripts:
 	- autoclose_vulns: Closes vulns from the current workspace if a certain time has passed
 	- change_vuln_status: Changes Vulns Status (to closed)
 	- create_cred: Creates new credentials
 	- create_executive_report: Creates a new executive report in current workspace
 	- create_host: Creates a new host in current workspace
 	- create_service: Creates a new service in a specified interface
 	- create_vuln: Creates a new vulnerability
 	- create_vulnweb: Creates a new website vulnerability in a specified service
 	- create_xlsx_report: Creates a xls report from current workspace
 	- del_all_hosts: Deletes all stored hosts
 	- del_all_services_closed: Deletes all services with a non open port
 	- del_all_vulns_with: Delete all vulnerabilities matched with regex
 	- fbruteforce_services: Script to perform a brute force attack on different services in a workspace
 	- filter_services: Filter services by port or service name
 	- get_all_ips: Get all scanned interfaces
 	- get_severitiy_by_cwe: Get Vulns filtered by Severity and change Severity based in CWE
 	- import_csv: Import Faraday objects from CSV file
 	- list_creds: Get all stored credentials
 	- list_hosts: List hosts
 	- list_ips: List all scanned IPs
 	- list_os: Lists all scanned OSs
 	- screenshot_server: Takes a Screenshot of the ip:ports of a given protocol
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
