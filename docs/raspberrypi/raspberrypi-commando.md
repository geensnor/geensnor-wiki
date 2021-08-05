---
layout: default
title: PI cheatsheet
parent: Raspberry Pi
---

# PI cheatsheet

Niet allemaal puur Raspberry Pi specifiek

## Algemene tips

### Hostnames ipv IP adressen

Meestal heb je thuis een lokale DHCP server draaien die elk nieuw device een dynamisch IP adres serveert. Zo kan het zijn dat je PI om wat voor reden een nieuw ip adres krijgt. Het achterhalen van een IP adres van je PI, met name een headless PI, is wat lastig. HDMI kabel zoeken, aansluiten, opzoeken. Gedoe gedoe.

Door gebruik te maken van hostnames los je dat op. Je PI broadcast de hostname over je netwerk waardoor alle clients weten hoe de PI heet. Op die manier kun je de PI direct benaderen op zijn naam en maakt het IP adres niet meer uit.

De hostname instellen kan via `raspi-config`. Vervolgens is de PI te bereiken op `gekozenaam.local`

### Voeding en undervoltage

PI's zijn gevoelig voor voldoende voeding. Bij onvoldoende voeding gaat hij throttlen, wordt traag en onstabiel. Een willekeurige telefoon USB voeding levert waarschijnlijk niet in alle situaties voldoende stroom. Dit is te zien door een bliksem icoontje in beeld (als je hem met scherm gebruikt) en anders kun je via `/opt/vc/bin/vcgencmd get_throttled` zien of hij throttled is (en dus undervoltage heeft). Is de response `throttled=0x0` dan is alles koek en ei. Andere situaties en codes zijn terug te vinden op deze [pagina met foutcodes](https://github.com/raspberrypi/documentation/blob/master/raspbian/applications/vcgencmd.md#get_throttled).

## Commando's

### Algemene handige commando's

|Wat|Commando|
|-----|------------------|
|Default username/password Raspberry Pi OS (voorheen raspbian)|pi/raspberry|
|Controleren welke DNS server de Raspberry Pi heeft gekregen|`sudo nano /etc/resolv.conf`|
|Config menu Raspberry Pi starten|`sudo raspi-config`|
|IP adres van PI bekijken|`ifconfig`|
|Hostname van PI bekijken|`Hostname`|
|Tekstbestand aanpassen|`nano <locatie/bestand>` eventueel met Sudo voor rechten|
|Commando uitvoeren met voldoende rechten|`sudo <command>`

### Updaten van je PI

|Wat|Commando|
|-----|------------------|
|Update and upgrade raspbian|`sudo apt-get update && sudo apt-get upgrade`|
|Dist. upgrade|`sudo apt-get dist-upgrade`|
|Firmware update|`sudo apt-get install rpi-update` en vervolgens `sudo rpi-update`|
|Pi-hole updaten|`pihole -up`|
