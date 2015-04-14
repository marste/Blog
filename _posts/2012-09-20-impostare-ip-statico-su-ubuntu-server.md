---
id: 1208
title: Impostare IP statico su Ubuntu Server
author: Stefano Marzorati
layout: post
guid: http://ubbunti.wordpress.com/?p=1208
permalink: /impostare-ip-statico-su-ubuntu-server/
authorsure_include_css:
  - 
dsq_thread_id:
  - 1906743003
categories:
  - Linux
---
`sudo nano /etc/network/interfaces`

e dentro modificare come segue:  
`auto lo<br />
iface lo inet loopback<br />
`

`auto eth0<br />
iface eth0 inet static<br />
address 192.168.1.2 #mettere qui l’IP desiderato<br />
netmask 255.255.255.0 #la netmask della rete<br />
gateway 192.168.1.1 #il gateway della rete<br />
`

poi

`sudo nano /etc/resolv.conf`

e dentro modificare come segue:

`nameserver 212.216.112.112 #dns primario della rete<br />
nameserver 212.216.172.62 #dns secondario della rete<br />
`

Riavviare la rete:  
`sudo ifdown eth0 && sudo ifup eth0`

<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-2779664131593194"
     data-ad-slot="2588551865"
     data-ad-format="auto"></ins>
<script>
(adsbygoogle = window.adsbygoogle || []).push({});
</script>
