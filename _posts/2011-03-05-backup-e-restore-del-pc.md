---
id: 124
title: Backup e Restore del pc
author: Stefano Marzorati
layout: post
guid: http://ubbunti.wordpress.com/2011/03/05/backup-e-restore-del-pc
permalink: /backup-e-restore-del-pc/
blogger_blog:
  - ubbunti.blogspot.com
  - ubbunti.blogspot.com
  - ubbunti.blogspot.com
blogger_author:
  - m@il_of_d@y
  - m@il_of_d@y
  - m@il_of_d@y
blogger_e466c7156e8bac77e64f63e8bad92c92_permalink:
  - 8710752210464683859
  - 8710752210464683859
  - 8710752210464683859
categories:
  - Linux
tags:
  - backup
  - restore
  - ubuntu
---
**Copiamo la lista dei pacchetti installati sul nostro sistema:**

** **  
`mkdir ~/backup`  
`dpkg --get-selections > ~/backup/lista_pacchetti`  
**Copiamo i repository del nostro sistema**:  
`cat /etc/apt/sources.list /etc/apt/sources.list.d/* > ~/backup/sources.list`  
**Copiamo la cartella backup **(presente nella nostra home) **da qualche parte **(anche **una chiavetta USB andrà benissimo**) oppure, opzionalmente, copiamo ***tutta la nostra home directory ***(se abbiamo bisogno di copiare anche i nostri dati).

<span style="font-weight:bold;"><br /> </span>

<h2 style="text-align:justify;">
  Restore
</h2>

<ol style="text-align:justify;">
  <li>
    <strong>Installiamo il sistema operativo </strong>(chiaramente della stessa versione di quello sorgente) <strong>sul nostro pc di destinazione </strong>e, cosa fondamentale, <strong>colleghiamolo a internet</strong>.<strong><br /> </strong>
  </li>
  <li>
    <strong>Copiamo </strong>la cartella <strong>backup</strong>, che avevamo salvato prima, <strong>dentro la <em>nostra nuova home directory</em></strong>; oppure, se avevamo deciso di <em>copiare tutta la home</em>,<strong> copiamo </strong>(ed eventualmente sovrascriviamo<strong>) i files presenti nella home vecchia all’interno della nuova home.<br /> </strong>
  </li>
  <li>
    <strong>Copiamo </strong>il nostro <em>nuovo file <strong>sources.list </strong></em>(quello creato in precedenza) <strong>nel posto in cui deve essere sul nuovo sistema</strong>, creiamo un backup (non si sa mai) di quello vecchio e aggiorniamo la lista pacchetti, ossia
  </li>
  <blockquote>
    <p>
      <code>&lt;strong>sudo mv&lt;/strong> /etc/apt/sources.list /etc/apt/sources.list.old&lt;br />
&lt;strong>sudo cp&lt;/strong> ~/backup/sources.list /etc/apt/sources.list&lt;br />
&lt;strong>sudo apt-get update&lt;/strong></code>
    </p>
  </blockquote>
  
  <li>
    A questo punto <strong>non ci resta che ripristinare </strong>tutti i pacchetti che <strong>avevamo installato sulla nostra macchina</strong>, utilizzando il file lista_pacchetti creato in precedenza. Anche questa è <strong>un’operazione pressochè immediata</strong>, in quanto abbiamo bisogno di <strong>un solo comando da terminale</strong>, cioè<br /> <blockquote>
      <p>
        <code>&lt;strong>dpkg --set-selections&lt;/strong> &lt; ~/backup/lista_pacchetti&lt;br />
&lt;strong>sudo apt-get&lt;/strong> dselect-upgrade</code>
      </p>
    </blockquote>
  </li>
</ol>

Aspettiamo il completamento dell’operazione ed avremo terminato! Ecco qui un bel sistema operativo clonato… con meno di un’ora di lavoro (di cui circa 40 minuti servono per installare il nuovo sistema operativo)