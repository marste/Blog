---
id: 1250
title: WordPress FORWARDED_HOST per dominio primo livello
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=1250
permalink: /wordpress-forwarded-host-reverse-proxy-per-dominio-primo-livello/
publicize_reach:
  - 'a:2:{s:7:"twitter";a:1:{i:3411;i:27;}s:2:"wp";a:1:{i:0;i:1;}}'
  - 'a:2:{s:7:"twitter";a:1:{i:3411;i:27;}s:2:"wp";a:1:{i:0;i:1;}}'
publicize_twitter_user:
  - marzorati_ste
  - marzorati_ste
authorsure_include_css:
  - 
layout_key:
  - 
post_slider_check_key:
  - 0
dsq_thread_id:
  - 1979225795
categories:
  - Linux
  - Windows
tags:
  - htaccess
---
Questa è la soluzione per quando si installa WordPress sotto un Reverse Proxy di Apache.

Aggiungere queste righe nel file **wp-config.php**

Esempio:

`$_SERVER['HTTP_HOST'] = $_SERVER['HTTP_X_FORWARDED_HOST'];   
define('WP_HOME', 'http://marzorati.co');   
define('WP_SITEURL', 'http://marzorati.co');   
$_SERVER['REQUEST_URI'] = str_replace("/marzorati", "", $_SERVER['REQUEST_URI']);`

**Modifica .htaccess per non aver problemi con i permalink**

`   
# BEGIN WordPress   
<IfModule mod_rewrite.c>   
RewriteEngine On   
RewriteBase /marzorati/   
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f   
RewriteCond %{REQUEST_FILENAME} !-d   
RewriteRule . /marzorati/index.php [L]
</IfModule>   
# END WordPress`