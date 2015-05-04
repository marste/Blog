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

``TIMESTAMP=$(date +"%F")   
BACKUP_DIR="/home/backup/$TIMESTAMP"   
MYSQL_USER="root"   
MYSQL_PASSWORD="password"   
MYSQL=/usr/bin/mysql   
MYSQLDUMP=/usr/bin/mysqldump   
mkdir -p $BACKUP_DIR   
databases=`$MYSQL -u$MYSQL_USER -p$MYSQL_PASSWORD -e "SHOW DATABASES;" | grep -Ev "(Database|information_schema|mysql|performance_schema)"`   
for db in $databases; do   
echo $db   
$MYSQLDUMP --force --opt --user=$MYSQL_USER -p$MYSQL_PASSWORD --databases $db | gzip > "$BACKUP_DIR/$db.gz"   
done``