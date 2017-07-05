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
**Verifica Porta collegata Cisco:**   
ping *ipaddress*   
show ip arp *ipaddress*   
show mac address-table address *mac-address*   


**Per cambiare VLAN su Cisco:**   
conf t   
interface gig1/0/x   
switchport access vlan 50   
end   
wr memory   


**Per mettere una porta in trunk su piu VLAN:**   
conf t   
interface gig1/0/x   
switchport mode trunk   
switchport trunk allowed vlan 1,100   
end   
wr memory   


**Togliere trunk:**  
conf t    
interface gig1/0/x   
switchport mode access   
end   
wr memory   


**Per vedere quali porte sono in trunk e su quali VLAN:**   
show interfaces trunk   
