---
layout: post
title: "Set Ubuntu locale."
description: "Set Ubuntu locale by LANG, LC_*"
category: Linux
tags: [Linux]
---
{% include JB/setup %}

##Summry
Locale is used to give the software ability to adapte different regions
language which users have.  

for example:  
    Date: 07/10/2013  
    In Ameracon: July 10th, 2013(US)  
    In English: Oct 7th, 2013(UK)  

So same datas have differents transfor at differents regions.

##Locale setting in Ubuntu
Here are 12 types about locale:

* LC_CTYPE: language and symbol.
* LC_NUMERIC: number
* LC_COLLATE: compare and sort
* LC_TIME: time style
* LC_MONETARY: monetary unit
* LC_MESSAGE: messages about error ,status ,title ,marks, button, menu .etc
* LC_NAME: name style
* LC_ADDRESS: address style
* LC_TELEPHONE: telephone style
* LC_MEASUREMENT: measurement style
* LC_PAPER: default paper format(A4)
* LC_IDENTIFICATION: locale metadata

At dir __/usr/share/i18n/locale/__, you can find the all locale setting files 
which have been installed, such as zh\_CN, en\_US. In the files, you can get 
setting about 12 locale types.

##How to setting locale for zh_CN
Here are three ways for locale setting:

* LC_ALL
* LC_*
* LANG

the priority: LC_ALL > LC_* > LANG

the values: zh_CN.UTF-8

So you can modify the LANG or LC\_ALL in ~/.bashrc to zh_CH.UTF-8.
