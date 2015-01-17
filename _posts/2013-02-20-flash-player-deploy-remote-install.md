---
id: 1432
title: Flash Player Deploy
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=1432
permalink: /flash-player-deploy-remote-install/
publicize_reach:
  - 'a:2:{s:7:"twitter";a:1:{i:3411;i:24;}s:2:"wp";a:1:{i:0;i:1;}}'
  - 'a:2:{s:7:"twitter";a:1:{i:3411;i:24;}s:2:"wp";a:1:{i:0;i:1;}}'
publicize_twitter_user:
  - marzorati_ste
  - marzorati_ste
authorsure_include_css:
  - 
dsq_thread_id:
  - 2096205692
categories:
  - Windows
tags:
  - deploy
  - flash
  - install
  - player
  - remote
---
`xcopy "\ServerSoftwareWindowsUtilityFlash Playerinstall_flash_player_11_active_x.exe" "\%1C$Temp" /r/i/c/h/k/e<br />
sleep 3<br />
pskill iexplore.exe \%1<br />
psexec.exe \%1 -s "C:Tempinstall_flash_player_11_active_x.exe" /install`

<a href="http://www.adobe.com/products/flashplayer/distribution3.html" target="_blank">http://www.adobe.com/products/flashplayer/distribution3.html</a>