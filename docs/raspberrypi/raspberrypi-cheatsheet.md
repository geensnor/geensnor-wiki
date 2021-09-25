---
layout: default
title: Pi cheatsheet
parent: Raspberry Pi
---

Niet allemaal puur Raspberry Pi specifiek

## Algemene handige commando's

|Wat|Commando|
|-----|------------------|
|Default username/password Raspberry Pi OS (voorheen raspbian)|pi/raspberry|
|Controleren welke DNS server de Raspberry Pi heeft gekregen|`sudo nano /etc/resolv.conf`|
|Config menu Raspberry Pi starten|`sudo raspi-config`|
|IP adres van PI bekijken|`ifconfig`|
|Hostname van PI bekijken|`Hostname`|
|Tekstbestand aanpassen|`nano <locatie/bestand>` eventueel met Sudo voor rechten|
|Commando uitvoeren met extra rechten|`sudo <command>`|
|Message buffer van de kernel tonen (jaja). Als je Pi bijvoorbeeld te weinig spanning heeft, zie je dat daar staan|`dmesg`|
|Directory weggooien met alles erin, zonder te vragen|`rm -r -f <directory>`|
|Uitgebreide lijst van onderdelen in een directory. Ook verborgen directories met een . ervoor bijvoorbeeld|`ls -al`| 
|Package weggooien|`sudo apt-get purge samba`|


### Updaten van je Pi

|Wat|Commando|
|-----|------------------|
|Update and upgrade raspbian|`sudo apt-get update && sudo apt-get upgrade`|
|Dist. upgrade|`sudo apt-get dist-upgrade`|
|Firmware update|`sudo apt-get install rpi-update` en vervolgens `sudo rpi-update`|
|Pi-hole updaten|`pihole -up`|
