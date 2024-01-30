---
Title: plaso
Homepage: https://github.com/log2timeline/plaso
Repository: https://salsa.debian.org/pkg-security-team/plaso
Architectures: all
Version: 20211229-0kali1
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### plaso
 
  This is a metapackage that depends on the Python 3
  package of the Plaso libraries and scripts.
 
 **Installed size:** `40 KB`  
 **How to install:** `sudo apt install plaso`  
 
 {{< spoiler "Dependencies:" >}}
 * python3-plaso 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python3-plaso
 
  Plaso (plaso langar að safna öllu) is the Python based back-end
  engine used by tools such as log2timeline for automatic creation of a
  super timelines. The goal of log2timeline (and thus plaso) is to
  provide a single tool that can parse various log files and forensic
  artifacts from computers and related systems, such as network
  equipment to produce a single correlated timeline. This timeline can
  then be easily analysed by forensic investigators/analysts, speeding
  up investigations by correlating the vast amount of information found
  on an average computer system.
   
  This package contains a Plaso installation for Python 3.
 
 **Installed size:** `10.05 MB`  
 **How to install:** `sudo apt install python3-plaso`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-artifacts 
 * python3-certifi 
 * python3-cffi-backend 
 * python3-cffi-backend-api-max 
 * python3-cffi-backend-api-min 
 * python3-chardet 
 * python3-cryptography 
 * python3-dateutil 
 * python3-defusedxml 
 * python3-dfdatetime 
 * python3-dfvfs 
 * python3-dfwinreg 
 * python3-dtfabric 
 * python3-elasticsearch 
 * python3-fsapfs 
 * python3-future 
 * python3-idna 
 * python3-libbde 
 * python3-libcreg 
 * python3-libesedb 
 * python3-libevt 
 * python3-libevtx 
 * python3-libewf 
 * python3-libfsext 
 * python3-libfshfs 
 * python3-libfsntfs 
 * python3-libfsxfs 
 * python3-libfvde 
 * python3-libfwnt 
 * python3-libfwsi 
 * python3-liblnk 
 * python3-libluksde 
 * python3-libmodi 
 * python3-libmsiecf 
 * python3-libolecf 
 * python3-libqcow 
 * python3-libregf 
 * python3-libscca 
 * python3-libsigscan 
 * python3-libsmdev 
 * python3-libsmraw 
 * python3-libvhdi 
 * python3-libvmdk 
 * python3-libvsgpt 
 * python3-libvshadow 
 * python3-libvslvm 
 * python3-lz4 
 * python3-pefile 
 * python3-pip
 * python3-psutil 
 * python3-pyparsing 
 * python3-pyxattr 
 * python3-redis 
 * python3-requests 
 * python3-six 
 * python3-tsk 
 * python3-tz
 * python3-urllib3 
 * python3-xlsxwriter 
 * python3-yaml 
 * python3-yara 
 * python3-zmq 
 {{< /spoiler >}}
 
 ##### image_export.py
 
 
 ```
 root@kali:~# image_export.py -h
 usage: image_export.py [-h] [--troubles] [-V] [-d] [-q] [-u]
                        [--artifact_definitions PATH]
                        [--custom_artifact_definitions PATH] [--data PATH]
                        [--process_memory_limit SIZE] [--vfs_back_end TYPE]
                        [--logfile FILENAME] [--partitions PARTITIONS]
                        [--volumes VOLUMES] [--no_vss] [--vss_only]
                        [--vss_stores VSS_STORES] [--credential TYPE:DATA]
                        [--artifact_filters ARTIFACT_FILTERS]
                        [--artifact_filters_file PATH]
                        [--date-filter TYPE_START_END] [-f FILE_FILTER]
                        [-x EXTENSIONS] [--names NAMES]
                        [--signatures IDENTIFIERS] [-w PATH]
                        [--include_duplicates] [--no_hashes]
                        [IMAGE]
 
 This is a simple collector designed to export files inside an image, both within a regular RAW image as well as inside a VSS. The tool uses a collection filter that uses the same syntax as a targeted plaso filter.
 
 positional arguments:
   IMAGE                 The full path to the image file that we are about to
                         extract files from, it should be a raw image or
                         another image that Plaso supports.
 
 options:
   -h, --help            Show this help message and exit.
   --troubles            Show troubleshooting information.
   -V, --version         Show the version information.
   -d, --debug           Enable debug output.
   -q, --quiet           Disable informational output.
   -u, --unattended      Enable unattended mode and do not ask the user for
                         additional input when needed, but terminate with an
                         error instead.
   --artifact_definitions PATH, --artifact-definitions PATH
                         Path to a directory or file containing artifact
                         definitions, which are .yaml files. Artifact
                         definitions can be used to describe and quickly
                         collect data of interest, such as specific files or
                         Windows Registry keys.
   --custom_artifact_definitions PATH, --custom-artifact-definitions PATH
                         Path to a directory or file containing custom artifact
                         definitions, which are .yaml files. Artifact
                         definitions can be used to describe and quickly
                         collect data of interest, such as specific files or
                         Windows Registry keys.
   --data PATH           Path to a directory containing the data files.
   --process_memory_limit SIZE, --process-memory-limit SIZE
                         Maximum amount of memory (data segment) a process is
                         allowed to allocate in bytes, where 0 represents no
                         limit. The default limit is 4294967296 (4 GiB). This
                         applies to both the main (foreman) process and the
                         worker processes. This limit is enforced by the
                         operating system and will supersede the worker memory
                         limit (--worker_memory_limit).
   --vfs_back_end TYPE, --vfs-back-end TYPE
                         The preferred dfVFS back-end: "auto", "fsext",
                         "fshfs", "fsntfs", "tsk" or "vsgpt".
   --logfile FILENAME, --log_file FILENAME, --log-file FILENAME
                         Path of the file in which to store log messages, by
                         default this file will be named: "image_export-
                         YYYYMMDDThhmmss.log.gz". Note that the file will be
                         gzip compressed if the extension is ".gz".
   --partitions PARTITIONS, --partition PARTITIONS
                         Define partitions to be processed. A range of
                         partitions can be defined as: "3..5". Multiple
                         partitions can be defined as: "1,3,5" (a list of comma
                         separated values). Ranges and lists can also be
                         combined as: "1,3..5". The first partition is 1. All
                         partitions can be specified with: "all".
   --volumes VOLUMES, --volume VOLUMES
                         Define volumes to be processed. A range of volumes can
                         be defined as: "3..5". Multiple volumes can be defined
                         as: "1,3,5" (a list of comma separated values). Ranges
                         and lists can also be combined as: "1,3..5". The first
                         volume is 1. All volumes can be specified with: "all".
   --no_vss, --no-vss    Do not scan for Volume Shadow Snapshots (VSS). This
                         means that Volume Shadow Snapshots (VSS) are not
                         processed.
   --vss_only, --vss-only
                         Do not process the current volume if Volume Shadow
                         Snapshots (VSS) have been selected.
   --vss_stores VSS_STORES, --vss-stores VSS_STORES
                         Define Volume Shadow Snapshots (VSS) (or stores that
                         need to be processed. A range of stores can be defined
                         as: "3..5". Multiple stores can be defined as: "1,3,5"
                         (a list of comma separated values). Ranges and lists
                         can also be combined as: "1,3..5". The first store is
                         1. All stores can be defined as: "all".
   --credential TYPE:DATA
                         Define a credentials that can be used to unlock
                         encrypted volumes e.g. BitLocker. The credential is
                         defined as type:data e.g. "password:BDE-test".
                         Supported credential types are: key_data, password,
                         recovery_password, startup_key. Binary key data is
                         expected to be passed in BASE-16 encoding
                         (hexadecimal). WARNING credentials passed via command
                         line arguments can end up in logs, so use this option
                         with care.
   --artifact_filters ARTIFACT_FILTERS, --artifact-filters ARTIFACT_FILTERS
                         Names of forensic artifact definitions, provided on
                         the command command line (comma separated). Forensic
                         artifacts are stored in .yaml files that are directly
                         pulled from the artifact definitions project. You can
                         also specify a custom artifacts yaml file (see
                         --custom_artifact_definitions). Artifact definitions
                         can be used to describe and quickly collect data of
                         interest, such as specific files or Windows Registry
                         keys.
   --artifact_filters_file PATH, --artifact-filters_file PATH
                         Names of forensic artifact definitions, provided in a
                         file with one artifact name per line. Forensic
                         artifacts are stored in .yaml files that are directly
                         pulled from the artifact definitions project. You can
                         also specify a custom artifacts yaml file (see
                         --custom_artifact_definitions). Artifact definitions
                         can be used to describe and quickly collect data of
                         interest, such as specific files or Windows Registry
                         keys.
   --date-filter TYPE_START_END, --date_filter TYPE_START_END
                         Filter based on file entry date and time ranges. This
                         parameter is formatted as
                         "TIME_VALUE,START_DATE_TIME,END_DATE_TIME" where
                         TIME_VALUE defines which file entry timestamp the
                         filter applies to e.g. atime, ctime, crtime, bkup,
                         etc. START_DATE_TIME and END_DATE_TIME define
                         respectively the start and end of the date time range.
                         A date time range requires at minimum start or end to
                         time of the boundary and END defines the end time.
                         Both timestamps be set. The date time values are
                         formatted as: YYYY-MM-DD hh:mm:ss.######[+-]##:##
                         Where # are numeric digits ranging from 0 to 9 and the
                         seconds fraction can be either 3 or 6 digits. The time
                         of day, seconds fraction and time zone offset are
                         optional. The default time zone is UTC. E.g. "atime,
                         2013-01-01 23:12:14, 2013-02-23". This parameter can
                         be repeated as needed to add additional date
                         boundaries, e.g. once for atime, once for crtime, etc.
   -f FILE_FILTER, --filter-file FILE_FILTER, --filter_file FILE_FILTER, --file-filter FILE_FILTER, --file_filter FILE_FILTER
                         List of files to include for targeted collection of
                         files to parse, one line per file path, setup is
                         /path|file - where each element can contain either a
                         variable set in the preprocessing stage or a regular
                         expression.
   -x EXTENSIONS, --extensions EXTENSIONS
                         Filter on file name extensions. This option accepts
                         multiple multiple comma separated values e.g.
                         "csv,docx,pst".
   --names NAMES         Filter on file names. This option accepts a comma
                         separated string denoting all file names, e.g. -x
                         "NTUSER.DAT,UsrClass.dat".
   --signatures IDENTIFIERS
                         Filter on file format signature identifiers. This
                         option accepts multiple comma separated values e.g.
                         "esedb,lnk". Use "list" to show an overview of the
                         supported file format signatures.
   -w PATH, --write PATH
                         The directory in which extracted files should be
                         stored.
   --include_duplicates, --include-duplicates
                         By default a digest hash (SHA-256) is calculated for
                         each file (data stream). These hashes are compared to
                         the previously exported files and duplicates are
                         skipped. Use this option to include duplicate files in
                         the export.
   --no_hashes, --no-hashes
                         Do not generate the hashes.json file
 
 And that is how you export files, plaso style.
 ```
 
 - - -
 
 ##### log2timeline.py
 
 
 ```
 root@kali:~# log2timeline.py -h
 usage: log2timeline.py [-h] [--troubles] [-V] [--artifact_definitions PATH]
                        [--custom_artifact_definitions PATH] [--data PATH]
                        [--artifact_filters ARTIFACT_FILTERS]
                        [--artifact_filters_file PATH] [--preferred_year YEAR]
                        [--process_archives] [--skip_compressed_streams]
                        [-f FILE_FILTER] [--hasher_file_size_limit SIZE]
                        [--hashers HASHER_LIST]
                        [--parsers PARSER_FILTER_EXPRESSION]
                        [--yara_rules PATH] [--partitions PARTITIONS]
                        [--volumes VOLUMES] [--language LANGUAGE_TAG]
                        [--no_extract_winevt_resources] [-z TIME_ZONE]
                        [--no_vss] [--vss_only] [--vss_stores VSS_STORES]
                        [--credential TYPE:DATA] [-d] [-q] [-u] [--info]
                        [--use_markdown] [--no_dependencies_check]
                        [--logfile FILENAME] [--status_view TYPE] [-t TEXT]
                        [--buffer_size BUFFER_SIZE] [--queue_size QUEUE_SIZE]
                        [--single_process] [--process_memory_limit SIZE]
                        [--temporary_directory DIRECTORY] [--vfs_back_end TYPE]
                        [--worker_memory_limit SIZE] [--worker_timeout MINUTES]
                        [--workers WORKERS] [--sigsegv_handler]
                        [--profilers PROFILERS_LIST]
                        [--profiling_directory DIRECTORY]
                        [--profiling_sample_rate SAMPLE_RATE]
                        [--storage_file PATH] [--storage_format FORMAT]
                        [--task_storage_format FORMAT]
                        [SOURCE]
 
 log2timeline is a command line tool to extract events from individual 
 files, recursing a directory (e.g. mount point) or storage media 
 image or device.
 
 More information can be gathered from here:
     https://plaso.readthedocs.io/en/latest/sources/user/Using-log2timeline.html
 
 positional arguments:
   SOURCE                Path to a source device, file or directory. If the
                         source is a supported storage media device or image
                         file, archive file or a directory, the files within
                         are processed recursively.
 
 options:
   -h, --help            Show this help message and exit.
   --troubles            Show troubleshooting information.
   -V, --version         Show the version information.
 
 data location arguments:
   --artifact_definitions PATH, --artifact-definitions PATH
                         Path to a directory or file containing artifact
                         definitions, which are .yaml files. Artifact
                         definitions can be used to describe and quickly
                         collect data of interest, such as specific files or
                         Windows Registry keys.
   --custom_artifact_definitions PATH, --custom-artifact-definitions PATH
                         Path to a directory or file containing custom artifact
                         definitions, which are .yaml files. Artifact
                         definitions can be used to describe and quickly
                         collect data of interest, such as specific files or
                         Windows Registry keys.
   --data PATH           Path to a directory containing the data files.
 
 extraction arguments:
   --artifact_filters ARTIFACT_FILTERS, --artifact-filters ARTIFACT_FILTERS
                         Names of forensic artifact definitions, provided on
                         the command command line (comma separated). Forensic
                         artifacts are stored in .yaml files that are directly
                         pulled from the artifact definitions project. You can
                         also specify a custom artifacts yaml file (see
                         --custom_artifact_definitions). Artifact definitions
                         can be used to describe and quickly collect data of
                         interest, such as specific files or Windows Registry
                         keys.
   --artifact_filters_file PATH, --artifact-filters_file PATH
                         Names of forensic artifact definitions, provided in a
                         file with one artifact name per line. Forensic
                         artifacts are stored in .yaml files that are directly
                         pulled from the artifact definitions project. You can
                         also specify a custom artifacts yaml file (see
                         --custom_artifact_definitions). Artifact definitions
                         can be used to describe and quickly collect data of
                         interest, such as specific files or Windows Registry
                         keys.
   --preferred_year YEAR, --preferred-year YEAR
                         When a format's timestamp does not include a year,
                         e.g. syslog, use this as the initial year instead of
                         attempting auto-detection.
   --process_archives, --process-archives
                         Process file entries embedded within archive files,
                         such as archive.tar and archive.zip. This can make
                         processing significantly slower.
   --skip_compressed_streams, --skip-compressed-streams
                         Skip processing file content within compressed
                         streams, such as syslog.gz and syslog.bz2.
   -f FILE_FILTER, --filter-file FILE_FILTER, --filter_file FILE_FILTER, --file-filter FILE_FILTER, --file_filter FILE_FILTER
                         List of files to include for targeted collection of
                         files to parse, one line per file path, setup is
                         /path|file - where each element can contain either a
                         variable set in the preprocessing stage or a regular
                         expression.
   --hasher_file_size_limit SIZE, --hasher-file-size-limit SIZE
                         Define the maximum file size in bytes that hashers
                         should process. Any larger file will be skipped. A
                         size of 0 represents no limit.
   --hashers HASHER_LIST
                         Define a list of hashers to use by the tool. This is a
                         comma separated list where each entry is the name of a
                         hasher, such as "md5,sha256". "all" indicates that all
                         hashers should be enabled. "none" disables all
                         hashers. Use "--hashers list" or "--info" to list the
                         available hashers.
   --parsers PARSER_FILTER_EXPRESSION
                         Define which presets, parsers and/or plugins to use,
                         or show possible values. The expression is a comma
                         separated string where each element is a preset,
                         parser or plugin name. Each element can be prepended
                         with an exclamation mark to exclude the item. Matching
                         is case insensitive. Examples: "linux,!bash_history"
                         enables the linux preset, without the bash_history
                         parser. "sqlite,!sqlite/chrome_history" enables all
                         sqlite plugins except for chrome_history".
                         "win7,syslog" enables the win7 preset, as well as the
                         syslog parser. Use "--parsers list" or "--info" to
                         list available presets, parsers and plugins.
   --yara_rules PATH, --yara-rules PATH
                         Path to a file containing Yara rules definitions.
   --partitions PARTITIONS, --partition PARTITIONS
                         Define partitions to be processed. A range of
                         partitions can be defined as: "3..5". Multiple
                         partitions can be defined as: "1,3,5" (a list of comma
                         separated values). Ranges and lists can also be
                         combined as: "1,3..5". The first partition is 1. All
                         partitions can be specified with: "all".
   --volumes VOLUMES, --volume VOLUMES
                         Define volumes to be processed. A range of volumes can
                         be defined as: "3..5". Multiple volumes can be defined
                         as: "1,3,5" (a list of comma separated values). Ranges
                         and lists can also be combined as: "1,3..5". The first
                         volume is 1. All volumes can be specified with: "all".
   --language LANGUAGE_TAG
                         The preferred language, which is used for extracting
                         and formatting Windows EventLog message strings. Use "
                         --language list" to see a list of supported language
                         tags. The en-US (LCID 0x0409) language is used as
                         fallback if preprocessing could not determine the
                         system language or no language information is
                         available in the winevt-rc.db database.
   --no_extract_winevt_resources, --no-extract-winevt-resources
                         Do not extract Windows EventLog resources such as
                         event message template strings. By default Windows
                         EventLog resources will be extracted when a Windows
                         EventLog parser is enabled.
   -z TIME_ZONE, --zone TIME_ZONE, --timezone TIME_ZONE
                         preferred time zone of extracted date and time values
                         that are stored without a time zone indicator. The
                         time zone is determined based on the source data where
                         possible otherwise it will default to UTC. Use "list"
                         to see a list of available time zones.
   --no_vss, --no-vss    Do not scan for Volume Shadow Snapshots (VSS). This
                         means that Volume Shadow Snapshots (VSS) are not
                         processed.
   --vss_only, --vss-only
                         Do not process the current volume if Volume Shadow
                         Snapshots (VSS) have been selected.
   --vss_stores VSS_STORES, --vss-stores VSS_STORES
                         Define Volume Shadow Snapshots (VSS) (or stores that
                         need to be processed. A range of stores can be defined
                         as: "3..5". Multiple stores can be defined as: "1,3,5"
                         (a list of comma separated values). Ranges and lists
                         can also be combined as: "1,3..5". The first store is
                         1. All stores can be defined as: "all".
   --credential TYPE:DATA
                         Define a credentials that can be used to unlock
                         encrypted volumes e.g. BitLocker. The credential is
                         defined as type:data e.g. "password:BDE-test".
                         Supported credential types are: key_data, password,
                         recovery_password, startup_key. Binary key data is
                         expected to be passed in BASE-16 encoding
                         (hexadecimal). WARNING credentials passed via command
                         line arguments can end up in logs, so use this option
                         with care.
 
 informational arguments:
   -d, --debug           Enable debug output.
   -q, --quiet           Disable informational output.
   -u, --unattended      Enable unattended mode and do not ask the user for
                         additional input when needed, but terminate with an
                         error instead.
   --info                Print out information about supported plugins and
                         parsers.
   --use_markdown, --use-markdown
                         Output lists in Markdown format use in combination
                         with "--hashers list", "--parsers list" or "--timezone
                         list"
   --no_dependencies_check, --no-dependencies-check
                         Disable the dependencies check.
   --logfile FILENAME, --log_file FILENAME, --log-file FILENAME
                         Path of the file in which to store log messages, by
                         default this file will be named: "log2timeline-
                         YYYYMMDDThhmmss.log.gz". Note that the file will be
                         gzip compressed if the extension is ".gz".
   --status_view TYPE, --status-view TYPE
                         The processing status view mode: "linear", "none" or
                         "window".
 
 output arguments:
   -t TEXT, --text TEXT  Define a free form text string that is prepended to
                         each path to make it easier to distinguish one record
                         from another in a timeline (like c:\, or host_w_c:\)
 
 processing arguments:
   --buffer_size BUFFER_SIZE, --buffer-size BUFFER_SIZE, --bs BUFFER_SIZE
                         The buffer size for the output (defaults to 196MiB).
   --queue_size QUEUE_SIZE, --queue-size QUEUE_SIZE
                         The maximum number of queued items per worker
                         (defaults to 125000)
   --single_process, --single-process
                         Indicate that the tool should run in a single process.
   --process_memory_limit SIZE, --process-memory-limit SIZE
                         Maximum amount of memory (data segment) a process is
                         allowed to allocate in bytes, where 0 represents no
                         limit. The default limit is 4294967296 (4 GiB). This
                         applies to both the main (foreman) process and the
                         worker processes. This limit is enforced by the
                         operating system and will supersede the worker memory
                         limit (--worker_memory_limit).
   --temporary_directory DIRECTORY, --temporary-directory DIRECTORY
                         Path to the directory that should be used to store
                         temporary files created during processing.
   --vfs_back_end TYPE, --vfs-back-end TYPE
                         The preferred dfVFS back-end: "auto", "fsext",
                         "fshfs", "fsntfs", "tsk" or "vsgpt".
   --worker_memory_limit SIZE, --worker-memory-limit SIZE
                         Maximum amount of memory (data segment and shared
                         memory) a worker process is allowed to consume in
                         bytes, where 0 represents no limit. The default limit
                         is 2147483648 (2 GiB). If a worker process exceeds
                         this limit it is killed by the main (foreman) process.
   --worker_timeout MINUTES, --worker-timeout MINUTES
                         Number of minutes before a worker process that is not
                         providing status updates is considered inactive. The
                         default timeout is 15.0 minutes. If a worker process
                         exceeds this timeout it is killed by the main
                         (foreman) process.
   --workers WORKERS     Number of worker processes. The default is the number
                         of available system CPUs minus one, for the main
                         (foreman) process.
   --sigsegv_handler, --sigsegv-handler
                         Enables the SIGSEGV handler. WARNING this
                         functionality is experimental and will a deadlock
                         worker process if a real segfault is caught, but not
                         signal SIGSEGV. This functionality is therefore
                         primarily intended for debugging purposes
 
 profiling arguments:
   --profilers PROFILERS_LIST
                         List of profilers to use by the tool. This is a comma
                         separated list where each entry is the name of a
                         profiler. Use "--profilers list" to list the available
                         profilers.
   --profiling_directory DIRECTORY, --profiling-directory DIRECTORY
                         Path to the directory that should be used to store the
                         profiling sample files. By default the sample files
                         are stored in the current working directory.
   --profiling_sample_rate SAMPLE_RATE, --profiling-sample-rate SAMPLE_RATE
                         Profiling sample rate (defaults to a sample every 1000
                         files).
 
 storage arguments:
   --storage_file PATH, --storage-file PATH
                         The path of the storage file. If not specified, one
                         will be made in the form <timestamp>-<source>.plaso
   --storage_format FORMAT, --storage-format FORMAT
                         Format of the storage file, the default is: sqlite.
                         Supported options: sqlite
   --task_storage_format FORMAT, --task-storage-format FORMAT
                         Format for task storage, the default is: sqlite.
                         Supported options: redis, sqlite
 
 Example usage:
 
 Run the tool against a storage media image (full kitchen sink)
     log2timeline.py /cases/mycase/storage.plaso ímynd.dd
 
 Instead of answering questions, indicate some of the options on the
 command line (including data from particular VSS stores).
     log2timeline.py --vss_stores 1,2 /cases/plaso_vss.plaso image.E01
 
 And that is how you build a timeline using log2timeline...
 ```
 
 - - -
 
 ##### pinfo.py
 
 
 ```
 root@kali:~# pinfo.py -h
 usage: pinfo.py [-h] [--troubles] [-V] [--process_memory_limit SIZE]
                 [--compare STORAGE_FILE] [--output_format FORMAT]
                 [--hash TYPE] [--report TYPE] [--sections SECTIONS_LIST] [-v]
                 [-w OUTPUTFILE]
                 [PATH]
 
 Shows information about a Plaso storage file, for example how it was collected, what information was extracted from a source, etc.
 
 positional arguments:
   PATH                  Path to a storage file.
 
 options:
   -h, --help            Show this help message and exit.
   --troubles            Show troubleshooting information.
   -V, --version         Show the version information.
   --process_memory_limit SIZE, --process-memory-limit SIZE
                         Maximum amount of memory (data segment) a process is
                         allowed to allocate in bytes, where 0 represents no
                         limit. The default limit is 4294967296 (4 GiB). This
                         applies to both the main (foreman) process and the
                         worker processes. This limit is enforced by the
                         operating system and will supersede the worker memory
                         limit (--worker_memory_limit).
   --compare STORAGE_FILE
                         The path of the storage file to compare against.
   --output_format FORMAT, --output-format FORMAT
                         Format of the output, the default is: text. Supported
                         options: json, markdown, text.
   --hash TYPE           Type of hash to output in file_hashes report.
                         Supported options: md5, sha1, sha256
   --report TYPE         Report on specific information. Supported options:
                         browser_search, chrome_extension,
                         environment_variables, file_hashes, list, none,
                         windows_services, winevt_providers
   --sections SECTIONS_LIST
                         List of sections to output. This is a comma separated
                         list where each entry is the name of a section. Use "
                         --sections list" to list the available sections and "
                         --sections all" to show all available sections.
   -v, --verbose         Print verbose output.
   -w OUTPUTFILE, --write OUTPUTFILE
                         Output filename.
 ```
 
 - - -
 
 ##### psort.py
 
 
 ```
 root@kali:~# psort.py -h
 usage: psort.py [-h] [--troubles] [-V] [--analysis PLUGIN_LIST]
                 [--process_memory_limit SIZE]
                 [--temporary_directory DIRECTORY] [--worker_memory_limit SIZE]
                 [--worker_timeout MINUTES] [--logfile FILENAME] [-d] [-q] [-u]
                 [--status_view TYPE] [--slice DATE_TIME]
                 [--slice_size SLICE_SIZE] [--slicer] [--data PATH] [-a]
                 [--language LANGUAGE_TAG] [--dynamic_time]
                 [--output_time_zone TIME_ZONE] [-o FORMAT] [-w OUTPUT_FILE]
                 [--fields FIELDS] [--additional_fields ADDITIONAL_FIELDS]
                 [--profilers PROFILERS_LIST] [--profiling_directory DIRECTORY]
                 [--profiling_sample_rate SAMPLE_RATE]
                 [PATH] [FILTER]
 
 Application to read, filter and process output from a Plaso storage file.
 
 positional arguments:
   PATH                  Path to a storage file.
 
 options:
   -h, --help            Show this help message and exit.
   --troubles            Show troubleshooting information.
   -V, --version         Show the version information.
 
 Analysis Arguments:
   --analysis PLUGIN_LIST
                         A comma separated list of analysis plugin names to be
                         loaded or "--analysis list" to see a list of available
                         plugins.
 
 Processing:
   --process_memory_limit SIZE, --process-memory-limit SIZE
                         Maximum amount of memory (data segment) a process is
                         allowed to allocate in bytes, where 0 represents no
                         limit. The default limit is 4294967296 (4 GiB). This
                         applies to both the main (foreman) process and the
                         worker processes. This limit is enforced by the
                         operating system and will supersede the worker memory
                         limit (--worker_memory_limit).
   --temporary_directory DIRECTORY, --temporary-directory DIRECTORY
                         Path to the directory that should be used to store
                         temporary files created during processing.
   --worker_memory_limit SIZE, --worker-memory-limit SIZE
                         Maximum amount of memory (data segment and shared
                         memory) a worker process is allowed to consume in
                         bytes, where 0 represents no limit. The default limit
                         is 2147483648 (2 GiB). If a worker process exceeds
                         this limit it is killed by the main (foreman) process.
   --worker_timeout MINUTES, --worker-timeout MINUTES
                         Number of minutes before a worker process that is not
                         providing status updates is considered inactive. The
                         default timeout is 15.0 minutes. If a worker process
                         exceeds this timeout it is killed by the main
                         (foreman) process.
 
 Informational Arguments:
   --logfile FILENAME, --log_file FILENAME, --log-file FILENAME
                         Path of the file in which to store log messages, by
                         default this file will be named: "psort-
                         YYYYMMDDThhmmss.log.gz". Note that the file will be
                         gzip compressed if the extension is ".gz".
   -d, --debug           Enable debug output.
   -q, --quiet           Disable informational output.
   -u, --unattended      Enable unattended mode and do not ask the user for
                         additional input when needed, but terminate with an
                         error instead.
   --status_view TYPE, --status-view TYPE
                         The processing status view mode: "linear", "none" or
                         "window".
 
 Filter Arguments:
   --slice DATE_TIME     Date and time to create a time slice around. This
                         parameter, if defined, will display all events that
                         happened X minutes before and after the defined date,
                         where X is controlled by the --slice_size option,
                         which is 5 minutes by default. The date and time must
                         be specified in ISO 8601 format including time zone
                         offset, for example: 20200619T20:09:23+02:00.
   --slice_size SLICE_SIZE, --slice-size SLICE_SIZE
                         Defines the slice size. In the case of a regular time
                         slice it defines the number of minutes the slice size
                         should be. In the case of the --slicer it determines
                         the number of events before and after a filter match
                         has been made that will be included in the result set.
                         The default value is 5. See --slice or --slicer for
                         more details about this option.
   --slicer              Create a time slice around every filter match. This
                         parameter, if defined will save all X events before
                         and after a filter match has been made. X is defined
                         by the --slice_size parameter.
   FILTER                A filter that can be used to filter the dataset before
                         it is written into storage. More information about the
                         filters and how to use them can be found here: https:/
                         /plaso.readthedocs.io/en/latest/sources/user/Event-
                         filters.html
 
 Input Arguments:
   --data PATH           Path to a directory containing the data files.
 
 Output Arguments:
   -a, --include_all, --include-all
                         By default the psort removes duplicate entries from
                         the output. This parameter changes that behavior so
                         all events are included.
   --language LANGUAGE_TAG
                         The preferred language, which is used for extracting
                         and formatting Windows EventLog message strings. Use "
                         --language list" to see a list of supported language
                         tags. The en-US (LCID 0x0409) language is used as
                         fallback if preprocessing could not determine the
                         system language or no language information is
                         available in the winevt-rc.db database.
   --dynamic_time, --dynamic-time
                         Indicate that the output should use dynamic time.
   --output_time_zone TIME_ZONE, --output-time-zone TIME_ZONE
                         time zone of date and time values written to the
                         output, if supported by the output format. Output
                         formats that support this are: dynamic and l2t_csv.
                         Use "list" to see a list of available time zones.
 
 Output Format Arguments:
   -o FORMAT, --output_format FORMAT, --output-format FORMAT
                         The output format. Use "-o list" to see a list of
                         available output formats.
   -w OUTPUT_FILE, --write OUTPUT_FILE
                         Output filename.
   --fields FIELDS       Defines which fields should be included in the output.
   --additional_fields ADDITIONAL_FIELDS, --additional-fields ADDITIONAL_FIELDS
                         Defines extra fields to be included in the output, in
                         addition to the default fields, which are datetime,
                         timestamp_desc, source, source_long, message, parser,
                         display_name, tag.
 
 profiling arguments:
   --profilers PROFILERS_LIST
                         List of profilers to use by the tool. This is a comma
                         separated list where each entry is the name of a
                         profiler. Use "--profilers list" to list the available
                         profilers.
   --profiling_directory DIRECTORY, --profiling-directory DIRECTORY
                         Path to the directory that should be used to store the
                         profiling sample files. By default the sample files
                         are stored in the current working directory.
   --profiling_sample_rate SAMPLE_RATE, --profiling-sample-rate SAMPLE_RATE
                         Profiling sample rate (defaults to a sample every 1000
                         files).
 ```
 
 - - -
 
 ##### psteal.py
 
 
 ```
 root@kali:~# psteal.py -h
 usage: psteal.py [-h] [--troubles] [-V] [--artifact_definitions PATH]
                  [--custom_artifact_definitions PATH] [--data PATH]
                  [--preferred_year YEAR] [--process_archives]
                  [--skip_compressed_streams] [--hasher_file_size_limit SIZE]
                  [--hashers HASHER_LIST] [--parsers PARSER_FILTER_EXPRESSION]
                  [--storage_file PATH] [--partitions PARTITIONS]
                  [--volumes VOLUMES] [--language LANGUAGE_TAG]
                  [--no_extract_winevt_resources] [-z TIME_ZONE] [--no_vss]
                  [--vss_only] [--vss_stores VSS_STORES]
                  [--credential TYPE:DATA] [-d] [-q] [-u]
                  [--no_dependencies_check] [--status_view TYPE]
                  [--source SOURCE] [--dynamic_time]
                  [--output_time_zone TIME_ZONE] [-o FORMAT] [-w OUTPUT_FILE]
                  [--fields FIELDS] [--additional_fields ADDITIONAL_FIELDS]
                  [--buffer_size BUFFER_SIZE] [--queue_size QUEUE_SIZE]
                  [--single_process] [--process_memory_limit SIZE]
                  [--temporary_directory DIRECTORY] [--vfs_back_end TYPE]
                  [--worker_memory_limit SIZE] [--worker_timeout MINUTES]
                  [--workers WORKERS]
 
 psteal is a command line tool to extract events from individual 
 files, recursing a directory (e.g. mount point) or storage media 
 image or device. The output events will be stored in a storage file.
 This tool will then read the output and process the events into a CSV 
 file.
 
 More information can be gathered from here:
     https://plaso.readthedocs.io/en/latest/sources/user/Using-log2timeline.html
 
 options:
   -h, --help            Show this help message and exit.
   --troubles            Show troubleshooting information.
   -V, --version         Show the version information.
 
 data location arguments:
   --artifact_definitions PATH, --artifact-definitions PATH
                         Path to a directory or file containing artifact
                         definitions, which are .yaml files. Artifact
                         definitions can be used to describe and quickly
                         collect data of interest, such as specific files or
                         Windows Registry keys.
   --custom_artifact_definitions PATH, --custom-artifact-definitions PATH
                         Path to a directory or file containing custom artifact
                         definitions, which are .yaml files. Artifact
                         definitions can be used to describe and quickly
                         collect data of interest, such as specific files or
                         Windows Registry keys.
   --data PATH           Path to a directory containing the data files.
 
 extraction arguments:
   --preferred_year YEAR, --preferred-year YEAR
                         When a format's timestamp does not include a year,
                         e.g. syslog, use this as the initial year instead of
                         attempting auto-detection.
   --process_archives, --process-archives
                         Process file entries embedded within archive files,
                         such as archive.tar and archive.zip. This can make
                         processing significantly slower.
   --skip_compressed_streams, --skip-compressed-streams
                         Skip processing file content within compressed
                         streams, such as syslog.gz and syslog.bz2.
   --hasher_file_size_limit SIZE, --hasher-file-size-limit SIZE
                         Define the maximum file size in bytes that hashers
                         should process. Any larger file will be skipped. A
                         size of 0 represents no limit.
   --hashers HASHER_LIST
                         Define a list of hashers to use by the tool. This is a
                         comma separated list where each entry is the name of a
                         hasher, such as "md5,sha256". "all" indicates that all
                         hashers should be enabled. "none" disables all
                         hashers. Use "--hashers list" or "--info" to list the
                         available hashers.
   --parsers PARSER_FILTER_EXPRESSION
                         Define which presets, parsers and/or plugins to use,
                         or show possible values. The expression is a comma
                         separated string where each element is a preset,
                         parser or plugin name. Each element can be prepended
                         with an exclamation mark to exclude the item. Matching
                         is case insensitive. Examples: "linux,!bash_history"
                         enables the linux preset, without the bash_history
                         parser. "sqlite,!sqlite/chrome_history" enables all
                         sqlite plugins except for chrome_history".
                         "win7,syslog" enables the win7 preset, as well as the
                         syslog parser. Use "--parsers list" or "--info" to
                         list available presets, parsers and plugins.
   --storage_file PATH, --storage-file PATH
                         The path of the storage file. If not specified, one
                         will be made in the form <timestamp>-<source>.plaso
   --partitions PARTITIONS, --partition PARTITIONS
                         Define partitions to be processed. A range of
                         partitions can be defined as: "3..5". Multiple
                         partitions can be defined as: "1,3,5" (a list of comma
                         separated values). Ranges and lists can also be
                         combined as: "1,3..5". The first partition is 1. All
                         partitions can be specified with: "all".
   --volumes VOLUMES, --volume VOLUMES
                         Define volumes to be processed. A range of volumes can
                         be defined as: "3..5". Multiple volumes can be defined
                         as: "1,3,5" (a list of comma separated values). Ranges
                         and lists can also be combined as: "1,3..5". The first
                         volume is 1. All volumes can be specified with: "all".
   --language LANGUAGE_TAG
                         The preferred language, which is used for extracting
                         and formatting Windows EventLog message strings. Use "
                         --language list" to see a list of supported language
                         tags. The en-US (LCID 0x0409) language is used as
                         fallback if preprocessing could not determine the
                         system language or no language information is
                         available in the winevt-rc.db database.
   --no_extract_winevt_resources, --no-extract-winevt-resources
                         Do not extract Windows EventLog resources such as
                         event message template strings. By default Windows
                         EventLog resources will be extracted when a Windows
                         EventLog parser is enabled.
   -z TIME_ZONE, --zone TIME_ZONE, --timezone TIME_ZONE
                         preferred time zone of extracted date and time values
                         that are stored without a time zone indicator. The
                         time zone is determined based on the source data where
                         possible otherwise it will default to UTC. Use "list"
                         to see a list of available time zones.
   --no_vss, --no-vss    Do not scan for Volume Shadow Snapshots (VSS). This
                         means that Volume Shadow Snapshots (VSS) are not
                         processed.
   --vss_only, --vss-only
                         Do not process the current volume if Volume Shadow
                         Snapshots (VSS) have been selected.
   --vss_stores VSS_STORES, --vss-stores VSS_STORES
                         Define Volume Shadow Snapshots (VSS) (or stores that
                         need to be processed. A range of stores can be defined
                         as: "3..5". Multiple stores can be defined as: "1,3,5"
                         (a list of comma separated values). Ranges and lists
                         can also be combined as: "1,3..5". The first store is
                         1. All stores can be defined as: "all".
   --credential TYPE:DATA
                         Define a credentials that can be used to unlock
                         encrypted volumes e.g. BitLocker. The credential is
                         defined as type:data e.g. "password:BDE-test".
                         Supported credential types are: key_data, password,
                         recovery_password, startup_key. Binary key data is
                         expected to be passed in BASE-16 encoding
                         (hexadecimal). WARNING credentials passed via command
                         line arguments can end up in logs, so use this option
                         with care.
 
 informational arguments:
   -d, --debug           Enable debug output.
   -q, --quiet           Disable informational output.
   -u, --unattended      Enable unattended mode and do not ask the user for
                         additional input when needed, but terminate with an
                         error instead.
   --no_dependencies_check, --no-dependencies-check
                         Disable the dependencies check.
   --status_view TYPE, --status-view TYPE
                         The processing status view mode: "linear", "none" or
                         "window".
 
 input arguments:
   --source SOURCE       The source to process
 
 output arguments:
   --dynamic_time, --dynamic-time
                         Indicate that the output should use dynamic time.
   --output_time_zone TIME_ZONE, --output-time-zone TIME_ZONE
                         time zone of date and time values written to the
                         output, if supported by the output format. Output
                         formats that support this are: dynamic and l2t_csv.
                         Use "list" to see a list of available time zones.
 
 output format arguments:
   -o FORMAT, --output_format FORMAT, --output-format FORMAT
                         The output format. Use "-o list" to see a list of
                         available output formats.
   -w OUTPUT_FILE, --write OUTPUT_FILE
                         Output filename.
   --fields FIELDS       Defines which fields should be included in the output.
   --additional_fields ADDITIONAL_FIELDS, --additional-fields ADDITIONAL_FIELDS
                         Defines extra fields to be included in the output, in
                         addition to the default fields, which are datetime,
                         timestamp_desc, source, source_long, message, parser,
                         display_name, tag.
 
 processing arguments:
   --buffer_size BUFFER_SIZE, --buffer-size BUFFER_SIZE, --bs BUFFER_SIZE
                         The buffer size for the output (defaults to 196MiB).
   --queue_size QUEUE_SIZE, --queue-size QUEUE_SIZE
                         The maximum number of queued items per worker
                         (defaults to 125000)
   --single_process, --single-process
                         Indicate that the tool should run in a single process.
   --process_memory_limit SIZE, --process-memory-limit SIZE
                         Maximum amount of memory (data segment) a process is
                         allowed to allocate in bytes, where 0 represents no
                         limit. The default limit is 4294967296 (4 GiB). This
                         applies to both the main (foreman) process and the
                         worker processes. This limit is enforced by the
                         operating system and will supersede the worker memory
                         limit (--worker_memory_limit).
   --temporary_directory DIRECTORY, --temporary-directory DIRECTORY
                         Path to the directory that should be used to store
                         temporary files created during processing.
   --vfs_back_end TYPE, --vfs-back-end TYPE
                         The preferred dfVFS back-end: "auto", "fsext",
                         "fshfs", "fsntfs", "tsk" or "vsgpt".
   --worker_memory_limit SIZE, --worker-memory-limit SIZE
                         Maximum amount of memory (data segment and shared
                         memory) a worker process is allowed to consume in
                         bytes, where 0 represents no limit. The default limit
                         is 2147483648 (2 GiB). If a worker process exceeds
                         this limit it is killed by the main (foreman) process.
   --worker_timeout MINUTES, --worker-timeout MINUTES
                         Number of minutes before a worker process that is not
                         providing status updates is considered inactive. The
                         default timeout is 15.0 minutes. If a worker process
                         exceeds this timeout it is killed by the main
                         (foreman) process.
   --workers WORKERS     Number of worker processes. The default is the number
                         of available system CPUs minus one, for the main
                         (foreman) process.
 
 Example usage:
 
 Run the tool against a storage media image (full kitchen sink)
     psteal.py --source ímynd.dd -w imynd.timeline.txt
 
 And that is how you build a timeline using psteal...
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
