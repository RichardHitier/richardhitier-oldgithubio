---
layout: post
title: "centos, grub et w8"
description: ""
category: 
tags: []
---
{% include JB/setup %}


Trop facile d'installer la Centos.

Même le service info de la boîte y participe en enregistrant
la nouvelle machine sur le réseau en un temps record.

Donc en 1/2h ç'aurait pu être bouclé.

C'eut été sans compter sur un windows qui ne boote plus
après l'installation de grub2 ...

# Recherche de Solutions


gdisk 
fdisk -l

# ntfs-3g 

- [installer ntfs-3g](http://tech.yipp.ca/linux/install-ntfs-centos-7/)
- vérifier qu'on a tout bon: `grub2-mkconfig >/dev/null | grep windows`
- mettre grub  jour : `grub2-mkconfig -o /boot/grub2/grub.cfg`


et rulez \o/

