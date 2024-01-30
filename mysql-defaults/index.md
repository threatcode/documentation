---
Title: mysql-defaults
Homepage: 
Repository: https://salsa.debian.org/mariadb-team/mysql/-/tree/mysql-defaults/debian/master
Architectures: any all
Version: 1.1.0
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-labs kali-linux-large kali-linux-nethunter kali-tools-exploitation kali-tools-forensics kali-tools-information-gathering kali-tools-passwords kali-tools-respond kali-tools-social-engineering kali-tools-top10 kali-tools-vulnerability kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### default-libmysqlclient-dev
 
  MySQL is a fast, stable and true multi-user, multi-threaded SQL database
  server. SQL (Structured Query Language) is the most popular database query
  language in the world. The main goals of MySQL are speed, robustness and
  ease of use.
   
  This package depends on the default implementation of the client development
  libraries and header files (API and ABI defined by MySQL). Depending on the
  default defined through this metapackage, the underlying implementation may be
  provided by either MySQL or MariaDB. Build-Depend on this package and then
  link using -lmysqlclient. You will end up with a binary that depends on either
  libmysqlclient.so.X or libmariadbclient.so.X depending on the current default.
  dpkg-shlibdeps should correctly generate a dependency on libmysqlclientX or
  libmariadbclientX as appropriate.
 
 **Installed size:** `9 KB`  
 **How to install:** `sudo apt install default-libmysqlclient-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libmariadb-dev-compat
 {{< /spoiler >}}
 
 
 - - -
 
 ### default-libmysqld-dev
 
  MySQL is a fast, stable and true multi-user, multi-threaded SQL database
  server. SQL (Structured Query Language) is the most popular database query
  language in the world. The main goals of MySQL are speed, robustness and
  ease of use.
   
  This package depends on the default implementation of the embedded server
  library development and header files.
 
 **Installed size:** `9 KB`  
 **How to install:** `sudo apt install default-libmysqld-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libmariadbd-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### default-mysql-client
 
  MySQL is a fast, stable and true multi-user, multi-threaded SQL database
  server. SQL (Structured Query Language) is the most popular database query
  language in the world. The main goals of MySQL are speed, robustness and
  ease of use.
   
  This package depends on the default implementation of the client binaries and
  the additional tools innotop and mysqlreport.
 
 **Installed size:** `9 KB`  
 **How to install:** `sudo apt install default-mysql-client`  
 
 {{< spoiler "Dependencies:" >}}
 * mariadb-client
 {{< /spoiler >}}
 
 
 - - -
 
 ### default-mysql-client-core
 
  MySQL is a fast, stable and true multi-user, multi-threaded SQL database
  server. SQL (Structured Query Language) is the most popular database query
  language in the world. The main goals of MySQL are speed, robustness and
  ease of use.
   
  This package depends on the default implementation of the core client files,
  as used by Akonadi.
 
 **Installed size:** `9 KB`  
 **How to install:** `sudo apt install default-mysql-client-core`  
 
 {{< spoiler "Dependencies:" >}}
 * mariadb-client-core
 {{< /spoiler >}}
 
 
 - - -
 
 ### default-mysql-server
 
  MySQL is a fast, stable and true multi-user, multi-threaded SQL database
  server. SQL (Structured Query Language) is the most popular database query
  language in the world. The main goals of MySQL are speed, robustness and
  ease of use.
   
  This package depends on the default implementation of all the infrastructure
  needed to setup system databases.
 
 **Installed size:** `9 KB`  
 **How to install:** `sudo apt install default-mysql-server`  
 
 {{< spoiler "Dependencies:" >}}
 * mariadb-server
 {{< /spoiler >}}
 
 
 - - -
 
 ### default-mysql-server-core
 
  MySQL is a fast, stable and true multi-user, multi-threaded SQL database
  server. SQL (Structured Query Language) is the most popular database query
  language in the world. The main goals of MySQL are speed, robustness and
  ease of use.
   
  This package depends on the default implementation of the server binaries but
  doesn't depend on all the infrastructure needed to setup system databases.
 
 **Installed size:** `9 KB`  
 **How to install:** `sudo apt install default-mysql-server-core`  
 
 {{< spoiler "Dependencies:" >}}
 * mariadb-server-core
 {{< /spoiler >}}
 
 
 - - -
 
 ### mysql-common
 
  MySQL is a fast, stable and true multi-user, multi-threaded SQL database
  server. SQL (Structured Query Language) is the most popular database query
  language in the world. The main goals of MySQL are speed, robustness and
  ease of use.
   
  This package includes files needed by all versions of the client library,
  e.g. /etc/mysql/my.cnf.
 
 **Installed size:** `33 KB`  
 **How to install:** `sudo apt install mysql-common`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
