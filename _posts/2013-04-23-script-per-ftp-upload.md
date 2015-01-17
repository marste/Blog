---
id: 1538
title: Script per FTP upload
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=1538
permalink: /script-per-ftp-upload/
publicize_reach:
  - 'a:2:{s:7:"twitter";a:1:{i:3411;i:29;}s:2:"wp";a:1:{i:0;i:1;}}'
  - 'a:2:{s:7:"twitter";a:1:{i:3411;i:29;}s:2:"wp";a:1:{i:0;i:1;}}'
publicize_twitter_user:
  - marzorati_ste
  - marzorati_ste
authorsure_include_css:
  - 
dsq_thread_id:
  - 1919572222
categories:
  - Linux
---
`<br />
#!/bin/sh<br />
USERNAME="tmp"<br />
PASSWORD="tmp"<br />
SERVER="192.168.101.8"</p>
<p># local directory to pickup *.tar.gz file<br />
LOCALDIR="/var/backups/snapshots"</p>
<p># remote server directory to upload backup<br />
BACKUPDIR="/prova"</p>
<p># login to remote server<br />
ftp -n -i $SERVER <<EOF<br />
user $USERNAME $PASSWORD<br />
cd $BACKUPDIR<br />
lcd $LOCALDIR<br />
mput *.tar.gz<br />
quit<br />
EOF<br />
`