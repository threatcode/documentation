---
Title: mongo-tools
Homepage: https://github.com/mongodb/mongo-tools
Repository: https://gitlab.com/kalilinux/packages/mongo-tools
Architectures: any
Version: 100.9.1+ds1-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### mongo-tools
 
  This package contains tools for MongDB:
   * bsondump - display BSON files in a human-readable format
   * mongoimport - Convert data from JSON, TSV or CSV and insert them
     into a collection
   * mongoexport - Write an existing collection to CSV or JSON format
   * mongodump/mongorestore - Dump MongoDB backups to disk in .BSON
     format, or restore them to a live database
   * mongostat - Monitor live MongoDB servers, replica sets, or
     sharded clusters
   * mongofiles - Read, write, delete, or update files in GridFS
 
 **Installed size:** `70.59 MB`  
 **How to install:** `sudo apt install mongo-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### bsondump
 
 
 ```
 root@kali:~# bsondump --help
 Usage:
   bsondump <options> <file>
 
 View and debug .bson files.
 
 See http://docs.mongodb.com/database-tools/bsondump/ for more information.
 
 general options:
       --help               print usage
       --version            print the tool version and exit
       --config=            path to a configuration file
 
 verbosity options:
   -v, --verbose=<level>    more detailed log output (include multiple times for
                            more verbosity, e.g. -vvvvv, or specify a numeric
                            value, e.g. --verbose=N)
       --quiet              hide all log output
 
 output options:
       --type=<type>        type of output: debug, json
       --objcheck           validate BSON during processing
       --pretty             output JSON formatted to be human-readable
       --bsonFile=          path to BSON file to dump to JSON; default is stdin
       --outFile=           path to output file to dump BSON to; default is
                            stdout
 ```
 
 - - -
 
 ##### mongodump
 
 
 ```
 root@kali:~# mongodump --help
 Usage:
   mongodump <options> <connection-string>
 
 Export the content of a running server into .bson files.
 
 Specify a database with -d and a collection with -c to only dump that database or collection.
 
 Connection strings must begin with mongodb:// or mongodb+srv://.
 
 See http://docs.mongodb.com/database-tools/mongodump/ for more information.
 
 general options:
       --help                                                print usage
       --version                                             print the tool
                                                             version and exit
       --config=                                             path to a
                                                             configuration file
 
 verbosity options:
   -v, --verbose=<level>                                     more detailed log
                                                             output (include
                                                             multiple times for
                                                             more verbosity,
                                                             e.g. -vvvvv, or
                                                             specify a numeric
                                                             value, e.g.
                                                             --verbose=N)
       --quiet                                               hide all log output
 
 connection options:
   -h, --host=<hostname>                                     mongodb host to
                                                             connect to
                                                             (setname/host1,host-
 
                                                             2 for replica sets)
       --port=<port>                                         server port (can
                                                             also use --host
                                                             hostname:port)
 
 ssl options:
       --ssl                                                 connect to a mongod
                                                             or mongos that has
                                                             ssl enabled
       --sslCAFile=<filename>                                the .pem file
                                                             containing the root
                                                             certificate chain
                                                             from the
                                                             certificate
                                                             authority
       --sslPEMKeyFile=<filename>                            the .pem file
                                                             containing the
                                                             certificate and key
       --sslPEMKeyPassword=<password>                        the password to
                                                             decrypt the
                                                             sslPEMKeyFile, if
                                                             necessary
       --sslCRLFile=<filename>                               the .pem file
                                                             containing the
                                                             certificate
                                                             revocation list
       --sslFIPSMode                                         use FIPS mode of
                                                             the installed
                                                             openssl library
       --tlsInsecure                                         bypass the
                                                             validation for
                                                             server's
                                                             certificate chain
                                                             and host name
 
 authentication options:
   -u, --username=<username>                                 username for
                                                             authentication
   -p, --password=<password>                                 password for
                                                             authentication
       --authenticationDatabase=<database-name>              database that holds
                                                             the user's
                                                             credentials
       --authenticationMechanism=<mechanism>                 authentication
                                                             mechanism to use
       --awsSessionToken=<aws-session-token>                 session token to
                                                             authenticate via
                                                             AWS IAM
 
 kerberos options:
       --gssapiServiceName=<service-name>                    service name to use
                                                             when authenticating
                                                             using
                                                             GSSAPI/Kerberos
                                                             (default: mongodb)
       --gssapiHostName=<host-name>                          hostname to use
                                                             when authenticating
                                                             using
                                                             GSSAPI/Kerberos
                                                             (default: <remote
                                                             server's address>)
 
 namespace options:
   -d, --db=<database-name>                                  database to use
   -c, --collection=<collection-name>                        collection to use
 
 uri options:
       --uri=mongodb-uri                                     mongodb uri
                                                             connection string
 
 query options:
   -q, --query=                                              query filter, as a
                                                             v2 Extended JSON
                                                             string, e.g.,
                                                             '{"x":{"$gt":1}}'
       --queryFile=                                          path to a file
                                                             containing a query
                                                             filter (v2 Extended
                                                             JSON)
       --readPreference=<string>|<json>                      specify either a
                                                             preference mode
                                                             (e.g. 'nearest') or
                                                             a preference json
                                                             object (e.g.
                                                             '{mode: "nearest",
                                                             tagSets: [{a:
                                                             "b"}],
                                                             maxStalenessSeconds-
 
                                                             : 123}')
       --forceTableScan                                      force a table scan
                                                             (do not use
                                                             $snapshot or hint
                                                             _id). Deprecated
                                                             since this is
                                                             default behavior on
                                                             WiredTiger
 
 output options:
   -o, --out=<directory-path>                                output directory,
                                                             or '-' for stdout
                                                             (default: 'dump')
       --gzip                                                compress archive or
                                                             collection output
                                                             with Gzip
       --oplog                                               use oplog for
                                                             taking a
                                                             point-in-time
                                                             snapshot
       --archive=<file-path>                                 dump as an archive
                                                             to the specified
                                                             path. If flag is
                                                             specified without a
                                                             value, archive is
                                                             written to stdout
       --dumpDbUsersAndRoles                                 dump user and role
                                                             definitions for the
                                                             specified database
       --excludeCollection=<collection-name>                 collection to
                                                             exclude from the
                                                             dump (may be
                                                             specified multiple
                                                             times to exclude
                                                             additional
                                                             collections)
       --excludeCollectionsWithPrefix=<collection-prefix>    exclude all
                                                             collections from
                                                             the dump that have
                                                             the given prefix
                                                             (may be specified
                                                             multiple times to
                                                             exclude additional
                                                             prefixes)
   -j, --numParallelCollections=                             number of
                                                             collections to dump
                                                             in parallel
       --viewsAsCollections                                  dump views as
                                                             normal collections
                                                             with their produced
                                                             data, omitting
                                                             standard collections
 ```
 
 - - -
 
 ##### mongoexport
 
 
 ```
 root@kali:~# mongoexport --help
 Usage:
   mongoexport <options> <connection-string>
 
 Export data from MongoDB in CSV or JSON format.
 
 Connection strings must begin with mongodb:// or mongodb+srv://.
 
 See http://docs.mongodb.com/database-tools/mongoexport/ for more information.
 
 general options:
       --help                                      print usage
       --version                                   print the tool version and
                                                   exit
       --config=                                   path to a configuration file
 
 verbosity options:
   -v, --verbose=<level>                           more detailed log output
                                                   (include multiple times for
                                                   more verbosity, e.g. -vvvvv,
                                                   or specify a numeric value,
                                                   e.g. --verbose=N)
       --quiet                                     hide all log output
 
 connection options:
   -h, --host=<hostname>                           mongodb host to connect to
                                                   (setname/host1,host2 for
                                                   replica sets)
       --port=<port>                               server port (can also use
                                                   --host hostname:port)
 
 ssl options:
       --ssl                                       connect to a mongod or mongos
                                                   that has ssl enabled
       --sslCAFile=<filename>                      the .pem file containing the
                                                   root certificate chain from
                                                   the certificate authority
       --sslPEMKeyFile=<filename>                  the .pem file containing the
                                                   certificate and key
       --sslPEMKeyPassword=<password>              the password to decrypt the
                                                   sslPEMKeyFile, if necessary
       --sslCRLFile=<filename>                     the .pem file containing the
                                                   certificate revocation list
       --sslFIPSMode                               use FIPS mode of the
                                                   installed openssl library
       --tlsInsecure                               bypass the validation for
                                                   server's certificate chain
                                                   and host name
 
 authentication options:
   -u, --username=<username>                       username for authentication
   -p, --password=<password>                       password for authentication
       --authenticationDatabase=<database-name>    database that holds the
                                                   user's credentials
       --authenticationMechanism=<mechanism>       authentication mechanism to
                                                   use
       --awsSessionToken=<aws-session-token>       session token to authenticate
                                                   via AWS IAM
 
 kerberos options:
       --gssapiServiceName=<service-name>          service name to use when
                                                   authenticating using
                                                   GSSAPI/Kerberos (default:
                                                   mongodb)
       --gssapiHostName=<host-name>                hostname to use when
                                                   authenticating using
                                                   GSSAPI/Kerberos (default:
                                                   <remote server's address>)
 
 namespace options:
   -d, --db=<database-name>                        database to use
   -c, --collection=<collection-name>              collection to use
 
 uri options:
       --uri=mongodb-uri                           mongodb uri connection string
 
 output options:
   -f, --fields=<field>[,<field>]*                 comma separated list of field
                                                   names (required for exporting
                                                   CSV) e.g. -f "name,age"
       --fieldFile=<filename>                      file with field names - 1 per
                                                   line
       --type=<type>                               the output format, either
                                                   json or csv
   -o, --out=<filename>                            output file; if not
                                                   specified, stdout is used
       --jsonArray                                 output to a JSON array rather
                                                   than one object per line
       --pretty                                    output JSON formatted to be
                                                   human-readable
       --noHeaderLine                              export CSV data without a
                                                   list of field names at the
                                                   first line
       --jsonFormat=<type>                         the extended JSON format to
                                                   output, either canonical or
                                                   relaxed (defaults to
                                                   'relaxed') (default: relaxed)
 
 querying options:
   -q, --query=<json>                              query filter, as a JSON
                                                   string, e.g., '{x:{$gt:1}}'
       --queryFile=<filename>                      path to a file containing a
                                                   query filter (JSON)
       --readPreference=<string>|<json>            specify either a preference
                                                   mode (e.g. 'nearest') or a
                                                   preference json object (e.g.
                                                   '{mode: "nearest", tagSets:
                                                   [{a: "b"}],
                                                   maxStalenessSeconds: 123}')
       --forceTableScan                            force a table scan (do not
                                                   use $snapshot or hint _id).
                                                   Deprecated since this is
                                                   default behavior on WiredTiger
       --skip=<count>                              number of documents to skip
       --limit=<count>                             limit the number of documents
                                                   to export
       --sort=<json>                               sort order, as a JSON string,
                                                   e.g. '{x:1}'
       --assertExists                              if specified, export fails if
                                                   the collection does not exist
 ```
 
 - - -
 
 ##### mongofiles
 
 
 ```
 root@kali:~# mongofiles --help
 Usage:
   mongofiles <options> <connection-string> <command> <filename or _id>
 
 Manipulate gridfs files using the command line.
 
 Connection strings must begin with mongodb:// or mongodb+srv://.
 
 Possible commands include:
 	list      - list all files; 'filename' is an optional prefix which listed filenames must begin with
 	search    - search all files; 'filename' is a regex which listed filenames must match
 	put       - add files with filenames specified in the supporting arguments
 	put_id    - add a file with filename 'filename' and a given '_id'
 	get       - get files with filenames specified in the supporting arguments
 	get_id    - get a file with the given '_id'
 	get_regex - get files matching the supplied 'regex'
 	delete    - delete all files with filename 'filename'
 	delete_id - delete a file with the given '_id'
 
 See http://docs.mongodb.com/database-tools/mongofiles/ for more information.
 
 general options:
       --help                                      print usage
       --version                                   print the tool version and
                                                   exit
       --config=                                   path to a configuration file
 
 verbosity options:
   -v, --verbose=<level>                           more detailed log output
                                                   (include multiple times for
                                                   more verbosity, e.g. -vvvvv,
                                                   or specify a numeric value,
                                                   e.g. --verbose=N)
       --quiet                                     hide all log output
 
 connection options:
   -h, --host=<hostname>                           mongodb host to connect to
                                                   (setname/host1,host2 for
                                                   replica sets)
       --port=<port>                               server port (can also use
                                                   --host hostname:port)
 
 ssl options:
       --ssl                                       connect to a mongod or mongos
                                                   that has ssl enabled
       --sslCAFile=<filename>                      the .pem file containing the
                                                   root certificate chain from
                                                   the certificate authority
       --sslPEMKeyFile=<filename>                  the .pem file containing the
                                                   certificate and key
       --sslPEMKeyPassword=<password>              the password to decrypt the
                                                   sslPEMKeyFile, if necessary
       --sslCRLFile=<filename>                     the .pem file containing the
                                                   certificate revocation list
       --sslFIPSMode                               use FIPS mode of the
                                                   installed openssl library
       --tlsInsecure                               bypass the validation for
                                                   server's certificate chain
                                                   and host name
 
 authentication options:
   -u, --username=<username>                       username for authentication
   -p, --password=<password>                       password for authentication
       --authenticationDatabase=<database-name>    database that holds the
                                                   user's credentials
       --authenticationMechanism=<mechanism>       authentication mechanism to
                                                   use
       --awsSessionToken=<aws-session-token>       session token to authenticate
                                                   via AWS IAM
 
 kerberos options:
       --gssapiServiceName=<service-name>          service name to use when
                                                   authenticating using
                                                   GSSAPI/Kerberos (default:
                                                   mongodb)
       --gssapiHostName=<host-name>                hostname to use when
                                                   authenticating using
                                                   GSSAPI/Kerberos (default:
                                                   <remote server's address>)
 
 uri options:
       --uri=mongodb-uri                           mongodb uri connection string
 
 storage options:
   -d, --db=<database-name>                        database to use
   -l, --local=<filename>                          local filename for put|get
   -t, --type=                                     content/MIME type for put
                                                   (optional)
   -r, --replace                                   remove other files with same
                                                   name after put
       --prefix=<prefix>                           GridFS prefix to use
       --writeConcern=<write-concern>              write concern options e.g.
                                                   --writeConcern majority,
                                                   --writeConcern '{w: 3,
                                                   wtimeout: 500, fsync: true,
                                                   j: true}'
       --regexOptions=<regex-options>              regex options used for
                                                   get_regex
 
 query options:
       --readPreference=<string>|<json>            specify either a preference
                                                   mode (e.g. 'nearest') or a
                                                   preference json object (e.g.
                                                   '{mode: "nearest", tagSets:
                                                   [{a: "b"}],
                                                   maxStalenessSeconds: 123}')
 ```
 
 - - -
 
 ##### mongoimport
 
 
 ```
 root@kali:~# mongoimport --help
 Usage:
   mongoimport <options> <connection-string> <file> 
 
 Import CSV, TSV or JSON data into MongoDB. If no file is provided, mongoimport reads from stdin.
 
 Connection strings must begin with mongodb:// or mongodb+srv://.
 
 See http://docs.mongodb.com/database-tools/mongoimport/ for more information.
 
 general options:
       --help                                      print usage
       --version                                   print the tool version and
                                                   exit
       --config=                                   path to a configuration file
 
 verbosity options:
   -v, --verbose=<level>                           more detailed log output
                                                   (include multiple times for
                                                   more verbosity, e.g. -vvvvv,
                                                   or specify a numeric value,
                                                   e.g. --verbose=N)
       --quiet                                     hide all log output
 
 connection options:
   -h, --host=<hostname>                           mongodb host to connect to
                                                   (setname/host1,host2 for
                                                   replica sets)
       --port=<port>                               server port (can also use
                                                   --host hostname:port)
 
 ssl options:
       --ssl                                       connect to a mongod or mongos
                                                   that has ssl enabled
       --sslCAFile=<filename>                      the .pem file containing the
                                                   root certificate chain from
                                                   the certificate authority
       --sslPEMKeyFile=<filename>                  the .pem file containing the
                                                   certificate and key
       --sslPEMKeyPassword=<password>              the password to decrypt the
                                                   sslPEMKeyFile, if necessary
       --sslCRLFile=<filename>                     the .pem file containing the
                                                   certificate revocation list
       --sslFIPSMode                               use FIPS mode of the
                                                   installed openssl library
       --tlsInsecure                               bypass the validation for
                                                   server's certificate chain
                                                   and host name
 
 authentication options:
   -u, --username=<username>                       username for authentication
   -p, --password=<password>                       password for authentication
       --authenticationDatabase=<database-name>    database that holds the
                                                   user's credentials
       --authenticationMechanism=<mechanism>       authentication mechanism to
                                                   use
       --awsSessionToken=<aws-session-token>       session token to authenticate
                                                   via AWS IAM
 
 kerberos options:
       --gssapiServiceName=<service-name>          service name to use when
                                                   authenticating using
                                                   GSSAPI/Kerberos (default:
                                                   mongodb)
       --gssapiHostName=<host-name>                hostname to use when
                                                   authenticating using
                                                   GSSAPI/Kerberos (default:
                                                   <remote server's address>)
 
 namespace options:
   -d, --db=<database-name>                        database to use
   -c, --collection=<collection-name>              collection to use
 
 uri options:
       --uri=mongodb-uri                           mongodb uri connection string
 
 input options:
   -f, --fields=<field>[,<field>]*                 comma separated list of
                                                   fields, e.g. -f name,age
       --fieldFile=<filename>                      file with field names - 1 per
                                                   line
       --file=<filename>                           file to import from; if not
                                                   specified, stdin is used
       --headerline                                use first line in input
                                                   source as the field list (CSV
                                                   and TSV only)
       --jsonArray                                 treat input source as a JSON
                                                   array
       --parseGrace=<grace>                        controls behavior when type
                                                   coercion fails - one of:
                                                   autoCast, skipField, skipRow,
                                                   stop (default: stop)
       --type=<type>                               input format to import: json,
                                                   csv, or tsv
       --columnsHaveTypes                          indicates that the field list
                                                   (from --fields, --fieldsFile,
                                                   or --headerline) specifies
                                                   types; They must be in the
                                                   form of
                                                   '<colName>.<type>(<arg>)'.
                                                   The type can be one of: auto,
                                                   binary, boolean, date,
                                                   date_go, date_ms,
                                                   date_oracle, decimal, double,
                                                   int32, int64, string. For
                                                   each of the date types, the
                                                   argument is a datetime layout
                                                   string. For the binary type,
                                                   the argument can be one of:
                                                   base32, base64, hex. All
                                                   other types take an empty
                                                   argument. Only valid for CSV
                                                   and TSV imports. e.g.
                                                   zipcode.string(),
                                                   thumbnail.binary(base64)
       --legacy                                    use the legacy extended JSON
                                                   format
       --useArrayIndexFields                       indicates that field names
                                                   may include array indexes
                                                   that should be used to
                                                   construct arrays during
                                                   import (e.g. foo.0,foo.1).
                                                   Indexes must start from 0 and
                                                   increase sequentially
                                                   (foo.1,foo.0 would fail).
 
 ingest options:
       --drop                                      drop collection before
                                                   inserting documents
       --ignoreBlanks                              ignore fields with empty
                                                   values in CSV and TSV
       --maintainInsertionOrder                    insert the documents in the
                                                   order of their appearance in
                                                   the input source. By default
                                                   the insertions will be
                                                   performed in an arbitrary
                                                   order. Setting this flag also
                                                   enables the behavior of
                                                   --stopOnError and restricts
                                                   NumInsertionWorkers to 1.
   -j, --numInsertionWorkers=<number>              number of insert operations
                                                   to run concurrently
       --stopOnError                               halt after encountering any
                                                   error during importing. By
                                                   default, mongoimport will
                                                   attempt to continue through
                                                   document validation and
                                                   DuplicateKey errors, but with
                                                   this option enabled, the tool
                                                   will stop instead. A small
                                                   number of documents may be
                                                   inserted after encountering
                                                   an error even with this
                                                   option enabled; use
                                                   --maintainInsertionOrder to
                                                   halt immediately after an
                                                   error
       --mode=[insert|upsert|merge|delete]         insert: insert only, skips
                                                   matching documents. upsert:
                                                   insert new documents or
                                                   replace existing documents.
                                                   merge: insert new documents
                                                   or modify existing documents.
                                                   delete: deletes matching
                                                   documents only. If upsert
                                                   fields match more than one
                                                   document, only one document
                                                   is deleted. (default: insert)
       --upsertFields=<field>[,<field>]*           comma-separated fields for
                                                   the query part when --mode is
                                                   set to upsert or merge
       --writeConcern=<write-concern-specifier>    write concern options e.g.
                                                   --writeConcern majority,
                                                   --writeConcern '{w: 3,
                                                   wtimeout: 500, fsync: true,
                                                   j: true}'
       --bypassDocumentValidation                  bypass document validation
 ```
 
 - - -
 
 ##### mongorestore
 
 
 ```
 root@kali:~# mongorestore --help
 Usage:
   mongorestore <options> <connection-string> <directory or file to restore>
 
 Restore backups generated with mongodump to a running server.
 
 Specify a database with -d to restore a single database from the target directory,
 or use -d and -c to restore a single collection from a single .bson file.
 
 Connection strings must begin with mongodb:// or mongodb+srv://.
 
 See http://docs.mongodb.com/database-tools/mongorestore/ for more information.
 
 general options:
       --help                                                print usage
       --version                                             print the tool
                                                             version and exit
       --config=                                             path to a
                                                             configuration file
 
 verbosity options:
   -v, --verbose=<level>                                     more detailed log
                                                             output (include
                                                             multiple times for
                                                             more verbosity,
                                                             e.g. -vvvvv, or
                                                             specify a numeric
                                                             value, e.g.
                                                             --verbose=N)
       --quiet                                               hide all log output
 
 connection options:
   -h, --host=<hostname>                                     mongodb host to
                                                             connect to
                                                             (setname/host1,host-
 
                                                             2 for replica sets)
       --port=<port>                                         server port (can
                                                             also use --host
                                                             hostname:port)
 
 ssl options:
       --ssl                                                 connect to a mongod
                                                             or mongos that has
                                                             ssl enabled
       --sslCAFile=<filename>                                the .pem file
                                                             containing the root
                                                             certificate chain
                                                             from the
                                                             certificate
                                                             authority
       --sslPEMKeyFile=<filename>                            the .pem file
                                                             containing the
                                                             certificate and key
       --sslPEMKeyPassword=<password>                        the password to
                                                             decrypt the
                                                             sslPEMKeyFile, if
                                                             necessary
       --sslCRLFile=<filename>                               the .pem file
                                                             containing the
                                                             certificate
                                                             revocation list
       --sslFIPSMode                                         use FIPS mode of
                                                             the installed
                                                             openssl library
       --tlsInsecure                                         bypass the
                                                             validation for
                                                             server's
                                                             certificate chain
                                                             and host name
 
 authentication options:
   -u, --username=<username>                                 username for
                                                             authentication
   -p, --password=<password>                                 password for
                                                             authentication
       --authenticationDatabase=<database-name>              database that holds
                                                             the user's
                                                             credentials
       --authenticationMechanism=<mechanism>                 authentication
                                                             mechanism to use
       --awsSessionToken=<aws-session-token>                 session token to
                                                             authenticate via
                                                             AWS IAM
 
 kerberos options:
       --gssapiServiceName=<service-name>                    service name to use
                                                             when authenticating
                                                             using
                                                             GSSAPI/Kerberos
                                                             (default: mongodb)
       --gssapiHostName=<host-name>                          hostname to use
                                                             when authenticating
                                                             using
                                                             GSSAPI/Kerberos
                                                             (default: <remote
                                                             server's address>)
 
 namespace options:
   -d, --db=<database-name>                                  database to use
   -c, --collection=<collection-name>                        collection to use
 
 uri options:
       --uri=mongodb-uri                                     mongodb uri
                                                             connection string
 
 namespace options:
       --excludeCollection=<collection-name>                 DEPRECATED;
                                                             collection to skip
                                                             over during restore
                                                             (may be specified
                                                             multiple times to
                                                             exclude additional
                                                             collections)
       --excludeCollectionsWithPrefix=<collection-prefix>    DEPRECATED;
                                                             collections to skip
                                                             over during restore
                                                             that have the given
                                                             prefix (may be
                                                             specified multiple
                                                             times to exclude
                                                             additional prefixes)
       --nsExclude=<namespace-pattern>                       exclude matching
                                                             namespaces
       --nsInclude=<namespace-pattern>                       include matching
                                                             namespaces
       --nsFrom=<namespace-pattern>                          rename matching
                                                             namespaces, must
                                                             have matching nsTo
       --nsTo=<namespace-pattern>                            rename matched
                                                             namespaces, must
                                                             have matching nsFrom
 
 input options:
       --objcheck                                            validate all
                                                             objects before
                                                             inserting
       --oplogReplay                                         replay oplog for
                                                             point-in-time
                                                             restore
       --oplogLimit=<seconds>[:ordinal]                      only include oplog
                                                             entries before the
                                                             provided Timestamp
       --oplogFile=<filename>                                oplog file to use
                                                             for replay of oplog
       --archive=<filename>                                  restore dump from
                                                             the specified
                                                             archive file.  If
                                                             flag is specified
                                                             without a value,
                                                             archive is read
                                                             from stdin
       --restoreDbUsersAndRoles                              restore user and
                                                             role definitions
                                                             for the given
                                                             database
       --dir=<directory-name>                                input directory,
                                                             use '-' for stdin
       --gzip                                                decompress gzipped
                                                             input
 
 restore options:
       --drop                                                drop each
                                                             collection before
                                                             import
       --dryRun                                              view summary
                                                             without importing
                                                             anything.
                                                             recommended with
                                                             verbosity
       --writeConcern=<write-concern>                        write concern
                                                             options e.g.
                                                             --writeConcern
                                                             majority,
                                                             --writeConcern '{w:
                                                             3, wtimeout: 500,
                                                             fsync: true, j:
                                                             true}'
       --noIndexRestore                                      don't restore
                                                             indexes
       --convertLegacyIndexes                                Removes invalid
                                                             index options and
                                                             rewrites legacy
                                                             option values (e.g.
                                                             true becomes 1).
       --noOptionsRestore                                    don't restore
                                                             collection options
       --keepIndexVersion                                    don't update index
                                                             version
       --maintainInsertionOrder                              restore the
                                                             documents in the
                                                             order of their
                                                             appearance in the
                                                             input source. By
                                                             default the
                                                             insertions will be
                                                             performed in an
                                                             arbitrary order.
                                                             Setting this flag
                                                             also enables the
                                                             behavior of
                                                             --stopOnError and
                                                             restricts
                                                             NumInsertionWorkers-
 
                                                             PerCollection to 1.
   -j, --numParallelCollections=                             number of
                                                             collections to
                                                             restore in parallel
       --numInsertionWorkersPerCollection=                   number of insert
                                                             operations to run
                                                             concurrently per
                                                             collection
       --stopOnError                                         halt after
                                                             encountering any
                                                             error during
                                                             insertion. By
                                                             default,
                                                             mongorestore will
                                                             attempt to continue
                                                             through document
                                                             validation and
                                                             DuplicateKey
                                                             errors, but with
                                                             this option
                                                             enabled, the tool
                                                             will stop instead.
                                                             A small number of
                                                             documents may be
                                                             inserted after
                                                             encountering an
                                                             error even with
                                                             this option
                                                             enabled; use
                                                             --maintainInsertion-
 
                                                             Order to halt
                                                             immediately after
                                                             an error
       --bypassDocumentValidation                            bypass document
                                                             validation
       --preserveUUID                                        preserve original
                                                             collection UUIDs
                                                             (off by default,
                                                             requires drop)
       --fixDottedHashIndex                                  when enabled, all
                                                             the hashed indexes
                                                             on dotted fields
                                                             will be created as
                                                             single field
                                                             ascending indexes
                                                             on the destination
 ```
 
 - - -
 
 ##### mongostat
 
 
 ```
 root@kali:~# mongostat --help
 Usage:
   mongostat <options> <connection-string> <polling interval in seconds>
 
 Monitor basic MongoDB server statistics.
 
 Connection strings must begin with mongodb:// or mongodb+srv://.
 
 See http://docs.mongodb.com/database-tools/mongostat/ for more information.
 
 general options:
       --help                                      print usage
       --version                                   print the tool version and
                                                   exit
       --config=                                   path to a configuration file
 
 verbosity options:
   -v, --verbose=<level>                           more detailed log output
                                                   (include multiple times for
                                                   more verbosity, e.g. -vvvvv,
                                                   or specify a numeric value,
                                                   e.g. --verbose=N)
       --quiet                                     hide all log output
 
 connection options:
   -h, --host=<hostname>                           mongodb host(s) to connect to
                                                   (use commas to delimit hosts)
       --port=<port>                               server port (can also use
                                                   --host hostname:port)
 
 ssl options:
       --ssl                                       connect to a mongod or mongos
                                                   that has ssl enabled
       --sslCAFile=<filename>                      the .pem file containing the
                                                   root certificate chain from
                                                   the certificate authority
       --sslPEMKeyFile=<filename>                  the .pem file containing the
                                                   certificate and key
       --sslPEMKeyPassword=<password>              the password to decrypt the
                                                   sslPEMKeyFile, if necessary
       --sslCRLFile=<filename>                     the .pem file containing the
                                                   certificate revocation list
       --sslFIPSMode                               use FIPS mode of the
                                                   installed openssl library
       --tlsInsecure                               bypass the validation for
                                                   server's certificate chain
                                                   and host name
 
 authentication options:
   -u, --username=<username>                       username for authentication
   -p, --password=<password>                       password for authentication
       --authenticationDatabase=<database-name>    database that holds the
                                                   user's credentials
       --authenticationMechanism=<mechanism>       authentication mechanism to
                                                   use
       --awsSessionToken=<aws-session-token>       session token to authenticate
                                                   via AWS IAM
 
 kerberos options:
       --gssapiServiceName=<service-name>          service name to use when
                                                   authenticating using
                                                   GSSAPI/Kerberos (default:
                                                   mongodb)
       --gssapiHostName=<host-name>                hostname to use when
                                                   authenticating using
                                                   GSSAPI/Kerberos (default:
                                                   <remote server's address>)
 
 uri options:
       --uri=mongodb-uri                           mongodb uri connection string
 
 stat options:
   -o=<field>[,<field>]*                           fields to show. For custom
                                                   fields, use dot-syntax to
                                                   index into serverStatus
                                                   output, and optional methods
                                                   .diff() and .rate() e.g.
                                                   metrics.record.moves.diff()
   -O=<field>[,<field>]*                           like -o, but preloaded with
                                                   default fields. Specified
                                                   fields inserted after default
                                                   output
       --humanReadable=                            print sizes and time in human
                                                   readable format (e.g. 1K 234M
                                                   2G). To use the more precise
                                                   machine readable format, use
                                                   --humanReadable=false
                                                   (default: true)
       --noheaders                                 don't output column names
   -n, --rowcount=<count>                          number of stats lines to
                                                   print (0 for indefinite)
       --discover                                  discover nodes and display
                                                   stats for all
       --http                                      use HTTP instead of raw db
                                                   connection
       --all                                       all optional fields
       --json                                      output as JSON rather than a
                                                   formatted table
       --useDeprecatedJsonKeys                     use old key names; only valid
                                                   with the json output option.
   -i, --interactive                               display stats in a
                                                   non-scrolling interface
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
