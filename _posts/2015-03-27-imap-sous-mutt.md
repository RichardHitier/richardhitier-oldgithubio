---
layout: post
title: "Mutt et Imap"
description: ""
category: localhost 
categories: [changes, tools]
---
{% include JB/setup %}

C'est décidé, je repasse à mutt. 

Mais cette fois ci, fini, ni MDA ni MTA, on oublie: Ce sera tout en imap/INBOX !

    set spoolfile="imaps://{user}:{pass}@ssl0.ovh.net/Inbox"
    set folder="imaps://ssl0.ovh.net/Inbox"


Je lis bien la Inbox, mais rhaa, qu'il est lent l'animal !!!

Et pas de thread_sort pour l'instant ...

Et impossible de poster à travers le smtp d'ovh  !!!!!

RHAAAA. c'est pas près.
