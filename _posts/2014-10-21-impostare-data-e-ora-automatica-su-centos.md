---
id: 3135
title: Impostare data e ora automatica su CentOS
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=3135
permalink: /impostare-data-e-ora-automatica-su-centos/
authorsure_include_css:
  - 
dsq_thread_id:
  - 3139838255
categories:
  - Linux
tags:
  - centos
  - data
  - impostare
  - ntp
  - ora
  - setup
---
Installa il servizio ntp:  
`yum install ntp`

Edita il file:  
`/etc/ntp/step-tickers`

Aggiungendo i servers ntp che vuoi, ad esempio:

`0.pool.ntp.org<br />
1.pool.ntp.org<br />
2.pool.ntp.org`

Fai in modo che il servizio si avvii automaticamente al boot:

`chkconfig ntpd on`

Avvia il servizio:  
`service ntpd start`

Controlla la data e l&#8217;ora:  
`date`