---
id: 1938
title: Backup tutti i databases mysql in files separati
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=1938
permalink: /backup-dbs-mysql-files-separati/
publicize_reach:
  - 'a:2:{s:7:"twitter";a:1:{i:3411;i:27;}s:2:"wp";a:1:{i:0;i:2;}}'
  - 'a:2:{s:7:"twitter";a:1:{i:3411;i:27;}s:2:"wp";a:1:{i:0;i:2;}}'
publicize_twitter_user:
  - marzorati_ste
  - marzorati_ste
authorsure_include_css:
  - 
dsq_thread_id:
  - 2046282403
categories:
  - Linux
tags:
  - backup
  - mysql
  - mysqldump
  - separati
---
`#!/bin/bash`

``TIMESTAMP=$(date +"%F")<br />
BACKUP_DIR="/home/backup/$TIMESTAMP"<br />
MYSQL_USER="root"<br />
MYSQL_PASSWORD="password"<br />
MYSQL=/usr/bin/mysql<br />
MYSQLDUMP=/usr/bin/mysqldump<br />
mkdir -p $BACKUP_DIR<br />
databases=`$MYSQL -u$MYSQL_USER -p$MYSQL_PASSWORD -e "SHOW DATABASES;" | grep -Ev "(Database|information_schema|mysql|performance_schema)"`<br />
for db in $databases; do<br />
echo $db<br />
$MYSQLDUMP --force --opt --user=$MYSQL_USER -p$MYSQL_PASSWORD --databases $db | gzip > "$BACKUP_DIR/$db.gz"<br />
done``