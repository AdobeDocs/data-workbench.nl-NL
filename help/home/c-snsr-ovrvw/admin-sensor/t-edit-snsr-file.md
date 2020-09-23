---
description: Het Sensor-configuratiebestand, txlogd.conf, bevat parameters die Sensor gebruikt om een verbinding tot stand te brengen met de gegevenswerkbench-server.
solution: Analytics
title: Het bestand Sensor txlogd.conf bewerken
uuid: e7f41c14-9047-4e1a-be0f-8acc8ecb1160
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Het bestand Sensor txlogd.conf bewerken{#editing-the-sensor-txlogd-conf-file}

Het Sensor-configuratiebestand, txlogd.conf, bevat parameters die Sensor gebruikt om een verbinding tot stand te brengen met de gegevenswerkbench-server.

Deze parameters zijn onder andere het adres, het poortnummer en het communicatieprotocol (HTTP of HTTPS) van de server. Het configuratiedossier bevat ook logboek-inhoud het filtreren opties en gecontroleerde experimentinformatie. Met gecontroleerde experimenten kunnen siteontwerpers experimenten uitvoeren om inhoud te testen of wijzigingen te ontwerpen voor een subset van alle sitebezoekers.

Wanneer het veranderen van andere [!DNL txlogd.conf] parameters, zoals het IP adres van het [!DNL data workbench server] of de naam van het [!DNL Sensor], kunt u eenvoudig [!DNL txlogd.conf] met de bijgewerkte versie kunnen vervangen en [!DNL Sensor] zal automatisch de veranderingen opnemen. Op sommige systemen kunt u het bestand mogelijk niet bewerken of vervangen zonder de webserver of het verzendproces te stoppen.

**Txlogd.conf openen en bewerken**

1. Blader naar de [!DNL Sensor] installatiemap en open het [!DNL txlogd.conf] bestand in een teksteditor.
1. Bewerk het bestand naar wens.
1. Sla het bestand op en sluit het.

   * De locatie van het gecontroleerde configuratiebestand voor experimenten (gedefinieerd door de parameter ExpFile in het [!DNL txlogd.conf] bestand) moet zich in een map op de webserver bevinden die toegankelijk is voor ontwikkelaars van webinhoud of wordt beheerd door uw contentbeheersysteem.
   * De waarde in de parameter ExpCookieURL is een virtuele pagina die wordt gebruikt om websites te testen. Een gebruiker die die de pagina bezoekt, krijgt een nieuwe tracking-id.

Neem voor meer informatie over het werken met [!DNL txlogd.conf]Adobe Consulting Services contact op.
