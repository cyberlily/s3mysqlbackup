s3mysqlbackup
=============
A simple bash script to dump and compress MySQL databases then store:
* on the local filesystem, with optional rotation of old backups
* and/or in an s3 bucket

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

Copyright (c) 2012, PayPerks, Inc.
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
* Neither the name of PayPerks, Inc. nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

