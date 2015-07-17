---
title: How to rename a Windows Computer remotely with PowerShell
date: 2015-07-17 12:15:00 -07:00
author: Stefano Marzorati
layout: post
permalink: /how-to-rename-windows-computer-remotely-powershell/
categories:
  - Windows
tags:
  - commandline
  - rename
  - remotely
  - powershell
  - name
  - computer
  - script
---

	#Changes the name of the computer you enter.  Prompts for admin credentials- include the domain name #when you put cred in.
	#Prompts for whether or not you want to restart the renamed computer imeadiately- changes do not take effect #until restart.
	
	
	$TargetComp=Read-Host -Prompt "Enter the Name of the Computer you want to change the name of "
	$Credential=Get-Credential
	$computerName = GWMI Win32_ComputerSystem -computername $TargetComp -Authentication 6
	Write-host "Current Computer Name is " $computerName
	$name = Read-Host -Prompt "Please Enter the ComputerName you want to use."
	Write-host "New Computer Name " $Name
	$Go=Read-Host -prompt "Proceed with computer name change? (Y / N)"
	If(($Go-eq"Y")-or($Go-eq"y"))
	{
	$computername.Rename($name,$credential.GetNetworkCredential().Password,$credential.Username)
	}
	$Reboot=Read-host -Prompt "Do you want to restart the computer? (Y / N)"
	If(($Reboot-eq"Y")-or($Reboot-eq"y"))
	{
	restart-computer -computername $TargetComp -Force
	}