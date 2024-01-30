---
Title: witnessme
Homepage: https://github.com/byt3bl33d3r/WitnessMe
Repository: https://gitlab.com/kalilinux/packages/witnessme
Architectures: all
Version: 1.5.0+git20201026-0kali2
Metapackages: kali-linux-everything kali-tools-identify 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### witnessme
 
  This package contains a Web Inventory tool inspired by Eyewitness, its also
  written to be extensible allowing you to create custom functionality that can
  take advantage of the headless browser it drives in the back-end.
 
 **Installed size:** `401 KB`  
 **How to install:** `sudo apt install witnessme`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-aiodns
 * python3-aiosqlite
 * python3-fastapi
 * python3-jinja2
 * python3-lxml
 * python3-multipart
 * python3-prompt-toolkit
 * python3-pydantic
 * python3-pyppeteer
 * python3-terminaltables
 * python3-uvicorn
 * python3-xmltodict
 * python3-yaml
 {{< /spoiler >}}
 
 ##### witnessme
 
 
 ```
 root@kali:~# witnessme -h
 usage: witnessme [-h] [--threads THREADS] [--timeout TIMEOUT] [-d] [-v]
                  {screenshot,grab} ...
 
 WitnessMe!
 
 positional arguments:
   {screenshot,grab}
 
 options:
   -h, --help         show this help message and exit
   --threads THREADS  Number of concurrent browser tab(s) to open
                      [WARNING: This can cause huge RAM consumption if set to high values] (default: 15)
   --timeout TIMEOUT  Timeout for each connection attempt in seconds (default: 15)
   -d, --debug        Enable debug output (default: False)
   -v, --version      show program's version number and exit
 ```
 
 - - -
 
 ##### wmapi
 
 
 ```
 root@kali:~# wmapi -h
 usage: wmapi [-h] [host] [port]
 
 positional arguments:
   host        IP to bind to (default: 127.0.0.1)
   port        port to bind to (default: 8000)
 
 options:
   -h, --help  show this help message and exit
 ```
 
 - - -
 
 ##### wmdb
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
