---
Title: cosign
Homepage: https://github.com/sigstore/cosign
Repository: https://gitlab.com/kalilinux/packages/cosign
Architectures: any
Version: 2.2.1-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cosign
 
  This package contains a tool to sign OCI containers (and other artifacts)
  using Sigstore (https://sigstore.dev/)!
   
  Cosign aims to make signatures **invisible infrastructure**.
   
  Cosign supports:
   
   * "Keyless signing" with the Sigstore public good Fulcio certificate
     authority and Rekor transparency log (default)
   * Hardware and KMS signing
   * Signing with a cosign generated encrypted private/public keypair
   * Container Signing, Verification and Storage in an OCI registry.
   * Bring-your-own PKI
 
 **Installed size:** `70.33 MB`  
 **How to install:** `sudo apt install cosign`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### cosign
 
 
 ```
 root@kali:~# cosign -h
 A tool for Container Signing, Verification and Storage in an OCI registry.
 
 Usage:
 cosign [command]
 
 Available Commands:
 attach                  Provides utilities for attaching artifacts to other artifacts in a registry
 attest                  Attest the supplied container image.
 attest-blob             Attest the supplied blob.
 clean                   Remove all signatures from an image.
 completion              Generate completion script
 copy                    Copy the supplied container image and signatures.
 dockerfile              Provides utilities for discovering images in and performing operations on Dockerfiles
 download                Provides utilities for downloading artifacts and attached artifacts in a registry
 env                     Prints Cosign environment variables
 generate                Generates (unsigned) signature payloads from the supplied container image.
 generate-key-pair       Generates a key-pair.
 help                    Help about any command
 import-key-pair         Imports a PEM-encoded RSA or EC private key.
 initialize              Initializes SigStore root to retrieve trusted certificate and key targets for verification.
 load                    Load a signed image on disk to a remote registry
 login                   Log in to a registry
 manifest                Provides utilities for discovering images in and performing operations on Kubernetes manifests
 public-key              Gets a public key from the key-pair.
 save                    Save the container image and associated signatures to disk at the specified directory.
 sign                    Sign the supplied container image.
 sign-blob               Sign the supplied blob, outputting the base64-encoded signature to stdout.
 tree                    Display supply chain security related artifacts for an image such as signatures, SBOMs and attestations
 triangulate             Outputs the located cosign image reference. This is the location cosign stores the specified artifact type.
 upload                  Provides utilities for uploading artifacts to a registry
 verify                  Verify a signature on the supplied container image
 verify-attestation      Verify an attestation on the supplied container image
 verify-blob             Verify a signature on the supplied blob
 verify-blob-attestation Verify an attestation on the supplied blob
 version                 Prints the version
 
 Flags:
     -h, --help=false:
 	help for cosign
 
     --output-file='':
 	log output to a file
 
     -t, --timeout=3m0s:
 	timeout for commands
 
     -d, --verbose=false:
 	log debug output
 
 Additional help topics:
 cosign piv-tool                This cosign was not built with piv-tool support!
 cosign pkcs11-tool             This cosign was not built with pkcs11-tool support!
 
 Use "cosign [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
