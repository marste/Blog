---
id: 1547
title: Cambiare indirizzo IP su CentOS
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=1547
permalink: /cambiare-indirizzo-ip-su-centos/
publicize_twitter_user:
  - marzorati_ste
  - marzorati_ste
authorsure_include_css:
  - 
dsq_thread_id:
  - 1934031114
categories:
  - Linux
---
Andare in:

`/etc/sysconfig/network-scripts`

editare il file inerente alla scheda di rete da modificare, esempio: ifcfg-eth2 (modifichi l&#8217;ip della scheda di rete eth2)

Esempio di file:

`Broadcom Corporation NetXtreme BCM5704S Gigabit Ethernet<br />
DEVICE=eth2<br />
BOOTPROTO=static<br />
HWADDR=00:14:5E:4B:57:E0<br />
ONBOOT=yes<br />
TYPE=Ethernet<br />
IPADDR=192.168.101.104<br />
NETMASK=255.255.252.0<br />
GATEWAY=192.168.101.101<br />
`
