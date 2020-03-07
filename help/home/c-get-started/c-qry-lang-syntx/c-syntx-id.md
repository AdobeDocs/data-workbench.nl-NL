---
description: De metrische, afmeting, en de filteruitdrukkingen kunnen herkenningstekens gebruiken om naar genoemde metriek, afmetingen, en filters te verwijzen.
solution: Analytics
title: Syntaxis voor identificatoren
topic: Data workbench
uuid: 9cfa188a-05ca-4163-a268-e33fce9a1929
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Syntaxis voor identificatoren{#syntax-for-identifiers}

De metrische, afmeting, en de filteruitdrukkingen kunnen herkenningstekens gebruiken om naar genoemde metriek, afmetingen, en filters te verwijzen.

Deze herkenningstekens zijn gevoelig geval en moeten precies worden getypt aangezien zij worden bepaald.

Een geldig herkenningsteken kan één of meer van het volgende bevatten:

* Onderstrepen (_). De onderstreept in een herkenningsteken vertegenwoordigen ruimten in metrisch, afmeting, of filternaam. Bijvoorbeeld, zou de dimensie van de Verwijzing van de Zitting worden bedoeld zoals [!DNL Session_Referrer] in een uitdrukking.
* Percentage tekens (%)
* Hoofdletters (A-Z)
* Lagere letters (a-z)
* Dollar-tekens ($)
* Aantallen (0-9), behalve als eerste karakter in een herkenningsteken.
* Niet-ASCII-tekens

Alle andere karakters zijn illegaal in een herkenningsteken.

Deze zelfde regels zijn op de namen van metriek, afmetingen, en filters van toepassing wanneer zij buiten uitdrukkingen worden gebruikt, behalve dat de namen ruimten kunnen bevatten maar niet onderstreept. Bijvoorbeeld, kunt u de afmeting van de Referateur van de Zitting in het [!DNL Transformation.cfg] dossier als Referrer van de Zitting bepalen, maar niet [!DNL Session_Referrer].
