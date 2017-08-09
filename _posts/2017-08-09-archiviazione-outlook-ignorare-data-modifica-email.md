---
title: Archiviazione Outlook, ignorare data di modifica delle email 
date: 2017-08-09 12:50:00 +0200
author: Stefano Marzorati
layout: post
permalink: /archiviazione-outlook-ignorare-data-modifica-email/
categories:
  - Windows
tags:
  - microsoft
  - outlook
  - archive
  - archiviazione
  - modifica
  - data
  - email
---
Per Outlook 2013 creare un valore DWORD con valore **1** e nominarlo **ArchiveIgnoreLastModifiedTime** all'interno della chiave:   
	
	HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Outlook\Preferences

	DWORD Value: ArchiveIgnoreLastModifiedTime
	
	Value data: 1

Per altre versioni di outlook la chiave è la stessa, basta sostituire il numero della versione con quella effettivamente installata:   

Outlook 2016   
	HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Outlook\Preferences
	
Outlook 2010   
	HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Outlook\Preferences
	
Outlook 2007   
	HKEY_CURRENT_USER\Software\Microsoft\Office\12.0\Outlook\Preferences 


Dopo aver creato e configurarto il valore del Registro di sistema **ArchiveIgnoreLastModifiedTime**, Outlook archivierà gli elementi nel seguente modo:   

I messaggi di posta elettronica vengono archiviate in base alla data di ricezione.
