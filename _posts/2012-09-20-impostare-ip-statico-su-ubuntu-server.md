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
`sudo /etc/init.d/networking restart`