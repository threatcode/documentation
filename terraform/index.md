---
Title: terraform
Homepage: https://github.com/hashicorp/terraform
Repository: https://gitlab.com/kalilinux/packages/terraform
Architectures: any
Version: 1.6.3-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### terraform
 
  This package contains a tool for building, changing, and versioning
  infrastructure safely and efficiently. Terraform can manage existing and
  popular service providers as well as custom in-house solutions.
   
  Terraform enables you to safely and predictably create, change, and improve
  infrastructure. It is an open source tool that codifies APIs into declarative
  configuration files that can be shared amongst team members, treated as code,
  edited, reviewed, and versioned.
   
  The key features of Terraform are:
   * Infrastructure as Code: Infrastructure is described using a high-
     level configuration syntax. This allows a blueprint of your datacenter
     to be versioned and treated as you would any other code. Additionally,
     infrastructure can be shared and re-used.
   * Execution Plans: Terraform has a "planning" step where it
     generates an execution plan. The execution plan shows what Terraform
     will do when you call apply. This lets you avoid any surprises when
     Terraform manipulates infrastructure.
   * Resource Graph: Terraform builds a graph of all your resources,
     and parallelizes the creation and modification of any non-dependent
     resources. Because of this, Terraform builds infrastructure as
     efficiently as possible, and operators get insight into dependencies in
     their infrastructure.
   * Change Automation: Complex changesets can be applied to your
     infrastructure with minimal human interaction. With the previously
     mentioned execution plan and resource graph, you know exactly what
     Terraform will change and in what order, avoiding many possible human
     errors.
 
 **Installed size:** `77.16 MB`  
 **How to install:** `sudo apt install terraform`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### terraform
 
 
 ```
 root@kali:~# terraform -h
 Usage: terraform [global options] <subcommand> [args]
 
 The available commands for execution are listed below.
 The primary workflow commands are given first, followed by
 less common or more advanced commands.
 
 Main commands:
   init          Prepare your working directory for other commands
   validate      Check whether the configuration is valid
   plan          Show changes required by the current configuration
   apply         Create or update infrastructure
   destroy       Destroy previously-created infrastructure
 
 All other commands:
   console       Try Terraform expressions at an interactive command prompt
   fmt           Reformat your configuration in the standard style
   force-unlock  Release a stuck lock on the current workspace
   get           Install or upgrade remote Terraform modules
   graph         Generate a Graphviz graph of the steps in an operation
   import        Associate existing infrastructure with a Terraform resource
   login         Obtain and save credentials for a remote host
   logout        Remove locally-stored credentials for a remote host
   metadata      Metadata related commands
   output        Show output values from your root module
   providers     Show the providers required for this configuration
   refresh       Update the state to match remote systems
   show          Show the current state or a saved plan
   state         Advanced state management
   taint         Mark a resource instance as not fully functional
   test          Execute integration tests for Terraform modules
   untaint       Remove the 'tainted' state from a resource instance
   version       Show the current Terraform version
   workspace     Workspace management
 
 Global options (use these before the subcommand, if any):
   -chdir=DIR    Switch to a different working directory before executing the
                 given subcommand.
   -help         Show this help output, or the help for a specified subcommand.
   -version      An alias for the "version" subcommand.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
