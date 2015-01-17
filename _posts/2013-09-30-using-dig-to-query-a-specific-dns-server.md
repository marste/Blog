---
id: 2023
title: Using dig to Query a Specific DNS Server
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=2023
permalink: /using-dig-to-query-a-specific-dns-server/
publicize_twitter_user:
  - marzorati_ste
  - marzorati_ste
publicize_twitter_url:
  - http://t.co/lLU5yIolyI
  - http://t.co/lLU5yIolyI
publicize_linkedin_url:
  - 'http://www.linkedin.com/updates?discuss=&scope=114372254&stype=M&topic=5790348283582898176&type=U&a=h6yk'
  - 'http://www.linkedin.com/updates?discuss=&scope=114372254&stype=M&topic=5790348283582898176&type=U&a=h6yk'
authorsure_include_css:
  - 
dsq_thread_id:
  - 2127918713
categories:
  - Linux
  - Windows
tags:
  - dig
  - dns
  - query
  - tool
---
Esempio:  
`dig marzorati.co NS @8.8.8.8`  
Risultato:  
`; <<>> DiG 9.3.2 <<>> marzorati.co NS @8.8.8.8<br />
; (1 server found)<br />
;; global options: printcmd<br />
;; Got answer:<br />
;; ->>HEADER< ;; flags: qr rd ra; QUERY: 1, ANSWER: 2, AUTHORITY: 0,`

` ADDITIONAL: 0<br />
;; QUESTION SECTION:<br />
;marzorati.co. IN NS`

`;; ANSWER SECTION:<br />
marzorati.co. 21600 IN NS ns01.000webhost.com.<br />
marzorati.co. 21600 IN NS ns02.000webhost.com.`

`;; Query time: 125 msec<br />
;; SERVER: 8.8.8.8#53(8.8.8.8)<br />
;; WHEN: Thu Oct 17 15:25:44 2013<br />
;; MSG SIZE rcvd: 82`