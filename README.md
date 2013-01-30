s3mysqlbackup
=============
A simple bash script to dump and compress MySQL databases then store:
1. on the local filesystem, with optional rotation of old backups
2. and/or in an s3 bucket

Uses s3cmd to upload files to S3.


##Usage
```
./s3mysqlbackup - dump a MySQL server's data, compress and optionally upload to S3

Options:

  -h           - this help
  -s <host>    - mysql server to connect from.  Creds from ~/.my.cnf
  -b <bucket>  - S3 bucket to place dump in
  -o <outdir>  - local dir to store backup in
  -r <days>    - delete dumps older than N days

Example A: ./s3mysqlbackup -s mysql.mycompany.com -b target-bucket
Example B: ./s3mysqlbackup -s mysql.mycompany.com -o /var/backups/our_mysql_backups -r 14
```


##History
* Originally created by Alex Hewson (alex@payperks.com, https://github.com/alexmbird)


##License
Copyright (c) 2013, PayPerks, Inc.

This work is licensed under the Creative Commons Attribution 3.0 Unported License. To view a copy of this license, visit http://creativecommons.org/licenses/by/3.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.
