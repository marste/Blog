---
id: 2526
title: Aggiornare phpBB e migrare dati su nuovo server
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=2526
permalink: /aggiornare-phpbb-migrare-dati-server/
authorsure_include_css:
  - 
layout_key:
  - 
post_slider_check_key:
  - 0
dsq_thread_id:
  - 2000710336
categories:
  - Linux
  - Windows
tags:
  - aggiornare
  - install
  - migrare
  - phpbb
---
Ipotizziamo di avere la versione 3.0.8 di phpBB su un server.  
Vorremmo installare l&#8217;ultima versione 3.0.12 di phpBB su un nuovo server.  
Come posso migrare?  
Ecco quali sono i passi principali:

1) Fai un backup del database  
2) Installa l&#8217;ultima versione di phpBB 3.0.12 e configuralo come se fosse la prima installazione.  
3) Importa il database backuppato in precedenza sovrascrivendo quello dell&#8217;installazione nuova.  
4) Lancia l&#8217;url `../install/database_update.php` &#8211; in questo modo aggiornerà il database  
5) Rinomina la directory &#8220;**install**&#8221;  
6) Copiare dal vecchio server al nuovo server tutta la directory "**images**", "**files**" e **store**.

Fine
