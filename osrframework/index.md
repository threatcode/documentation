---
Title: osrframework
Homepage: https://github.com/i3visio/osrframework
Repository: https://gitlab.com/kalilinux/packages/osrframework
Architectures: all
Version: 0.20.1-0kali2
Metapackages: kali-linux-everything kali-tools-identify 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### osrframework
 
  This package contains a set of libraries developed by i3visio to perform Open
  Source Intelligence tasks. They include references to a bunch of different
  applications related to username checking, DNS lookups, information leaks
  research, deep web search, regular expressions extraction and many others.
 
 **Installed size:** `1.73 MB`  
 **How to install:** `sudo apt install osrframework`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-bs4
 * python3-cfscrape
 * python3-colorama
 * python3-decorator
 * python3-emailahoy3
 * python3-networkx
 * python3-oauthlib
 * python3-pkg-resources
 * python3-pyexcel
 * python3-pyexcel-io
 * python3-pyexcel-ods
 * python3-pyexcel-text
 * python3-pyexcel-xls
 * python3-pyexcel-xlsx
 * python3-requests
 * python3-tabulate
 * python3-tweepy
 * python3-whois
 * python3-yaml
 {{< /spoiler >}}
 
 ##### alias_generator
 
 
 ```
 root@kali:~# alias_generator -h
 usage: alias_generator [-n <NAME>] [-s1 <SURNAME_1>] [-s2 <SURNAME_2>]
                        [-c <CITY>] [-C <COUNTRY>] [-y <YEAR>]
                        [-o <path_to_output_file>] [--numbers] [--common-words]
                        [--leet] [--locales]
                        [--extra-words EXTRA_WORDS [EXTRA_WORDS ...]] [-h]
                        [--version]
 
 alias_generator is a tool that tries to create possible aliases based on the
 inputs known from a person.
 
 options:
   -n <NAME>, --name <NAME>
                         Name of the person.
   -s1 <SURNAME_1>, --surname1 <SURNAME_1>
                         First surname.
   -s2 <SURNAME_2>, --surname2 <SURNAME_2>
                         Second surname.
   -c <CITY>, --city <CITY>
                         A city linked to the profile.
   -C <COUNTRY>, --country <COUNTRY>
                         A country.
   -y <YEAR>, --year <YEAR>
                         Birth year.
   -o <path_to_output_file>, --output-file <path_to_output_file>
                         Path to the output file.
 
 Profile squatting arguments:
   Showing additional configuration options for this program based on the
   original -s option in usufy.py.
 
   --numbers             Adds numbers at the end of the nicknames.
   --common-words        Adds some famous words at the end of the nicknames.
   --leet                Adds the leet mode to change 'a' by '4', 'e' by '3',
                         etc.
   --locales             Adds ending linked to countries.
   --extra-words EXTRA_WORDS [EXTRA_WORDS ...]
                         Adds new words to the nicknames provided by the user.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 ```
 
 - - -
 
 ##### alias_generator.py
 
 
 ```
 root@kali:~# alias_generator.py -h
 usage: alias_generator [-n <NAME>] [-s1 <SURNAME_1>] [-s2 <SURNAME_2>]
                        [-c <CITY>] [-C <COUNTRY>] [-y <YEAR>]
                        [-o <path_to_output_file>] [--numbers] [--common-words]
                        [--leet] [--locales]
                        [--extra-words EXTRA_WORDS [EXTRA_WORDS ...]] [-h]
                        [--version]
 
 alias_generator is a tool that tries to create possible aliases based on the
 inputs known from a person.
 
 options:
   -n <NAME>, --name <NAME>
                         Name of the person.
   -s1 <SURNAME_1>, --surname1 <SURNAME_1>
                         First surname.
   -s2 <SURNAME_2>, --surname2 <SURNAME_2>
                         Second surname.
   -c <CITY>, --city <CITY>
                         A city linked to the profile.
   -C <COUNTRY>, --country <COUNTRY>
                         A country.
   -y <YEAR>, --year <YEAR>
                         Birth year.
   -o <path_to_output_file>, --output-file <path_to_output_file>
                         Path to the output file.
 
 Profile squatting arguments:
   Showing additional configuration options for this program based on the
   original -s option in usufy.py.
 
   --numbers             Adds numbers at the end of the nicknames.
   --common-words        Adds some famous words at the end of the nicknames.
   --leet                Adds the leet mode to change 'a' by '4', 'e' by '3',
                         etc.
   --locales             Adds ending linked to countries.
   --extra-words EXTRA_WORDS [EXTRA_WORDS ...]
                         Adds new words to the nicknames provided by the user.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 ```
 
 - - -
 
 ##### checkfy
 
 
 ```
 root@kali:~# checkfy -h
 usage: checkfy (--license | -n <nicks> [<nicks> ...] | -N <nicks_file>) -m
                <pattern> [-o <path_to_output_folder>] [-t <type>] [--quiet]
                [-h] [--version]
 
 checkfy - Finding potential email addresses based on a list of known aliases
 (either provided as arguments or read from a file) and a known pattern.
 Default values can be io
 
 Input options (one required):
   --license             shows the GPLv3+ license and exists.
   -n <nicks> [<nicks> ...], --nicks <nicks> [<nicks> ...]
                         the list of nicks to be checked in the domains
                         selected.
   -N <nicks_file>, --nicks_file <nicks_file>
                         the file with the list of nicks to be checked in the
                         domains selected.
   -m <pattern>, --email-pattern <pattern>
                         The email pattern that the generated email address
                         SHOULD match. The pattern type can be configured using
                         `--type`.
 
 Other options:
   Configuring other options.
 
   -o <path_to_output_folder>, --output_folder <path_to_output_folder>
                         output folder for the generated files. Default: ./.
   -t <type>, --type <type>
                         The type of pattern provided. It can be either the
                         style used by Twitter to show the pattern suggestions
                         or a regular expression. Default: twitter.
   --quiet               tells the program not to show anything.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### checkfy.py
 
 
 ```
 root@kali:~# checkfy.py -h
 usage: checkfy (--license | -n <nicks> [<nicks> ...] | -N <nicks_file>) -m
                <pattern> [-o <path_to_output_folder>] [-t <type>] [--quiet]
                [-h] [--version]
 
 checkfy - Finding potential email addresses based on a list of known aliases
 (either provided as arguments or read from a file) and a known pattern.
 Default values can be io
 
 Input options (one required):
   --license             shows the GPLv3+ license and exists.
   -n <nicks> [<nicks> ...], --nicks <nicks> [<nicks> ...]
                         the list of nicks to be checked in the domains
                         selected.
   -N <nicks_file>, --nicks_file <nicks_file>
                         the file with the list of nicks to be checked in the
                         domains selected.
   -m <pattern>, --email-pattern <pattern>
                         The email pattern that the generated email address
                         SHOULD match. The pattern type can be configured using
                         `--type`.
 
 Other options:
   Configuring other options.
 
   -o <path_to_output_folder>, --output_folder <path_to_output_folder>
                         output folder for the generated files. Default: ./.
   -t <type>, --type <type>
                         The type of pattern provided. It can be either the
                         style used by Twitter to show the pattern suggestions
                         or a regular expression. Default: twitter.
   --quiet               tells the program not to show anything.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### domainfy
 
 
 ```
 root@kali:~# domainfy -h
 usage: domainfy (-n <nicks> [<nicks> ...] | -N <nicks_file> | --license)
                 [-e <sum_ext> [<sum_ext> ...]] [-o <path_to_output_folder>]
                 [-t <tld_type> [<tld_type> ...]]
                 [-u <new_tld> [<new_tld> ...]] [-x <domain> [<domain> ...]]
                 [-F <alternative_header_file>] [-T <num_threads>] [--quiet]
                 [--whois] [-h] [--version]
 
 domainfy - Checking the existence of domains that resolev to an IP address.
 
 Input options (one required):
   -n <nicks> [<nicks> ...], --nicks <nicks> [<nicks> ...]
                         the list of nicks to be checked in the domains
                         selected.
   -N <nicks_file>, --nicks_file <nicks_file>
                         the file with the list of nicks to be checked in the
                         domains selected.
   --license             shows the GPLv3+ license and exists.
 
 Processing arguments:
   Configuring the way in which mailfy will process the identified profiles.
 
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -o <path_to_output_folder>, --output-folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy.py will try to create;
                         if this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -t <tld_type> [<tld_type> ...], --tlds <tld_type> [<tld_type> ...]
                         list of TLD types where the nick will be looked for.
   -u <new_tld> [<new_tld> ...], --user-defined <new_tld> [<new_tld> ...]
                         additional TLD that will be searched.
   -x <domain> [<domain> ...], --exclude <domain> [<domain> ...]
                         select the domains to be avoided. The format should
                         include the initial '.'.
   -F <alternative_header_file>, --file-header <alternative_header_file>
                         header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>.
   -T <num_threads>, --threads <num_threads>
                         write down the number of threads to be used (default
                         16). If 0, the maximum number possible will be used,
                         which may make the system feel unstable.
   --quiet               tells the program not to show anything.
   --whois               tells the program to launch whois queries.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### domainfy.py
 
 
 ```
 root@kali:~# domainfy.py -h
 usage: domainfy (-n <nicks> [<nicks> ...] | -N <nicks_file> | --license)
                 [-e <sum_ext> [<sum_ext> ...]] [-o <path_to_output_folder>]
                 [-t <tld_type> [<tld_type> ...]]
                 [-u <new_tld> [<new_tld> ...]] [-x <domain> [<domain> ...]]
                 [-F <alternative_header_file>] [-T <num_threads>] [--quiet]
                 [--whois] [-h] [--version]
 
 domainfy - Checking the existence of domains that resolev to an IP address.
 
 Input options (one required):
   -n <nicks> [<nicks> ...], --nicks <nicks> [<nicks> ...]
                         the list of nicks to be checked in the domains
                         selected.
   -N <nicks_file>, --nicks_file <nicks_file>
                         the file with the list of nicks to be checked in the
                         domains selected.
   --license             shows the GPLv3+ license and exists.
 
 Processing arguments:
   Configuring the way in which mailfy will process the identified profiles.
 
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -o <path_to_output_folder>, --output-folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy.py will try to create;
                         if this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -t <tld_type> [<tld_type> ...], --tlds <tld_type> [<tld_type> ...]
                         list of TLD types where the nick will be looked for.
   -u <new_tld> [<new_tld> ...], --user-defined <new_tld> [<new_tld> ...]
                         additional TLD that will be searched.
   -x <domain> [<domain> ...], --exclude <domain> [<domain> ...]
                         select the domains to be avoided. The format should
                         include the initial '.'.
   -F <alternative_header_file>, --file-header <alternative_header_file>
                         header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>.
   -T <num_threads>, --threads <num_threads>
                         write down the number of threads to be used (default
                         16). If 0, the maximum number possible will be used,
                         which may make the system feel unstable.
   --quiet               tells the program not to show anything.
   --whois               tells the program to launch whois queries.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### mailfy
 
 
 ```
 root@kali:~# mailfy -h
 usage: mailfy
               (--license | -m <emails> [<emails> ...] | -M <emails_file> | -n <nicks> [<nicks> ...] | -N <nicks_file> | --create-emails <nicks_file>)
               [-e <sum_ext> [<sum_ext> ...]]
               [-d <candidate_domains> [<candidate_domains> ...]]
               [-o <path_to_output_folder>] [-p <platform> [<platform> ...]]
               [-x <domain> [<domain> ...]] [-F <alternative_header_file>]
               [-T <num_threads>] [--quiet] [-h] [--version]
 
 mailfy - Checking the existence of a given mail.
 
 Input options (one required):
   --license             shows the GPLv3+ license and exists.
   -m <emails> [<emails> ...], --emails <emails> [<emails> ...]
                         the list of emails to be checked.
   -M <emails_file>, --emails-file <emails_file>
                         the file with the list of emails.
   -n <nicks> [<nicks> ...], --nicks <nicks> [<nicks> ...]
                         the list of nicks to be checked in the domains
                         selected.
   -N <nicks_file>, --nicks-file <nicks_file>
                         the file with the list of nicks to be checked in the
                         domains selected.
   --create-emails <nicks_file>
                         the file with the list of nicks to be created in the
                         domains selected.
 
 Processing arguments:
   Configuring the way in which mailfy will process the identified profiles.
 
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -d <candidate_domains> [<candidate_domains> ...], --domains <candidate_domains> [<candidate_domains> ...]
                         list of domains where the nick will be looked for.
   -o <path_to_output_folder>, --output-folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy.py will try to create;
                         if this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -p <platform> [<platform> ...], --platforms <platform> [<platform> ...]
                         select the platforms where you want to perform the
                         search amongst the following: ['all', 'infojobs',
                         'instagram', 'keyserverio', 'twitter', 'youtube'].
                         More than one option can be selected.
   -x <domain> [<domain> ...], --exclude <domain> [<domain> ...]
                         select the domains to be excluded from the search.
   -F <alternative_header_file>, --file-header <alternative_header_file>
                         Header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>.
   -T <num_threads>, --threads <num_threads>
                         write down the number of threads to be used (default
                         16). If 0, the maximum number possible will be used,
                         which may make the system feel unstable.
   --quiet               tells the program not to show anything.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### mailfy.py
 
 
 ```
 root@kali:~# mailfy.py -h
 usage: mailfy
               (--license | -m <emails> [<emails> ...] | -M <emails_file> | -n <nicks> [<nicks> ...] | -N <nicks_file> | --create-emails <nicks_file>)
               [-e <sum_ext> [<sum_ext> ...]]
               [-d <candidate_domains> [<candidate_domains> ...]]
               [-o <path_to_output_folder>] [-p <platform> [<platform> ...]]
               [-x <domain> [<domain> ...]] [-F <alternative_header_file>]
               [-T <num_threads>] [--quiet] [-h] [--version]
 
 mailfy - Checking the existence of a given mail.
 
 Input options (one required):
   --license             shows the GPLv3+ license and exists.
   -m <emails> [<emails> ...], --emails <emails> [<emails> ...]
                         the list of emails to be checked.
   -M <emails_file>, --emails-file <emails_file>
                         the file with the list of emails.
   -n <nicks> [<nicks> ...], --nicks <nicks> [<nicks> ...]
                         the list of nicks to be checked in the domains
                         selected.
   -N <nicks_file>, --nicks-file <nicks_file>
                         the file with the list of nicks to be checked in the
                         domains selected.
   --create-emails <nicks_file>
                         the file with the list of nicks to be created in the
                         domains selected.
 
 Processing arguments:
   Configuring the way in which mailfy will process the identified profiles.
 
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -d <candidate_domains> [<candidate_domains> ...], --domains <candidate_domains> [<candidate_domains> ...]
                         list of domains where the nick will be looked for.
   -o <path_to_output_folder>, --output-folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy.py will try to create;
                         if this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -p <platform> [<platform> ...], --platforms <platform> [<platform> ...]
                         select the platforms where you want to perform the
                         search amongst the following: ['all', 'infojobs',
                         'instagram', 'keyserverio', 'twitter', 'youtube'].
                         More than one option can be selected.
   -x <domain> [<domain> ...], --exclude <domain> [<domain> ...]
                         select the domains to be excluded from the search.
   -F <alternative_header_file>, --file-header <alternative_header_file>
                         Header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>.
   -T <num_threads>, --threads <num_threads>
                         write down the number of threads to be used (default
                         16). If 0, the maximum number possible will be used,
                         which may make the system feel unstable.
   --quiet               tells the program not to show anything.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### osrf
 
 
 ```
 root@kali:~# osrf -h
 usage: osrf [-h] [--license] [--version]
             <sub_command> <sub_command_options> ...
 
 OSRFramework CLI. Collection of tools included in the framework.
 
 SUBCOMMANDS:
   List of available commands that can be invoked using OSRFramework CLI.
 
   <sub_command> <sub_command_options>
     alias_generator     Generates a list of candidate usernames based on known
                         information.
     checkfy             Verifies if a given email address matches a pattern.
     domainfy            Checks whether domain names using words and nicknames
                         are available.
     mailfy              Gets information about email accounts.
     phonefy             Looks for information linked to spam practices by a
                         phone number.
     searchfy            Performs queries on several platforms.
     usufy               Looks for registered accounts with given nicknames.
 
 ABOUT ARGUMENTS:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --license             shows the AGPLv3+ license and exists.
   --version             shows the version of the program and exists.
 
 Use 'osrf <command> --help' to learn more about each command. Check
 OSRFramework README.md file for further details on the usage of this program
 or follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### osrframework-cli
 
 
 ```
 root@kali:~# osrframework-cli -h
 usage: osrf [-h] [--license] [--version]
             <sub_command> <sub_command_options> ...
 
 OSRFramework CLI. Collection of tools included in the framework.
 
 SUBCOMMANDS:
   List of available commands that can be invoked using OSRFramework CLI.
 
   <sub_command> <sub_command_options>
     alias_generator     Generates a list of candidate usernames based on known
                         information.
     checkfy             Verifies if a given email address matches a pattern.
     domainfy            Checks whether domain names using words and nicknames
                         are available.
     mailfy              Gets information about email accounts.
     phonefy             Looks for information linked to spam practices by a
                         phone number.
     searchfy            Performs queries on several platforms.
     usufy               Looks for registered accounts with given nicknames.
 
 ABOUT ARGUMENTS:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --license             shows the AGPLv3+ license and exists.
   --version             shows the version of the program and exists.
 
 Use 'osrf <command> --help' to learn more about each command. Check
 OSRFramework README.md file for further details on the usage of this program
 or follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### phonefy
 
 
 ```
 root@kali:~# phonefy -h
 usage: phonefy (--license | -n <phones> [<phones> ...])
                [-e <sum_ext> [<sum_ext> ...]] [-o <path_to_output_folder>]
                [-p <platform> [<platform> ...]] [-F <alternative_header_file>]
                [--quiet] [-w] [-x <platform> [<platform> ...]] [-h]
                [--version]
 
 phonefy - Piece of software that checks the existence of a given series of
 phones in a bunch of phone number lists associated to malicious activities.
 
 Input options (one required):
   --license             shows the GPLv3+ license and exists.
   -n <phones> [<phones> ...], --numbers <phones> [<phones> ...]
                         the list of phones to process (at least one is
                         required).
 
 Processing arguments:
   Configuring the way in which usufy will process the identified profiles.
 
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -o <path_to_output_folder>, --output_folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy.py will try to create;
                         if this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -p <platform> [<platform> ...], --platforms <platform> [<platform> ...]
                         select the platforms where you want to perform the
                         search amongst the following: ['all',
                         'infotelefonica', 'listaspam', 'xtelefonos']. More
                         than one option can be selected.
   -F <alternative_header_file>, --file_header <alternative_header_file>
                         Header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>.
   --quiet               tells the program not to show anything.
   -w, --web_browser     opening the URIs returned in the default web browser.
   -x <platform> [<platform> ...], --exclude <platform> [<platform> ...]
                         select the platforms that you want to exclude from the
                         processing.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### phonefy.py
 
 
 ```
 root@kali:~# phonefy.py -h
 usage: phonefy (--license | -n <phones> [<phones> ...])
                [-e <sum_ext> [<sum_ext> ...]] [-o <path_to_output_folder>]
                [-p <platform> [<platform> ...]] [-F <alternative_header_file>]
                [--quiet] [-w] [-x <platform> [<platform> ...]] [-h]
                [--version]
 
 phonefy - Piece of software that checks the existence of a given series of
 phones in a bunch of phone number lists associated to malicious activities.
 
 Input options (one required):
   --license             shows the GPLv3+ license and exists.
   -n <phones> [<phones> ...], --numbers <phones> [<phones> ...]
                         the list of phones to process (at least one is
                         required).
 
 Processing arguments:
   Configuring the way in which usufy will process the identified profiles.
 
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -o <path_to_output_folder>, --output_folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy.py will try to create;
                         if this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -p <platform> [<platform> ...], --platforms <platform> [<platform> ...]
                         select the platforms where you want to perform the
                         search amongst the following: ['all',
                         'infotelefonica', 'listaspam', 'xtelefonos']. More
                         than one option can be selected.
   -F <alternative_header_file>, --file_header <alternative_header_file>
                         Header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>.
   --quiet               tells the program not to show anything.
   -w, --web_browser     opening the URIs returned in the default web browser.
   -x <platform> [<platform> ...], --exclude <platform> [<platform> ...]
                         select the platforms that you want to exclude from the
                         processing.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### searchfy
 
 
 ```
 root@kali:~# searchfy -h
 usage: searchfy (--license | -q <searches> [<searches> ...])
                 [-e <sum_ext> [<sum_ext> ...]] [-F <alternative_header_file>]
                 [-o <path_to_output_folder>] [-p <platform> [<platform> ...]]
                 [-w] [-x <platform> [<platform> ...]] [-h] [--version]
 
 searchfy - Piece of software that performs a query on the platforms in
 OSRFramework.
 
 Input options (one required):
   --license             shows the GPLv3+ license and exists.
   -q <searches> [<searches> ...], --queries <searches> [<searches> ...]
                         the list of queries to be performed).
 
 Processing arguments:
   Configuring the way in which searchfy will process the identified
   profiles.
 
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -F <alternative_header_file>, --file_header <alternative_header_file>
                         Header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>
   -o <path_to_output_folder>, --output_folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy.py will try to create;
                         if this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -p <platform> [<platform> ...], --platforms <platform> [<platform> ...]
                         select the platforms where you want to perform the
                         search amongst the following: ['all', 'facebook',
                         'github', 'instagram', 'keyserverio', 'twitter',
                         'youtube']. More than one option can be selected.
   -w, --web_browser     opening the URIs returned in the default web browser.
   -x <platform> [<platform> ...], --exclude <platform> [<platform> ...]
                         select the platforms that you want to exclude from the
                         processing.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### searchfy.py
 
 
 ```
 root@kali:~# searchfy.py -h
 usage: searchfy (--license | -q <searches> [<searches> ...])
                 [-e <sum_ext> [<sum_ext> ...]] [-F <alternative_header_file>]
                 [-o <path_to_output_folder>] [-p <platform> [<platform> ...]]
                 [-w] [-x <platform> [<platform> ...]] [-h] [--version]
 
 searchfy - Piece of software that performs a query on the platforms in
 OSRFramework.
 
 Input options (one required):
   --license             shows the GPLv3+ license and exists.
   -q <searches> [<searches> ...], --queries <searches> [<searches> ...]
                         the list of queries to be performed).
 
 Processing arguments:
   Configuring the way in which searchfy will process the identified
   profiles.
 
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -F <alternative_header_file>, --file_header <alternative_header_file>
                         Header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>
   -o <path_to_output_folder>, --output_folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy.py will try to create;
                         if this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -p <platform> [<platform> ...], --platforms <platform> [<platform> ...]
                         select the platforms where you want to perform the
                         search amongst the following: ['all', 'facebook',
                         'github', 'instagram', 'keyserverio', 'twitter',
                         'youtube']. More than one option can be selected.
   -w, --web_browser     opening the URIs returned in the default web browser.
   -x <platform> [<platform> ...], --exclude <platform> [<platform> ...]
                         select the platforms that you want to exclude from the
                         processing.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   --version             shows the version of the program and exists.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### usufy
 
 
 ```
 root@kali:~# usufy -h
 usage: usufy
              (--info <action> | -b | -f <path_to_fuzzing_list> | -l <path_to_nick_list> | -n <nick> [<nick> ...] | --show_tags)
              [-p <platform> [<platform> ...]] [-t <tag> [<tag> ...]]
              [-x <platform> [<platform> ...]] [--avoid_download]
              [--avoid_processing] [--fuzz_config <path_to_fuzz_list>]
              [--nonvalid <not_valid_characters>]
              [-e <sum_ext> [<sum_ext> ...]] [-L <path_to_log_folder]
              [-o <path_to_output_folder>] [-w] [-F <alternative_header_file>]
              [-T <num_threads>] [-h] [-v <verbosity>] [--version]
 
 usufy - Piece of software that checks the existence of a profile for a given
 user in dozens of different platforms.
 
 Input options (one required):
   --info <action>       select the action to be performed amongst the
                         following: list_platforms (list the details of the
                         selected platforms), list_tags (list the tags of the
                         selected platforms). Afterwards, it exists.
   -b, --benchmark       perform the benchmarking tasks.
   -f <path_to_fuzzing_list>, --fuzz <path_to_fuzzing_list>
                         this option will try to find usufy-like URLs. The list
                         of fuzzing platforms in the file should be (one per
                         line): <BASE_DOMAIN> <VALID_NICK>
   -l <path_to_nick_list>, --list <path_to_nick_list>
                         path to the file where the list of nicks to verify is
                         stored (one per line).
   -n <nick> [<nick> ...], --nicks <nick> [<nick> ...]
                         the list of nicks to process (at least one is
                         required).
   --show_tags           it will show the platforms grouped by tags.
 
 Platform selection arguments:
   Criteria for selecting the platforms where performing the search.
 
   -p <platform> [<platform> ...], --platforms <platform> [<platform> ...]
                         select the platforms where you want to perform the
                         search amongst the following: ['all', '500px',
                         'about', 'affilorama', 'archive', 'arduino', 'ariva',
                         'armorgames', 'askfm', 'audiob', 'audioboom',
                         'authorstream', 'badoo', 'bandcamp', 'bennugd',
                         'betblog', 'bitbacker', 'bitbucket', 'bitcointalk',
                         'bitrated', 'blip', 'blogmarks', 'blogspot', 'boonex',
                         'bubok', 'bucketlistly', 'buddypic', 'burbuja.info',
                         'canva', 'carbonmade', 'cartodb', 'causes', 'ccm',
                         'ccsinfo', 'chess', 'cockos', 'codecademy',
                         'codementor', 'coderwall', 'colourlovers',
                         'connectingsingles', 'couchsurfing', 'crokes',
                         'crowdin', 'cryptocompare', 'cryptofresh',
                         'dailymotion', 'datpiff', 'deviantart', 'digitalspy',
                         'disqus', 'doodle', 'douban', 'dreamstime',
                         'dribbble', 'drupal', 'dzone', 'ebay', 'echatta',
                         'eightbitme', 'ello', 'emoneyspace', 'enfemenino',
                         'ethereum', 'etsy', 'eyeem', 'facebook', 'fanpop',
                         'fark', 'fiverr', 'flickr', 'forocoches', 'foros24h',
                         'forosperu', 'forospyware', 'foursquare',
                         'freelancer', 'freerepublic', 'getsatisfaction',
                         'github', 'goblinrefuge', 'goodreads', 'gravatar',
                         'gsmspain', 'houzz', 'htcmania', 'hubpages',
                         'ibosocial', 'ifunny', 'instagram', 'instructables',
                         'issuu', 'ivoox', 'jamiiforums', 'kali', 'kanogames',
                         'keybase', 'kickstarter', 'kinja', 'kongregate',
                         'kupika', 'lastfm', 'livejournal', 'losviajeros',
                         'mastodonsocial', 'mastodonxyz', 'mcneel',
                         'mediavida', 'medium', 'memrise', 'meneame',
                         'mercadolibre', 'metacafe', 'meteor', 'minds',
                         'mozilla', 'mstdnjp', 'musicasacra', 'myeloma',
                         'myfitnesspal', 'myspace', 'nairaland', 'netvibes',
                         'newgrounds', 'notabug', 'occupywallst', 'ok',
                         'okcupid', 'onename', 'openbugbounty',
                         'openframeworks', 'openstreetmap', 'papaly',
                         'pastebin', 'patreon', 'pawoo', 'pearltrees',
                         'periscope', 'phishtank', 'photobucket', 'pixinsight',
                         'pixls', 'pjrc', 'pokerred', 'pokerstrategy',
                         'pornhub', 'rankia', 'reddit', 'redtube',
                         'researchgate', 'reverbnation', 'ripenear',
                         'rojadirecta', 'ruby', 'sarahah', 'scribd',
                         'seatwish', 'sencha', 'sidereel', 'singletrackworld',
                         'slashdot', 'slideshare', 'smartcitizen', 'smugmug',
                         'soundcloud', 'soup', 'spaniards', 'spoj', 'spotify',
                         'spreaker', 'steamcommunity', 'steemit', 'steinberg',
                         'taringa', 'teamtreehouse', 'telegram', 'thesims',
                         'thestudentroom', 'theverge', 'thiscrush',
                         'tippin_me', 'trakt', 'twitter', 'twoplustwo',
                         'typepad', 'unsplash', 'v7n', 'venmo', 'verbling',
                         'vexforum', 'viddler', 'videohelp', 'vimeo',
                         'virustotal', 'vk', 'warriorforum', 'wattpad',
                         'webtv', 'wikia', 'wikipedia_ar', 'wikipedia_ca',
                         'wikipedia_de', 'wikipedia_en', 'wikipedia_es',
                         'wikipedia_eu', 'wikipedia_fr', 'wikipedia_pt',
                         'wikipedia_ru', 'winamp', 'wishlistr', 'witty',
                         'wykop', 'xing', 'xtube', 'youtube', 'zentyal',
                         'zotero']. More than one option can be selected.
   -t <tag> [<tag> ...], --tags <tag> [<tag> ...]
                         select the list of tags that fit the platforms in
                         which you want to perform the search. More than one
                         option can be selected.
   -x <platform> [<platform> ...], --exclude <platform> [<platform> ...]
                         select the platforms that you want to exclude from the
                         processing.
 
 Processing arguments:
   Configuring the way in which usufy will process the identified profiles.
 
   --avoid_download      argument to force usufy NOT to store the downloadable
                         version of the profiles.
   --avoid_processing    argument to force usufy NOT to perform any processing
                         task with the valid profiles.
   --fuzz_config <path_to_fuzz_list>
                         path to the fuzzing config details. Wildcards such as
                         the domains or the nicknames should come as: <DOMAIN>,
                         <USERNAME>.
   --nonvalid <not_valid_characters>
                         string containing the characters considered as not
                         valid for nicknames.
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -L <path_to_log_folder, --logfolder <path_to_log_folder
                         path to the log folder. If none was provided, ./logs
                         is assumed.
   -o <path_to_output_folder>, --output_folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy will try to create; if
                         this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -w, --web_browser     opening the uris returned in the default web browser.
   -F <alternative_header_file>, --file_header <alternative_header_file>
                         Header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>.
   -T <num_threads>, --threads <num_threads>
                         write down the number of threads to be used (default
                         32). If 0, the maximum number possible will be used,
                         which may make the system feel unstable.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   -v <verbosity>, --verbose <verbosity>
                         select the verbosity level: 0 - minimal; 1 - normal
                         (default); 2 - debug.
   --version             shows the version of the program and exits.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
 ##### usufy.py
 
 
 ```
 root@kali:~# usufy.py -h
 usage: usufy
              (--info <action> | -b | -f <path_to_fuzzing_list> | -l <path_to_nick_list> | -n <nick> [<nick> ...] | --show_tags)
              [-p <platform> [<platform> ...]] [-t <tag> [<tag> ...]]
              [-x <platform> [<platform> ...]] [--avoid_download]
              [--avoid_processing] [--fuzz_config <path_to_fuzz_list>]
              [--nonvalid <not_valid_characters>]
              [-e <sum_ext> [<sum_ext> ...]] [-L <path_to_log_folder]
              [-o <path_to_output_folder>] [-w] [-F <alternative_header_file>]
              [-T <num_threads>] [-h] [-v <verbosity>] [--version]
 
 usufy - Piece of software that checks the existence of a profile for a given
 user in dozens of different platforms.
 
 Input options (one required):
   --info <action>       select the action to be performed amongst the
                         following: list_platforms (list the details of the
                         selected platforms), list_tags (list the tags of the
                         selected platforms). Afterwards, it exists.
   -b, --benchmark       perform the benchmarking tasks.
   -f <path_to_fuzzing_list>, --fuzz <path_to_fuzzing_list>
                         this option will try to find usufy-like URLs. The list
                         of fuzzing platforms in the file should be (one per
                         line): <BASE_DOMAIN> <VALID_NICK>
   -l <path_to_nick_list>, --list <path_to_nick_list>
                         path to the file where the list of nicks to verify is
                         stored (one per line).
   -n <nick> [<nick> ...], --nicks <nick> [<nick> ...]
                         the list of nicks to process (at least one is
                         required).
   --show_tags           it will show the platforms grouped by tags.
 
 Platform selection arguments:
   Criteria for selecting the platforms where performing the search.
 
   -p <platform> [<platform> ...], --platforms <platform> [<platform> ...]
                         select the platforms where you want to perform the
                         search amongst the following: ['all', '500px',
                         'about', 'affilorama', 'archive', 'arduino', 'ariva',
                         'armorgames', 'askfm', 'audiob', 'audioboom',
                         'authorstream', 'badoo', 'bandcamp', 'bennugd',
                         'betblog', 'bitbacker', 'bitbucket', 'bitcointalk',
                         'bitrated', 'blip', 'blogmarks', 'blogspot', 'boonex',
                         'bubok', 'bucketlistly', 'buddypic', 'burbuja.info',
                         'canva', 'carbonmade', 'cartodb', 'causes', 'ccm',
                         'ccsinfo', 'chess', 'cockos', 'codecademy',
                         'codementor', 'coderwall', 'colourlovers',
                         'connectingsingles', 'couchsurfing', 'crokes',
                         'crowdin', 'cryptocompare', 'cryptofresh',
                         'dailymotion', 'datpiff', 'deviantart', 'digitalspy',
                         'disqus', 'doodle', 'douban', 'dreamstime',
                         'dribbble', 'drupal', 'dzone', 'ebay', 'echatta',
                         'eightbitme', 'ello', 'emoneyspace', 'enfemenino',
                         'ethereum', 'etsy', 'eyeem', 'facebook', 'fanpop',
                         'fark', 'fiverr', 'flickr', 'forocoches', 'foros24h',
                         'forosperu', 'forospyware', 'foursquare',
                         'freelancer', 'freerepublic', 'getsatisfaction',
                         'github', 'goblinrefuge', 'goodreads', 'gravatar',
                         'gsmspain', 'houzz', 'htcmania', 'hubpages',
                         'ibosocial', 'ifunny', 'instagram', 'instructables',
                         'issuu', 'ivoox', 'jamiiforums', 'kali', 'kanogames',
                         'keybase', 'kickstarter', 'kinja', 'kongregate',
                         'kupika', 'lastfm', 'livejournal', 'losviajeros',
                         'mastodonsocial', 'mastodonxyz', 'mcneel',
                         'mediavida', 'medium', 'memrise', 'meneame',
                         'mercadolibre', 'metacafe', 'meteor', 'minds',
                         'mozilla', 'mstdnjp', 'musicasacra', 'myeloma',
                         'myfitnesspal', 'myspace', 'nairaland', 'netvibes',
                         'newgrounds', 'notabug', 'occupywallst', 'ok',
                         'okcupid', 'onename', 'openbugbounty',
                         'openframeworks', 'openstreetmap', 'papaly',
                         'pastebin', 'patreon', 'pawoo', 'pearltrees',
                         'periscope', 'phishtank', 'photobucket', 'pixinsight',
                         'pixls', 'pjrc', 'pokerred', 'pokerstrategy',
                         'pornhub', 'rankia', 'reddit', 'redtube',
                         'researchgate', 'reverbnation', 'ripenear',
                         'rojadirecta', 'ruby', 'sarahah', 'scribd',
                         'seatwish', 'sencha', 'sidereel', 'singletrackworld',
                         'slashdot', 'slideshare', 'smartcitizen', 'smugmug',
                         'soundcloud', 'soup', 'spaniards', 'spoj', 'spotify',
                         'spreaker', 'steamcommunity', 'steemit', 'steinberg',
                         'taringa', 'teamtreehouse', 'telegram', 'thesims',
                         'thestudentroom', 'theverge', 'thiscrush',
                         'tippin_me', 'trakt', 'twitter', 'twoplustwo',
                         'typepad', 'unsplash', 'v7n', 'venmo', 'verbling',
                         'vexforum', 'viddler', 'videohelp', 'vimeo',
                         'virustotal', 'vk', 'warriorforum', 'wattpad',
                         'webtv', 'wikia', 'wikipedia_ar', 'wikipedia_ca',
                         'wikipedia_de', 'wikipedia_en', 'wikipedia_es',
                         'wikipedia_eu', 'wikipedia_fr', 'wikipedia_pt',
                         'wikipedia_ru', 'winamp', 'wishlistr', 'witty',
                         'wykop', 'xing', 'xtube', 'youtube', 'zentyal',
                         'zotero']. More than one option can be selected.
   -t <tag> [<tag> ...], --tags <tag> [<tag> ...]
                         select the list of tags that fit the platforms in
                         which you want to perform the search. More than one
                         option can be selected.
   -x <platform> [<platform> ...], --exclude <platform> [<platform> ...]
                         select the platforms that you want to exclude from the
                         processing.
 
 Processing arguments:
   Configuring the way in which usufy will process the identified profiles.
 
   --avoid_download      argument to force usufy NOT to store the downloadable
                         version of the profiles.
   --avoid_processing    argument to force usufy NOT to perform any processing
                         task with the valid profiles.
   --fuzz_config <path_to_fuzz_list>
                         path to the fuzzing config details. Wildcards such as
                         the domains or the nicknames should come as: <DOMAIN>,
                         <USERNAME>.
   --nonvalid <not_valid_characters>
                         string containing the characters considered as not
                         valid for nicknames.
   -e <sum_ext> [<sum_ext> ...], --extension <sum_ext> [<sum_ext> ...]
                         output extension for the summary files. Default: xls.
   -L <path_to_log_folder, --logfolder <path_to_log_folder
                         path to the log folder. If none was provided, ./logs
                         is assumed.
   -o <path_to_output_folder>, --output_folder <path_to_output_folder>
                         output folder for the generated documents. While if
                         the paths does not exist, usufy will try to create; if
                         this argument is not provided, usufy will NOT write
                         any down any data. Check permissions if something goes
                         wrong.
   -w, --web_browser     opening the uris returned in the default web browser.
   -F <alternative_header_file>, --file_header <alternative_header_file>
                         Header for the output filenames to be generated. If
                         None was provided the following will be used:
                         profiles.<extension>.
   -T <num_threads>, --threads <num_threads>
                         write down the number of threads to be used (default
                         32). If 0, the maximum number possible will be used,
                         which may make the system feel unstable.
 
 About arguments:
   Showing additional information about this program.
 
   -h, --help            shows this help and exists.
   -v <verbosity>, --verbose <verbosity>
                         select the verbosity level: 0 - minimal; 1 - normal
                         (default); 2 - debug.
   --version             shows the version of the program and exits.
 
 Check the README.md file for further details on the usage of this program or
 follow us on Twitter in <http://twitter.com/i3visio>.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## osrframework Usage Examples

Check for the `-n kalilinux` username across all available services:

```
root@kali:~# usufy.py -n kalilinux

  ___  ____  ____  _____                                            _
 / _ \/ ___||  _ \|  ___| __ __ _ _ __ ___   _____      _____  _ __| | __
| | | \___ \| |_) | |_ | '__/ _` | '_ ` _ \ / _ \ \ /\ / / _ \| '__| |/ /
| |_| |___) |  _ <|  _|| | | (_| | | | | | |  __/\ V  V / (_) | |  |   <
 \___/|____/|_| \_\_|  |_|  \__,_|_| |_| |_|\___| \_/\_/ \___/|_|  |_|\_

                Version:      OSRFramework 0.17.2
                Created by:   Felix Brezo and Yaiza Rubio, (i3visio)



usufy.py Copyright (C) F. Brezo and Y. Rubio (i3visio) 2014-2017

This program comes with ABSOLUTELY NO WARRANTY. This is free software, and you
are welcome to redistribute it under certain conditions. For additional info,
visit https://www.gnu.org/licenses/agpl-3.0.txt

2017-10-05 11:20:10.448178  Starting search in 297 platform(s)... Relax!

    Press <Ctrl + C> to stop...

[!] In skype.py, exception caught when checking information in Skype!

2017-10-05 11:20:30.854308  A summary of the results obtained are shown in the following table:

Sheet Name: Profiles recovered (2017-10-5_11h20m).
+-----------------------------------------------------------------+---------------+-------------------+
|                           i3visio_uri                           | i3visio_alias | i3visio_platform  |
+=================================================================+===============+===================+
| https://www.facebook.com/kalilinux                              | kalilinux     | Facebook          |
+-----------------------------------------------------------------+---------------+-------------------+
| http://twitter.com/kalilinux                                    | kalilinux     | Twitter           |
+-----------------------------------------------------------------+---------------+-------------------+
[...]
```

Search for a given email address.

```
root@kali:~# mailfy.py -n ltorvalds

  ___  ____  ____  _____                                            _
 / _ \/ ___||  _ \|  ___| __ __ _ _ __ ___   _____      _____  _ __| | __
| | | \___ \| |_) | |_ | '__/ _` | '_ ` _ \ / _ \ \ /\ / / _ \| '__| |/ /
| |_| |___) |  _ <|  _|| | | (_| | | | | | |  __/\ V  V / (_) | |  |   <
 \___/|____/|_| \_\_|  |_|  \__,_|_| |_| |_|\___| \_/\_/ \___/|_|  |_|\_

                Version:      OSRFramework 0.17.2
                Created by:   Felix Brezo and Yaiza Rubio, (i3visio)


mailfy.py Copyright (C) F. Brezo and Y. Rubio (i3visio) 2016-2017

This program comes with ABSOLUTELY NO WARRANTY. This is free software, and you
are welcome to redistribute it under certain conditions. For additional info,
visit https://www.gnu.org/licenses/agpl-3.0.txt

2017-10-05 11:32:49.178753  Starting search in 22 different emails:
[
  "ltorvalds@000.com",
  "ltorvalds@111.com",
  "ltorvalds@000.cn",
[...]
```

Search for a given string across all OSRF services.

```
root@kali:~$ searchfy.py -q "dookie2000ca"

  ___  ____  ____  _____                                            _
 / _ \/ ___||  _ \|  ___| __ __ _ _ __ ___   _____      _____  _ __| | __
| | | \___ \| |_) | |_ | '__/ _` | '_ ` _ \ / _ \ \ /\ / / _ \| '__| |/ /
| |_| |___) |  _ <|  _|| | | (_| | | | | | |  __/\ V  V / (_) | |  |   <
 \___/|____/|_| \_\_|  |_|  \__,_|_| |_| |_|\___| \_/\_/ \___/|_|  |_|\_

                Version:      OSRFramework 0.17.2
                Created by:   Felix Brezo and Yaiza Rubio, (i3visio)



searchfy.py Copyright (C) F. Brezo and Y. Rubio (i3visio) 2014-2017

This program comes with ABSOLUTELY NO WARRANTY. This is free software, and you
are welcome to redistribute it under certain conditions. For additional info,
visit https://www.gnu.org/licenses/agpl-3.0.txt

2017-10-05 11:38:33.545680  Starting search in different platform(s)... Relax!

    Press <Ctrl + C> to stop...

[!] In skype.py, exception caught when checking information in Skype!

2017-10-05 11:38:36.672623  A summary of the results obtained are listed in the following table:

Sheet Name: Profiles recovered (2017-10-5_11h38m).
+---------------------------------+---------------+------------------+
|           i3visio_uri           | i3visio_alias | i3visio_platform |
+=================================+===============+==================+
| http://github.com/dookie2000ca  | dookie2000ca  | Github           |
+---------------------------------+---------------+------------------+
| http://twitter.com/dookie2000ca | dookie2000ca  | Twitter          |
+---------------------------------+---------------+------------------+

2017-10-05 11:38:36.685354  You can find all the information collected in the following files:
    ./profiles.csv

2017-10-05 11:38:36.685581  Finishing execution...

Total time used:    0:00:03.139901
Average seconds/query:  3.139901 seconds

Did something go wrong? Is a platform reporting false positives? Do you need to
integrate a new one and you don't know how to start? Then, you can always place
an issue in the Github project:
    https://github.com/i3visio/osrframework/issues
Note that otherwise, we won't know about it!
```
