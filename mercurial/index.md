---
Title: mercurial
Homepage: https://www.mercurial-scm.org/
Repository: https://salsa.debian.org/python-team/packages/mercurial
Architectures: any all
Version: 6.5.3-1
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### mercurial
 
  Mercurial is a fast, lightweight Source Control Management system designed
  for efficient handling of very large distributed projects.
   
  Its features include:
   * O(1) delta-compressed file storage and retrieval scheme
   * Complete cross-indexing of files and changesets for efficient exploration
     of project history
   * Robust SHA1-based integrity checking and append-only storage model
   * Decentralized development model with arbitrary merging between trees
   * High-speed HTTP-based network merge protocol
   * Easy-to-use command-line interface
   * Integrated stand-alone web interface
   * Small Python codebase
   
  This package contains the architecture dependent files.
 
 **Installed size:** `1.02 MB`  
 **How to install:** `sudo apt install mercurial`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * mercurial-common 
 * python3
 * python3 
 * ucf 
 {{< /spoiler >}}
 
 ##### chg
 
 A fast client for Mercurial command server
 
 ```
 root@kali:~# chg -h
 Mercurial Distributed SCM
 
 list of commands:
 
 Repository creation:
 
  clone         make a copy of an existing repository
  init          create a new repository in the given directory
 
 Remote repository management:
 
  incoming      show new changesets found in source
  outgoing      show changesets not found in the destination
  paths         show aliases for remote repositories
  pull          pull changes from the specified source
  push          push changes to the specified destination
  serve         start stand-alone webserver
 
 Change creation:
 
  commit        commit the specified files or all outstanding changes
 
 Change manipulation:
 
  backout       reverse effect of earlier changeset
  graft         copy changes from other branches onto the current branch
  merge         merge another revision into working directory
 
 Change organization:
 
  bookmarks     create a new bookmark or list existing bookmarks
  branch        set or show the current branch name
  branches      list repository named branches
  phase         set or show the current phase name
  tag           add one or more tags for the current or given revision
  tags          list repository tags
 
 File content management:
 
  annotate      show changeset information by line for each file
  cat           output the current or given revision of files
  copy          mark files as copied for the next commit
  diff          diff repository (or selected files)
  grep          search for a pattern in specified files
 
 Change navigation:
 
  bisect        subdivision search of changesets
  heads         show branch heads
  identify      identify the working directory or specified revision
  log           show revision history of entire repository or files
 
 Working directory management:
 
  add           add the specified files on the next commit
  addremove     add all new files, delete all missing files
  files         list tracked files
  forget        forget the specified files on the next commit
  purge         removes files not tracked by Mercurial
  remove        remove the specified files on the next commit
  rename        rename files; equivalent of copy + remove
  resolve       redo merges or set/view the merge status of files
  revert        restore files to their checkout state
  root          print the root (top) of the current working directory
  shelve        save and set aside changes from the working directory
  status        show changed files in the working directory
  summary       summarize working directory state
  unshelve      restore a shelved change to the working directory
  update        update working directory (or switch revisions)
 
 Change import/export:
 
  archive       create an unversioned archive of a repository revision
  bundle        create a bundle file
  export        dump the header and diffs for one or more changesets
  import        import an ordered set of patches
  unbundle      apply one or more bundle files
 
 Repository maintenance:
 
  manifest      output the current or given revision of the project manifest
  recover       roll back an interrupted transaction
  verify        verify the integrity of the repository
 
 Help:
 
  config        show combined config settings from all hgrc files
  help          show help for a given topic or a help overview
  version       output version and copyright information
 
 additional help topics:
 
 Mercurial identifiers:
 
  filesets      Specifying File Sets
  hgignore      Syntax for Mercurial Ignore Files
  patterns      File Name Patterns
  revisions     Specifying Revisions
  urls          URL Paths
 
 Mercurial output:
 
  color         Colorizing Outputs
  dates         Date Formats
  diffs         Diff Formats
  templating    Template Usage
 
 Mercurial configuration:
 
  config        Configuration Files
  environment   Environment Variables
  extensions    Using Additional Features
  flags         Command-line flags
  hgweb         Configuring hgweb
  merge-tools   Merge Tools
  pager         Pager Support
  rust          Rust in Mercurial
 
 Concepts:
 
  bundlespec    Bundle File Formats
  evolution     Safely rewriting history (EXPERIMENTAL)
  glossary      Glossary
  phases        Working with Phases
  subrepos      Subrepositories
 
 Miscellaneous:
 
  deprecated    Deprecated Features
  internals     Technical implementation topics
  scripting     Using Mercurial from scripts and automation
 
 (use 'hg help -v' to show built-in aliases and global options)
 ```
 
 - - -
 
 ##### hg
 
 Mercurial source code management system
 
 ```
 root@kali:~# hg -h
 Mercurial Distributed SCM
 
 list of commands:
 
 Repository creation:
 
  clone         make a copy of an existing repository
  init          create a new repository in the given directory
 
 Remote repository management:
 
  incoming      show new changesets found in source
  outgoing      show changesets not found in the destination
  paths         show aliases for remote repositories
  pull          pull changes from the specified source
  push          push changes to the specified destination
  serve         start stand-alone webserver
 
 Change creation:
 
  commit        commit the specified files or all outstanding changes
 
 Change manipulation:
 
  backout       reverse effect of earlier changeset
  graft         copy changes from other branches onto the current branch
  merge         merge another revision into working directory
 
 Change organization:
 
  bookmarks     create a new bookmark or list existing bookmarks
  branch        set or show the current branch name
  branches      list repository named branches
  phase         set or show the current phase name
  tag           add one or more tags for the current or given revision
  tags          list repository tags
 
 File content management:
 
  annotate      show changeset information by line for each file
  cat           output the current or given revision of files
  copy          mark files as copied for the next commit
  diff          diff repository (or selected files)
  grep          search for a pattern in specified files
 
 Change navigation:
 
  bisect        subdivision search of changesets
  heads         show branch heads
  identify      identify the working directory or specified revision
  log           show revision history of entire repository or files
 
 Working directory management:
 
  add           add the specified files on the next commit
  addremove     add all new files, delete all missing files
  files         list tracked files
  forget        forget the specified files on the next commit
  purge         removes files not tracked by Mercurial
  remove        remove the specified files on the next commit
  rename        rename files; equivalent of copy + remove
  resolve       redo merges or set/view the merge status of files
  revert        restore files to their checkout state
  root          print the root (top) of the current working directory
  shelve        save and set aside changes from the working directory
  status        show changed files in the working directory
  summary       summarize working directory state
  unshelve      restore a shelved change to the working directory
  update        update working directory (or switch revisions)
 
 Change import/export:
 
  archive       create an unversioned archive of a repository revision
  bundle        create a bundle file
  export        dump the header and diffs for one or more changesets
  import        import an ordered set of patches
  unbundle      apply one or more bundle files
 
 Repository maintenance:
 
  manifest      output the current or given revision of the project manifest
  recover       roll back an interrupted transaction
  verify        verify the integrity of the repository
 
 Help:
 
  config        show combined config settings from all hgrc files
  help          show help for a given topic or a help overview
  version       output version and copyright information
 
 additional help topics:
 
 Mercurial identifiers:
 
  filesets      Specifying File Sets
  hgignore      Syntax for Mercurial Ignore Files
  patterns      File Name Patterns
  revisions     Specifying Revisions
  urls          URL Paths
 
 Mercurial output:
 
  color         Colorizing Outputs
  dates         Date Formats
  diffs         Diff Formats
  templating    Template Usage
 
 Mercurial configuration:
 
  config        Configuration Files
  environment   Environment Variables
  extensions    Using Additional Features
  flags         Command-line flags
  hgweb         Configuring hgweb
  merge-tools   Merge Tools
  pager         Pager Support
  rust          Rust in Mercurial
 
 Concepts:
 
  bundlespec    Bundle File Formats
  evolution     Safely rewriting history (EXPERIMENTAL)
  glossary      Glossary
  phases        Working with Phases
  subrepos      Subrepositories
 
 Miscellaneous:
 
  deprecated    Deprecated Features
  internals     Technical implementation topics
  scripting     Using Mercurial from scripts and automation
 
 (use 'hg help -v' to show built-in aliases and global options)
 ```
 
 - - -
 
 ### mercurial-common
 
  Mercurial is a fast, lightweight Source Control Management system designed
  for efficient handling of very large distributed projects.
   
  This package contains the architecture independent components of Mercurial,
  and is generally useless without the mercurial package.
 
 **Installed size:** `14.55 MB`  
 **How to install:** `sudo apt install mercurial-common`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### hg-ssh
 
 Restricted ssh login shell for Mercurial
 
 ```
 root@kali:~# man hg-ssh
 HG-SSH(8)                      Mercurial Manual                      HG-SSH(8)
 
 NAME
        hg-ssh - restricted ssh login shell for Mercurial
 
 SYNOPSIS
        hg-ssh repositories...
 
 DESCRIPTION
        hg-ssh is a wrapper for ssh access to a limited set of mercurial repos.
 
        To  be  used  in  ~/.ssh/authorized_keys with the "command" option, see
        sshd(8):   command="hg-ssh   path/to/repo1    /path/to/repo2    ~/repo3
        ~user/repo4"  ssh-dss  ...   (probably together with these other useful
        options: no-port-forwarding,no-X11-forwarding,no-agent-forwarding)
 
        This allows pull/push over ssh from/to the repositories given as  argu-
        ments.
 
        If  all your repositories are subdirectories of a common directory, you
        can allow shorter paths with:  command="cd  path/to/my/repositories  &&
        hg-ssh repo1 subdir/repo2"
 
        You  can  use  pattern matching of your normal shell, e.g.: command="cd
        repos && hg-ssh user/thomas/* projects/{mercurial,foo}"
 
        You can also add a --read-only flag to allow read-only access to a key,
        e.g.: command="hg-ssh --read-only repos/*"
 
 BUGS
        Probably lots, please post them to  the  mailing  list  (see  Resources
        below) when you find them.
 
 SEE ALSO
        hg(1)
 
 AUTHOR
        Written by Olivia Mackall <olivia@selenic.com>
 
 RESOURCES
        Main Web Site: https://mercurial-scm.org/
 
        Source code repository: https://www.mercurial-scm.org/repo/hg
 
        Mailing list: https://www.mercurial-scm.org/mailman/listinfo/mercurial/
 
 COPYING
        Copyright  (C)  2005-2016 Olivia Mackall.  Free use of this software is
        granted under the terms of the GNU General Public License version 2  or
        any later version.
 
 AUTHOR
        Thomas Arendsen Hein <thomas@intevation.de>
 
        Organization: Mercurial
 
                                                                      HG-SSH(8)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
