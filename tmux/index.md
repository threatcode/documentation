---
Title: tmux
Homepage: https://tmux.github.io/
Repository: https://salsa.debian.org/rfrancoise/tmux
Architectures: any
Version: 3.3a-5
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-802-11 kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tmux
 
  tmux enables a number of terminals (or windows) to be accessed and
  controlled from a single terminal like screen. tmux runs as a
  server-client system. A server is created automatically when necessary
  and holds a number of sessions, each of which may have a number of
  windows linked to it. Any number of clients may connect to a session,
  or the server may be controlled by issuing commands with tmux.
  Communication takes place through a socket, by default placed in /tmp.
  Moreover tmux provides a consistent and well-documented command
  interface, with the same syntax whether used interactively, as a key
  binding, or from the shell. It offers a choice of vim or Emacs key
  layouts.
 
 **Installed size:** `1.08 MB`  
 **How to install:** `sudo apt install tmux`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libevent-core-2.1-7 
 * libtinfo6 
 * libutempter0 
 {{< /spoiler >}}
 
 ##### tmux
 
 Terminal multiplexer
 
 ```
 root@kali:~# tmux -h
 tmux: unknown option -- h
 usage: tmux [-2CDlNuvV] [-c shell-command] [-f file] [-L socket-name]
             [-S socket-path] [-T features] [command [flags]]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
