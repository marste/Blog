---
id: 2707
title: Script per ascoltare radio con mplayer
author: Stefano Marzorati
layout: post
guid: http://marzorati.co/?p=2707
permalink: /script-per-ascoltare-radio-con-mplayer/
dsq_thread_id:
  - 2170313924
categories:
  - Windows
tags:
  - listen
  - mplayer
  - radio
  - script
  - Windows
---
`@ECHO OFF<br />
CLS<br />
:LOOP<br />
ECHO 1) Radio Planet<br />
ECHO 2) Radio DeeJay<br />
ECHO 3) Radio 24<br />
ECHO 4) Smoothjazz.com<br />
ECHO 5) Venus Radio Mykonos<br />
ECHO 6) m2o<br />
ECHO 7) Hardcoreradio.nl<br />
ECHO 8) Hot Mix Radio 80<br />
ECHO 9) Radio Party Groove<br />
ECHO 10) Razor FM<br />
ECHO 11) Radio 538 IBIZA<br />
ECHO 12) PulsRadio 80<br />
ECHO 13) ----------<br />
ECHO 14) SKY.FM 80<br />
ECHO 15) ----------<br />
ECHO 16) ----------<br />
ECHO 17) ----------<br />
ECHO 18) ----------<br />
ECHO 19) Classica<br />
ECHO 20) Solo Piano<br />
ECHO.<br />
ECHO e) Esci<br />
:: SET /P prompts for input and sets the variable<br />
:: to whatever the user types<br />
ECHO.<br />
SET Choice=<br />
SET /P Choice=Scegli la radio che vuoi ascoltare e premi INVIO:<br />
:: The syntax in the next line extracts the substring<br />
:: starting at 0 (the beginning) and 1 character long<br />
IF NOT '%Choice%'=='' SET Choice=%Choice:~0,2%<br />
ECHO.<br />
:: /I makes the IF comparison case-insensitive<br />
IF /I '%Choice%'=='1' GOTO Item1<br />
IF /I '%Choice%'=='2' GOTO Item2<br />
IF /I '%Choice%'=='3' GOTO Item3<br />
IF /I '%Choice%'=='4' GOTO Item4<br />
IF /I '%Choice%'=='5' GOTO Item5<br />
IF /I '%Choice%'=='6' GOTO Item6<br />
IF /I '%Choice%'=='7' GOTO Item7<br />
IF /I '%Choice%'=='8' GOTO Item8<br />
IF /I '%Choice%'=='9' GOTO Item9<br />
IF /I '%Choice%'=='10' GOTO Item10<br />
IF /I '%Choice%'=='11' GOTO Item11<br />
IF /I '%Choice%'=='12' GOTO Item12<br />
IF /I '%Choice%'=='13' GOTO Item13<br />
IF /I '%Choice%'=='14' GOTO Item14<br />
IF /I '%Choice%'=='15' GOTO Item15<br />
IF /I '%Choice%'=='16' GOTO Item16<br />
IF /I '%Choice%'=='17' GOTO Item17<br />
IF /I '%Choice%'=='18' GOTO Item18<br />
IF /I '%Choice%'=='19' GOTO Item19<br />
IF /I '%Choice%'=='20' GOTO Item20<br />
IF /I '%Choice%'=='e' GOTO End<br />
ECHO "%Choice%" Ma cosa cazzo hai scelto? Riprova va...<br />
ECHO.<br />
GOTO Loop<br />
:Item1<br />
mplayer http://91.121.104.139:8100<br />
GOTO Again<br />
:Item2<br />
mplayer http://mp3.kataweb.it:8000/RadioDeejay<br />
GOTO Again<br />
:Item3<br />
mplayer http://shoutcast.radio24.it:8000/<br />
GOTO Again<br />
:Item4<br />
mplayer http://sj128.hnux.com<br />
GOTO Again<br />
:Item5<br />
mplayer http://s7.onweb.gr:8410/<br />
GOTO Again<br />
:Item6<br />
mplayer http://mp3.kataweb.it:8000/M2O<br />
GOTO Again<br />
:Item7<br />
mplayer http://shoutcast2.hardcoreradio.nl<br />
GOTO Again<br />
:Item8<br />
mplayer http://wma.hotmixradios.net/hotmixradio80?MSWMExt=.asf<br />
GOTO Again<br />
:Item9<br />
mplayer http://stream12.top-ix.org:80/partygroove<br />
GOTO Again<br />
:Item10<br />
mplayer http://radio.razorfm.nl:443/<br />
GOTO Again<br />
:Item11<br />
mplayer http://82.201.100.9:8000/WEB19_WEB_MP3<br />
GOTO Again<br />
:Item12<br />
mplayer http://stream80.pulsradio.com:6000<br />
GOTO Again<br />
:Item13<br />
mplayer ------------<br />
GOTO Again<br />
:Item14<br />
mplayer http://pub2.sky.fm/sky_the80s_aacplus<br />
GOTO Again<br />
:Item15<br />
mplayer ------------<br />
GOTO Again<br />
:Item16<br />
mplayer ------------<br />
GOTO Again<br />
:Item17<br />
mplayer ------------<br />
GOTO Again<br />
:Item18<br />
mplayer ------------<br />
GOTO Again:<br />
:Item19<br />
mplayer http://222.122.131.58:6400<br />
GOTO Again<br />
:Item20<br />
mplayer http://stream-76.shoutcast.com:80/piano_skyfm_mp3_96kbps<br />
GOTO Again<br />
:Again<br />
PAUSE<br />
CLS<br />
GOTO Loop<br />
:End`