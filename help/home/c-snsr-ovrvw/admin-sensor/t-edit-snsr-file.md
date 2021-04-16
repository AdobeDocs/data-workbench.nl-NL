---
description: Het Sensor-configuratiebestand, txlogd.conf, bevat parameters die Sensor gebruikt om een verbinding tot stand te brengen met de gegevenswerkbench-server.
title: Het bestand Sensor txlogd.conf bewerken
uuid: e7f41c14-9047-4e1a-be0f-8acc8ecb1160
exl-id: ed243bb4-cf87-4bcf-89d6-5ff5cec3bc6e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Het bestand Sensor txlogd.conf{#editing-the-sensor-txlogd-conf-file} bewerken

Het Sensor-configuratiebestand, txlogd.conf, bevat parameters die Sensor gebruikt om een verbinding tot stand te brengen met de gegevenswerkbench-server.

Deze parameters zijn onder andere het adres, het poortnummer en het communicatieprotocol (HTTP of HTTPS) van de server. Het configuratiedossier bevat ook logboek-inhoud het filtreren opties en gecontroleerde experimentinformatie. Met gecontroleerde experimenten kunnen siteontwerpers experimenten uitvoeren om inhoud te testen of wijzigingen te ontwerpen voor een subset van alle sitebezoekers.

Wanneer u andere [!DNL txlogd.conf] parameters wijzigt, zoals het IP-adres van [!DNL data workbench server] of de naam van [!DNL Sensor], kunt u [!DNL txlogd.conf] eenvoudig vervangen door de bijgewerkte versie en [!DNL Sensor] zal de wijzigingen automatisch doorvoeren. Op sommige systemen kunt u het bestand mogelijk niet bewerken of vervangen zonder de webserver of het verzendproces te stoppen.

**Txlogd.conf openen en bewerken**

1. Blader naar de installatiemap [!DNL Sensor] en open het bestand [!DNL txlogd.conf] in een teksteditor.
1. Bewerk het bestand naar wens.
1. Sla het bestand op en sluit het.

   * De locatie van het gecontroleerde configuratiebestand voor experimenten (gedefinieerd door de parameter ExpFile in het bestand [!DNL txlogd.conf]) moet zich in een map op de webserver bevinden die toegankelijk is voor uw ontwikkelaars van webinhoud of wordt beheerd door uw contentbeheersysteem.
   * De waarde in de parameter ExpCookieURL is een virtuele pagina die wordt gebruikt om websites te testen. Een gebruiker die die de pagina bezoekt, krijgt een nieuwe tracking-id.

Neem contact op met de Adobe Consulting Services voor meer informatie over het werken met [!DNL txlogd.conf].
