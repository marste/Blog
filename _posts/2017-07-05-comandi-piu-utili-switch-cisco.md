---
title: Comandi più usati su Switch Cisco
date: 2017-07-05 15:00:00 +0200
author: Stefano Marzorati
layout: post
permalink: /comandi-piu-utili-switch-cisco/
categories:
  - Networks
tags:
  - switch
  - Cisco
  - comandi
  - utili
  - vlan
  - porte
  - access
  - trunk
---
**Verifica su quale porta è collegato un certo pc o device:**   
<code>ping *ipaddress*</code>   
<code>show ip arp *ipaddress*</code>   
<code>show mac address-table address *mac-address*</code>   


**Per assegnare una VLAN su una determinata porta:**   
<code>conf t</code>   
<code>interface gig1/0/x</code>   
<code>switchport access vlan 50</code>   
<code>end</code>   
<code>wr memory</code>   


**Per mettere una porta in trunk su piu VLAN:**   
<code>conf t</code>   
<code>interface gig1/0/x</code>   
<code>switchport mode trunk</code>   
<code>switchport trunk allowed vlan 1,100</code>   
<code>end</code>   
<code>wr memory</code>   


**Togliere trunk:**  
<code>conf t</code>    
<code>interface gig1/0/x</code>   
<code>switchport mode access</code>   
<code>end</code>   
<code>wr memory</code>   


**Per vedere quali porte sono in trunk e su quali VLAN:**   
<code>show interfaces trunk</code>   


**Per vedere lo stato di tutte le porte e la loro descrizione:**   
<code>show interfaces description</code>   
