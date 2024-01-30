---
Title: rake
Homepage: https://github.com/ruby/rake
Repository: https://salsa.debian.org/ruby-team/rake
Architectures: all
Version: 13.0.6-3
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-exploitation kali-tools-identify kali-tools-information-gathering kali-tools-passwords kali-tools-post-exploitation kali-tools-reporting kali-tools-reverse-engineering kali-tools-social-engineering kali-tools-top10 kali-tools-vulnerability kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rake
 
  Rake is a simple ruby build program with capabilities similar to make.
   
  Rake has the following features:
    * Rakefiles (rakes version of Makefiles) are completely defined in
      standard Ruby syntax. No XML files to edit. No quirky Makefile
      syntax to worry about (is that a tab or a space?)
    * Users can specify tasks with prerequisites.
    * Rake supports rule patterns to sythesize implicit tasks.
    * Rake is lightweight. It can be distributed with other
      projects as a single file. Projects that depend upon
      rake do not require that rake be installed on target
      systems.
 
 **Installed size:** `272 KB`  
 **How to install:** `sudo apt install rake`  
 
 {{< spoiler "Dependencies:" >}}
 * ruby
 {{< /spoiler >}}
 
 ##### rake
 
 Make-like build utility for Ruby
 
 ```
 root@kali:~# rake -h
 rake [-f rakefile] {options} targets...
 
 Options are ...
         --backtrace=[OUT]            Enable full backtrace.  OUT can be stderr (default) or stdout.
         --comments                   Show commented tasks only
         --job-stats [LEVEL]          Display job statistics. LEVEL=history displays a complete job list
         --rules                      Trace the rules resolution.
         --suppress-backtrace PATTERN Suppress backtrace lines matching regexp PATTERN. Ignored if --trace is on.
     -A, --all                        Show all tasks, even uncommented ones (in combination with -T or -D)
     -B, --build-all                  Build all prerequisites, including those which are up-to-date.
     -C, --directory [DIRECTORY]      Change to DIRECTORY before doing anything.
     -D, --describe [PATTERN]         Describe the tasks (matching optional PATTERN), then exit.
     -e, --execute CODE               Execute some Ruby code and exit.
     -E, --execute-continue CODE      Execute some Ruby code, then continue with normal task processing.
     -f, --rakefile [FILENAME]        Use FILENAME as the rakefile to search for.
     -G, --no-system, --nosystem      Use standard project Rakefile search paths, ignore system wide rakefiles.
     -g, --system                     Using system wide (global) rakefiles (usually '~/.rake/*.rake').
     -I, --libdir LIBDIR              Include LIBDIR in the search path for required modules.
     -j, --jobs [NUMBER]              Specifies the maximum number of tasks to execute in parallel. (default is number of CPU cores + 4)
     -m, --multitask                  Treat all tasks as multitasks.
     -n, --dry-run                    Do a dry run without executing actions.
     -N, --no-search, --nosearch      Do not search parent directories for the Rakefile.
     -P, --prereqs                    Display the tasks and dependencies, then exit.
     -p, --execute-print CODE         Execute some Ruby code, print the result, then exit.
     -q, --quiet                      Do not log messages to standard output.
     -r, --require MODULE             Require MODULE before executing rakefile.
     -R, --rakelibdir RAKELIBDIR,     Auto-import any .rake files in RAKELIBDIR. (default is 'rakelib')
         --rakelib
     -s, --silent                     Like --quiet, but also suppresses the 'in directory' announcement.
     -t, --trace=[OUT]                Turn on invoke/execute tracing, enable full backtrace. OUT can be stderr (default) or stdout.
     -T, --tasks [PATTERN]            Display the tasks (matching optional PATTERN) with descriptions, then exit. -AT combination displays all of tasks contained no description.
     -v, --verbose                    Log message to standard output.
     -V, --version                    Display the program version.
     -W, --where [PATTERN]            Describe the tasks (matching optional PATTERN), then exit.
     -X, --no-deprecation-warnings    Disable the deprecation warnings.
     -h, -H, --help                   Display this help message.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
