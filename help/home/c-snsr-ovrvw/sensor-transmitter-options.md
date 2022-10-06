---
description: Informatie over de opstartopdrachten van de zender Sensor voor UNIX en voor Windows.
title: Sensor Transmitter Command-Line Opties
uuid: 8d077d76-a709-494e-a176-07ca3e761662
exl-id: f4b27859-8fab-42cd-bad0-b32f87764668
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Sensor Transmitter Command-Line Opties{#sensor-transmitter-command-line-options}

{{eol}}

Informatie over de opstartopdrachten van de zender Sensor voor UNIX en voor Windows.

## Opdracht opstarten voor UNIX {#section-e8e7a6e62971499ba5f633d896590949}

Om de zender van de Sensor op een stam van UNIX te beginnen, gebruikt u het volgende bevel:

```
txlogd -f configFileName
```

waarbij configFileName de volledig gekwalificeerde naam van het dossier van de transmissieconfiguratie (txlogd.conf) is.

Door gebrek, loopt de zender als achtergrondproces (een daemon) en schrijft operationele berichten aan syslog.

Hier volgt een volledige lijst met opdrachtregelswitches voor txlogd:

| Overschakelen | Beschrijving |
|---|---|
| -f | Specificeert volledig - gekwalificeerde naam van het configuratiedossier (txlogd.conf). Als u deze schakelaar niet specificeert, zoekt de zender txlogd.conf in de huidige folder. |
| -n | Start de zender in de interactieve modus (niet als een achtergrondproces). |
| -i | Start de zender in de interactieve modus en stuurt foutopsporingsuitvoer naar stdout. |
| -d | Start de zender als een achtergrondproces en stuurt foutopsporingsuitvoer naar txlogd-debug.log in de huidige map. |
| -c | Start de zender en maak het bestand voor de schijfwachtrij als dit niet bestaat. Als de schijfwachtrij al bestaat, wordt deze parameter genegeerd. |
| -x | Begint de zender en veroorzaakt het om weg te gaan nadat het het laatste pakket in de schijfrij overbrengt. U kunt deze optie gebruiken om de wachtrij te laten leegmaken ter voorbereiding op een beheerbewerking, zoals het maken van een nieuw bestand in de wachtrij. |

## Opdracht opstarten voor Windows {#section-aaafbb68559a45c7a40abe6a4c80ccc0}

Om Sensor te beginnen en het als dienst op een systeem van Vensters te registreren, gebruikt u het volgende bevel:

```
txlog /regserver
```
