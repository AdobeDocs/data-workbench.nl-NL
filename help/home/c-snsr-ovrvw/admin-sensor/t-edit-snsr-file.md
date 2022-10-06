---
description: Het Sensor-configuratiebestand, txlogd.conf, bevat parameters die Sensor gebruikt om een verbinding tot stand te brengen met de gegevenswerkbench-server.
title: Het bestand Sensor txlogd.conf bewerken
uuid: e7f41c14-9047-4e1a-be0f-8acc8ecb1160
exl-id: ed243bb4-cf87-4bcf-89d6-5ff5cec3bc6e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Het bestand Sensor txlogd.conf bewerken{#editing-the-sensor-txlogd-conf-file}

{{eol}}

Het Sensor-configuratiebestand, txlogd.conf, bevat parameters die Sensor gebruikt om een verbinding tot stand te brengen met de gegevenswerkbench-server.

Deze parameters zijn onder andere het adres, het poortnummer en het communicatieprotocol (HTTP of HTTPS) van de server. Het configuratiedossier bevat ook logboek-inhoud het filtreren opties en gecontroleerde experimentinformatie. Met gecontroleerde experimenten kunnen siteontwerpers experimenten uitvoeren om inhoud te testen of wijzigingen te ontwerpen voor een subset van alle sitebezoekers.

Bij het wijzigen van andere [!DNL txlogd.conf] parameters, zoals het IP-adres van de [!DNL data workbench server] of de naam van de [!DNL Sensor], kunt u eenvoudig vervangen [!DNL txlogd.conf] met de bijgewerkte versie en [!DNL Sensor] worden de wijzigingen automatisch doorgevoerd. Op sommige systemen kunt u het bestand mogelijk niet bewerken of vervangen zonder de webserver of het verzendproces te stoppen.

**Txlogd.conf openen en bewerken**

1. Bladeren naar de [!DNL Sensor] installatiemap en open de [!DNL txlogd.conf] in een teksteditor.
1. Bewerk het bestand naar wens.
1. Sla het bestand op en sluit het.

   * De locatie van het gecontroleerde configuratiebestand voor het experiment (gedefinieerd door de parameter ExpFile in het dialoogvenster [!DNL txlogd.conf] bestand) moet zich in een map op de webserver bevinden die toegankelijk is voor ontwikkelaars van webinhoud of wordt beheerd door uw contentbeheersysteem.
   * De waarde in de parameter ExpCookieURL is een virtuele pagina die wordt gebruikt om websites te testen. Een gebruiker die die de pagina bezoekt, krijgt een nieuwe tracking-id.

Meer informatie over het werken met [!DNL txlogd.conf], neem contact op met de Adobe Consulting Services.
