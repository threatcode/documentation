---
Title: slimtoolkit
Homepage: https://github.com/slimtoolkit/slim
Repository: https://gitlab.com/kalilinux/packages/slimtoolkit
Architectures: amd64 arm64 armel armhf
Version: 1.40.6-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### slimtoolkit
 
  This package contains Slim(toolkit). It was called DockerSlim, and it is
  now just Slim (SlimToolkit).
   
  It is a tool for developers with a number of different commands (build, xray,
  lint, debug and others) to simplify and optimize your developer experience
  with containers. It makes your containers better, smaller and more secure
  while providing advanced visibility and improved usability working with the
 
 **Installed size:** `65.77 MB`  
 **How to install:** `sudo apt install slimtoolkit`  
 
 {{< spoiler "Dependencies:" >}}
 * docker.io
 * libc6 
 {{< /spoiler >}}
 
 ##### slim-sensor
 
 
 ```
 root@kali:~# slim-sensor -h
 Usage of slim-sensor:
   -a string
     	set path to an executable that'll be invoked at various sensor lifecycle events (post-start, pre-shutdown, etc)
   -appbom
     	get sensor application BOM
   -artifacts-dir string
     	output director for all sensor artifacts (default "/opt/_slim/artifacts")
   -b	get sensor application BOM
   -c string
     	provide a JSONL-encoded file with one ore more sensor commands (standalone mode only) (default "/opt/_slim/commands.json")
   -command-file string
     	provide a JSONL-encoded file with one ore more sensor commands (standalone mode only) (default "/opt/_slim/commands.json")
   -d	enable debug logging
   -debug
     	enable debug logging
   -e string
     	output director for all sensor artifacts (default "/opt/_slim/artifacts")
   -f string
     	set the logging format ('text', or 'json') (default "text")
   -l string
     	set the logging level ('debug', 'info', 'warn', 'error', 'fatal', 'panic') (default "info")
   -lifecycle-hook string
     	set path to an executable that'll be invoked at various sensor lifecycle events (post-start, pre-shutdown, etc)
   -log-file string
     	enable logging redirection to a file (allowing to keep sensor's output separate from the target app's output)
   -log-format string
     	set the logging format ('text', or 'json') (default "text")
   -log-level string
     	set the logging level ('debug', 'info', 'warn', 'error', 'fatal', 'panic') (default "info")
   -m string
     	set the sensor execution mode ('controlled' when sensor expect the driver docker-slim app to manipulate its lifecycle; or 'standalone' when sensor depends on nothing but the target app (default "controlled")
   -mode string
     	set the sensor execution mode ('controlled' when sensor expect the driver docker-slim app to manipulate its lifecycle; or 'standalone' when sensor depends on nothing but the target app (default "controlled")
   -mondel
     	enable monitor data event logging
   -n	enable monitor data event logging
   -o string
     	enable logging redirection to a file (allowing to keep sensor's output separate from the target app's output)
   -s string
     	set the signal to stop the target app (and, eventually, the sensor) (default "TERM")
   -stop-grace-period duration
     	set the time to wait for the graceful termination of the target app (before sensor SIGKILL's it) (default 5s)
   -stop-signal string
     	set the signal to stop the target app (and, eventually, the sensor) (default "TERM")
   -w duration
     	set the time to wait for the graceful termination of the target app (before sensor SIGKILL's it) (default 5s)
 ```
 
 - - -
 
 ##### slimtoolkit
 
 
 ```
 root@kali:~# slimtoolkit -h
 Incorrect Usage. flag: help requested
 
 NAME:
    slimtoolkit - inspect, optimize and debug your containers!
 
 USAGE:
    slimtoolkit [global options] command [command options] [arguments...]
 
 VERSION:
    linux|Transformer|latest|latest|latest
 
 COMMANDS:
    xray, x          Shows what's inside of your container image and reverse engineers its Dockerfile
    lint, l          Analyzes container instructions in Dockerfiles
    build, b         Analyzes, profiles and optimizes your container image auto-generating Seccomp and AppArmor security profiles
    merge, m         Merge two container images (optimized to merge minified images)
    registry, r      Execute registry operations
    profile, p       Collects fat image information and generates a fat container report
    version, v       Shows slim and docker version information
    appbom, a        Show application BOM
    help, h          Show help info
    update, u        Updates slim
    install, i       Installs slim
    edit, e          Edit container image
    probe, prb       Probe target endpoint
    convert, k       Convert container image
    run, r           Run one or more containers
    server, s        Run as an HTTP server
    debug, dbg       Debug the target container from a debug (side-car) container
    containerize, c  Containerize the target app
    internal.metadata:
      docker-cli-plugin-metadata  Plugin metadata for the docker cli
 
 GLOBAL OPTIONS:
    --report value          command report location (enabled by default; set it to "off" to disable it) (default: "slim.report.json")
    --check-version         check if the current version is outdated (default: true) [$DSLIM_CHECK_VERSION]
    --debug                 enable debug logs (default: false) [$DSLIM_DEBUG]
    --verbose               enable info logs (default: false) [$DSLIM_VERBOSE]
    --quiet                 Quiet CLI execution mode (default: false) [$DSLIM_QUIET]
    --log-level value       set the logging level ('debug', 'info', 'warn' (default), 'error', 'fatal', 'panic') (default: "warn") [$DSLIM_LOG_LEVEL]
    --log value             log file to store logs
    --log-format value      set the format used by logs ('text' (default), or 'json') (default: "text")
    --console-format value  set the console output format to use ('text' (default), or 'json') (default: "text")
    --tls                   use TLS (default: true)
    --tls-verify            verify TLS (default: true)
    --tls-cert-path value   path to TLS cert files
    --host value            Docker host address
    --state-path value      app state base path
    --in-container          app is running in a container (default: false)
    --archive-state value   archive app state to the selected Docker volume (default volume - slim-state). By default, enabled when app is running in a container (disabled otherwise). Set it to "off" to disable explicitly.
    --no-color              disable color output (default: false)
    --version, -v           print the version (default: false)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
