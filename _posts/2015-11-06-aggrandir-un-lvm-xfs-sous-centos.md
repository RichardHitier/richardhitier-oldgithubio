---
layout: post
title: "Aggrandir un LVM xfs sous Centos"
description: ""
category: 
tags: []
---
{% include JB/setup %}


lvm ça roxe sa maman: ça m'a pris un moment, mais 2 coups de
cuiller à pot et rulez \o/

## Déplacer la partoch W7

wais, ya du windows, et je préfère tout faire depuis ce
systéme: AOMEI, ça marche bien pour déplacer une partition
C:

ça va redémarrer (via grub) pour faire son boulot, et sans
changer le grub windows reboot sur une partition neuve.

## Aggrandir le LVM

on va rajouter une nouvelle partition /dev/sda1

voir un peu les groupes LVM

    $ sudo gvs
    VG     #PV #LV #SN Attr   VSize   VFree
    centos   2   2   0 wz--n- 10.58g    0 


et les volumes

    $ sudo lvs
    LV   VG     Attr       LSize   Pool Origin Data%  Meta%  Move Log Cpy%Sync Convert
    root centos -wi-ao---- 8.70g                                                    
    swap centos -wi-ao---- 900.00m                                                    


rajouter un volume physique au groupe logique

    sudo pvcreate /dev/sda1
    sudo vgextend centos

étendre la taille du volume logique

    sudo lvextend -l +100%FREE /dev/centos/root


redimensionner la partition, attention, petite astuce,
`resize2fs` ne  fonctionnera pas sur une partition xfs ...
donc:

    sudo xfs_growfs /dev/mapper/centos-root


et rulez \o/
vraiment rapide et facile.
