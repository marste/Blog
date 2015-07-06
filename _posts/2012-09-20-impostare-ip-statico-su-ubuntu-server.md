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
	auto lo   
	iface lo inet loopback   


	auto eth0   
	iface eth0 inet static   
	address 192.168.1.2 #mettere qui l’IP desiderato   
	netmask 255.255.255.0 #la netmask della rete   
	gateway 192.168.1.1 #il gateway della rete   

poi

`sudo nano /etc/resolv.conf`

e dentro modificare come segue:

	nameserver 212.216.112.112 #dns primario della rete   
	nameserver 212.216.172.62 #dns secondario della rete   


Riavviare la rete:  
`sudo ifdown eth0 && sudo ifup eth0`
