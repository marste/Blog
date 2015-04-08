---
title: Comandi più usati in GitHub
author: Stefano Marzorati
layout: post
permalink: /comandi-usati-comuni-github/
categories:
  - Linux
  - Windows
tags:
  - comandi
  - github
  - utili
  - comuni
  - commandline
---
![github](https://lh5.googleusercontent.com/-y3eDXI2CMns/T2U5R9nANoI/AAAAAAAAD8U/vTeJoJXlShU/s256/GithubLogo.png)   
Se dovete caricare dei nuovi files da command line su GitHub, ecco i comandi principali per uploadarli:   

`git status`   
`git add .`   
`git commit -m "Modifica effettuata"`   
`git pull`   
`git push`   
`git fetch`   

Se invece dovete eliminare dei files, i comandi da digitare saranno questi:   

`git rm $(git ls-files --deleted)`   
`git commit -m "Modifica effettuata"`   
`git push`   