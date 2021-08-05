---
layout: default
title: Commando's
parent: Raspberry Pi
---

# PI cheatsheet

Niet allemaal puur Raspberry Pi specifiek

## Algemeen

|Wat|Commando|
|-----|------------------|
|Controleren welke DNS server de Raspberry Pi heeft gekregen|`sudo nano /etc/resolv.conf`|
|Config menu Raspberry Pi starten|`sudo raspi-config`|

## Updaten 

|Wat|Commando|
|-----|------------------|
|Update raspbian|`sudo apt-get update`|
|Upgrade raspbian|`sudo apt-get upgrade`|
|Dist upgrade|`sudo apt-get dist-upgrade`|
|Firmware update|`sudo apt-get install rpi-update` en vervolgens `sudo rpi-update`|

