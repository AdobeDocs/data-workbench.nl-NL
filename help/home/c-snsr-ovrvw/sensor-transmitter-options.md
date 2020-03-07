---
description: Informatie over de opstartopdrachten van de zender van de Sensor voor UNIX en voor Vensters.
title: Sensor Transmitter bevel-lijn Opties
uuid: 8d077d76-a709-494e-a176-07ca3e761662
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Sensor Transmitter bevel-lijn Opties{#sensor-transmitter-command-line-options}

Informatie over de opstartopdrachten van de zender van de Sensor voor UNIX en voor Vensters.

## Opstartopdracht voor UNIX {#section-e8e7a6e62971499ba5f633d896590949}

Om de zender van de Sensor op een stam van UNIX te beginnen, gebruikt u het volgende bevel:

```
txlogd -f configFileName
```

waar configFileName volledig is - gekwalificeerde naam van het dossier van de transmissieconfiguratie (txlogd.conf).

Door gebrek, loopt de zender als achtergrondproces (een daemon) en schrijft operationele berichten aan syslog.

Het volgende is een volledige lijst van de bevel-lijn schakelaars voor tekst:

| Schakelaar | Beschrijving |
|---|---|
| -f | Specificeert volledig - gekwalificeerde naam van het configuratiedossier (txlogd.conf). Als u deze schakelaar niet specificeert, zoekt de zender txlogd.conf in de huidige folder. |
| -n | Begint de zender op interactieve wijze (niet als achtergrondproces). |
| -i | Begint de zender op interactieve wijze en leidt zuiveren output aan stdout. |
| -d | Begint de zender als achtergrondproces en leidt zuiveren output aan txlogd-debug.log in de huidige folder. |
| -c | Begint de zender en leidt tot het dossier van de schijfrij als het niet bestaat. Als de schijfrij reeds bestaat, wordt deze parameter genegeerd. |
| -x | Begint de zender en veroorzaakt het om weg te gaan nadat het het laatste pakket in de schijfrij overbrengt. U kunt deze optie gebruiken om de rij in voorbereiding op een administratieve verrichting zoals het creëren van een nieuw rijdossier af te voeren. |

## Opstartopdracht voor Windows {#section-aaafbb68559a45c7a40abe6a4c80ccc0}

Om Sensor te beginnen en het te registreren als dienst op een systeem van Vensters, gebruikt u het volgende bevel:

```
txlog /regserver
```

