---
Title: syft
Homepage: https://github.com/anchore/syft
Repository: https://gitlab.com/kalilinux/packages/syft
Architectures: any
Version: 0.97.1+ds-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### syft
 
  This package contains a CLI tool and Go library for generating a Software Bill
  of Materials (SBOM) from container images and filesystems. Exceptional for
  vulnerability detection when used with a scanner like Grype.
   
   * Generates SBOMs for container images, filesystems, archives, and more
     to discover packages and libraries
   * Supports OCI, Docker and Singularity image formats
   * Linux distribution identification
   * Works seamlessly with Grype (a fast, modern vulnerability scanner)
   * Able to create signed SBOM attestations using the in-toto
     specification
   * Convert between SBOM formats, such as CycloneDX, SPDX, and Syft's own
     format.
 
 **Installed size:** `49.89 MB`  
 **How to install:** `sudo apt install syft`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### syft
 
 
 ```
 root@kali:~# syft -h
 Generate a packaged-based Software Bill Of Materials (SBOM) from container images and filesystems
 
 Usage:
   syft [command]
 
 Application Configuration:
 
   # (env: SYFT_CONFIG)
   config: ''
   
   # report output format (<format>=<file> to output to a file), formats=[cyclonedx-json cyclonedx-xml github-json spdx-json spdx-tag-value syft-json syft-table syft-text template] (env: SYFT_OUTPUT)
   output: 
     - 'syft-table'
   
   # file to write the default report output to (default is STDOUT) (env: SYFT_FILE)
   file: ''
   
   format:
     template:
       # specify the path to a Go template file (env: SYFT_FORMAT_TEMPLATE_PATH)
       path: ''
       
     json:
       # (env: SYFT_FORMAT_JSON_LEGACY)
       legacy: false
       
   # (env: SYFT_CHECK_FOR_APP_UPDATE)
   check-for-app-update: true
   
   # enable one or more package catalogers (env: SYFT_CATALOGERS)
   catalogers: []
   
   package:
     cataloger:
       # (env: SYFT_PACKAGE_CATALOGER_ENABLED)
       enabled: true
       
       # selection of layers to catalog, options=[squashed all-layers] (env: SYFT_PACKAGE_CATALOGER_SCOPE)
       scope: 'Squashed'
       
     # (env: SYFT_PACKAGE_SEARCH_UNINDEXED_ARCHIVES)
     search-unindexed-archives: false
     
     # (env: SYFT_PACKAGE_SEARCH_INDEXED_ARCHIVES)
     search-indexed-archives: true
     
   golang:
     # (env: SYFT_GOLANG_SEARCH_LOCAL_MOD_CACHE_LICENSES)
     search-local-mod-cache-licenses: false
     
     # (env: SYFT_GOLANG_LOCAL_MOD_CACHE_DIR)
     local-mod-cache-dir: ''
     
     # (env: SYFT_GOLANG_SEARCH_REMOTE_LICENSES)
     search-remote-licenses: false
     
     # (env: SYFT_GOLANG_PROXY)
     proxy: ''
     
     # (env: SYFT_GOLANG_NO_PROXY)
     no-proxy: ''
     
   java:
     # (env: SYFT_JAVA_USE_NETWORK)
     use-network: false
     
     # (env: SYFT_JAVA_MAVEN_URL)
     maven-url: ''
     
     # (env: SYFT_JAVA_MAX_PARENT_RECURSIVE_DEPTH)
     max-parent-recursive-depth: 0
     
   linux-kernel:
     # (env: SYFT_LINUX_KERNEL_CATALOG_MODULES)
     catalog-modules: true
     
   python:
     # (env: SYFT_PYTHON_GUESS_UNPINNED_REQUIREMENTS)
     guess-unpinned-requirements: false
     
   file-metadata:
     cataloger:
       # (env: SYFT_FILE_METADATA_CATALOGER_ENABLED)
       enabled: false
       
       # (env: SYFT_FILE_METADATA_CATALOGER_SCOPE)
       scope: 'Squashed'
       
     # (env: SYFT_FILE_METADATA_DIGESTS)
     digests: 
       - 'sha256'
     
   file-classification:
     cataloger:
       # (env: SYFT_FILE_CLASSIFICATION_CATALOGER_ENABLED)
       enabled: false
       
       # (env: SYFT_FILE_CLASSIFICATION_CATALOGER_SCOPE)
       scope: 'Squashed'
       
   file-contents:
     cataloger:
       # (env: SYFT_FILE_CONTENTS_CATALOGER_ENABLED)
       enabled: false
       
       # (env: SYFT_FILE_CONTENTS_CATALOGER_SCOPE)
       scope: 'Squashed'
       
     # (env: SYFT_FILE_CONTENTS_SKIP_FILES_ABOVE_SIZE)
     skip-files-above-size: 1048576
     
     # (env: SYFT_FILE_CONTENTS_GLOBS)
     globs: []
     
   secrets:
     cataloger:
       # (env: SYFT_SECRETS_CATALOGER_ENABLED)
       enabled: false
       
       # (env: SYFT_SECRETS_CATALOGER_SCOPE)
       scope: 'AllLayers'
       
     # (env: SYFT_SECRETS_ADDITIONAL_PATTERNS)
     additional-patterns: map[]
     
     # (env: SYFT_SECRETS_EXCLUDE_PATTERN_NAMES)
     exclude-pattern-names: []
     
     # (env: SYFT_SECRETS_REVEAL_VALUES)
     reveal-values: false
     
     # (env: SYFT_SECRETS_SKIP_FILES_ABOVE_SIZE)
     skip-files-above-size: 1048576
     
   registry:
     # (env: SYFT_REGISTRY_INSECURE_SKIP_TLS_VERIFY)
     insecure-skip-tls-verify: false
     
     # (env: SYFT_REGISTRY_INSECURE_USE_HTTP)
     insecure-use-http: false
     
     auth: []
     
     # (env: SYFT_REGISTRY_CA_CERT)
     ca-cert: ''
     
   # exclude paths from being scanned using a glob expression (env: SYFT_EXCLUDE)
   exclude: []
   
   # an optional platform specifier for container image sources (e.g. 'linux/arm64', 'linux/arm64/v8', 'arm64', 'linux') (env: SYFT_PLATFORM)
   platform: ''
   
   # (env: SYFT_NAME)
   name: ''
   
   source:
     # set the name of the target being analyzed (env: SYFT_SOURCE_NAME)
     name: ''
     
     # set the version of the target being analyzed (env: SYFT_SOURCE_VERSION)
     version: ''
     
     file:
       # (env: SYFT_SOURCE_FILE_DIGESTS)
       digests: 
         - 'sha256'
       
   # (env: SYFT_PARALLELISM)
   parallelism: 1
   
   # (env: SYFT_DEFAULT_IMAGE_PULL_SOURCE)
   default-image-pull-source: ''
   
   # base directory for scanning, no links will be followed above this directory, and all paths will be reported relative to this directory (env: SYFT_BASE_PATH)
   base-path: ''
   
   # (env: SYFT_EXCLUDE_BINARY_OVERLAP_BY_OWNERSHIP)
   exclude-binary-overlap-by-ownership: true
   
   log:
     # suppress all logging output (env: SYFT_LOG_QUIET)
     quiet: false
     
     # increase verbosity (-v = info, -vv = debug) (env: SYFT_LOG_VERBOSITY)
     verbosity: 0
     
     # explicitly set the logging level (available: [error warn info debug trace]) (env: SYFT_LOG_LEVEL)
     level: warn
     
     # file path to write logs to (env: SYFT_LOG_FILE)
     file: ''
     
   dev:
     # capture resource profiling data (available: [cpu, mem]) (env: SYFT_DEV_PROFILE)
     profile: none
     
   # (env: SYFT_KEY)
   key: 
   
   # (env: SYFT_PASSWORD)
   password: 
 
 Config Search Locations:
   - .syft.yaml
   - .syft/config.yaml
   - /root/.syft.yaml
   - /root/.config/syft/config.yaml
   - /etc/xdg/syft/config.yaml
 
 Available Commands:
   attest      Generate an SBOM as an attestation for the given [SOURCE] container image
   completion  Generate the autocompletion script for the specified shell
   convert     Convert between SBOM formats
   help        Help about any command
   login       Log in to a registry
   packages    Generate a package SBOM
   version     show version information
 
 Flags:
       --base-path string         base directory for scanning, no links will be followed above this directory, and all paths will be reported relative to this directory
       --catalogers stringArray   enable one or more package catalogers
   -c, --config string            syft configuration file
       --exclude stringArray      exclude paths from being scanned using a glob expression
       --file string              file to write the default report output to (default is STDOUT) (DEPRECATED: use: output)
   -h, --help                     help for syft
       --name string              set the name of the target being analyzed (DEPRECATED: use: source-name)
   -o, --output stringArray       report output format (<format>=<file> to output to a file), formats=[cyclonedx-json cyclonedx-xml github-json spdx-json spdx-tag-value syft-json syft-table syft-text template] (default [syft-table])
       --platform string          an optional platform specifier for container image sources (e.g. 'linux/arm64', 'linux/arm64/v8', 'arm64', 'linux')
   -q, --quiet                    suppress all logging output
   -s, --scope string             selection of layers to catalog, options=[squashed all-layers] (default "Squashed")
       --source-name string       set the name of the target being analyzed
       --source-version string    set the version of the target being analyzed
   -t, --template string          specify the path to a Go template file
   -v, --verbose count            increase verbosity (-v = info, -vv = debug)
       --version                  version for syft
 
 Use "syft [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}