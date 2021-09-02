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
|Commando uitvoeren met voldoende rechten|`sudo <command>`

### Updaten van je Pi

|Wat|Commando|
|-----|------------------|
|Update and upgrade raspbian|`sudo apt-get update && sudo apt-get upgrade`|
|Dist. upgrade|`sudo apt-get dist-upgrade`|
|Firmware update|`sudo apt-get install rpi-update` en vervolgens `sudo rpi-update`|
|Pi-hole updaten|`pihole -up`|
