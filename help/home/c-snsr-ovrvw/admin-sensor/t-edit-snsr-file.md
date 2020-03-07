---
description: Het de configuratiedossier van de Sensor, txlogd.conf, bevat parameters die de Sensor gebruikt om een verbinding met de server van de gegevenswerkbank te vestigen.
solution: Insight
title: Het uitgeven van het Dossier van de Sensor txlogd.conf
uuid: e7f41c14-9047-4e1a-be0f-8acc8ecb1160
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# Het uitgeven van het Dossier van de Sensor txlogd.conf{#editing-the-sensor-txlogd-conf-file}

Het de configuratiedossier van de Sensor, txlogd.conf, bevat parameters die de Sensor gebruikt om een verbinding met de server van de gegevenswerkbank te vestigen.

Deze parameters omvatten het adres van de server, het havenaantal, en het communicatie protocol (HTTP of HTTPS). Het configuratiedossier bevat ook logboek-inhoud het filtreren opties en gecontroleerde experimentele informatie. De gecontroleerde experimenten laten plaatsontwerpers toe om experimenten uit te voeren om inhoud of ontwerpveranderingen op een ondergroep van alle plaatsbezoekers te testen.

Wanneer het veranderen van andere [!DNL txlogd.conf] parameters, zoals het IP adres van het [!DNL data workbench server] of de naam van het [!DNL Sensor], kunt u eenvoudig kunnen vervangen [!DNL txlogd.conf] met de bijgewerkte versie en [!DNL Sensor] zal automatisch de veranderingen opnemen. Op sommige systemen, kunt u niet het dossier uitgeven of kunnen vervangen zonder of de Webserver of het transmissieproces tegen te houden.

**Om txlogd.conf te openen en uit te geven**

1. Doorblader aan de [!DNL Sensor] installatiefolder en open het [!DNL txlogd.conf] dossier in een tekstredacteur.
1. Bewerk het bestand indien nodig.
1. Sparen en sluit het dossier.

   * De plaats van het gecontroleerde dossier van de experimentconfiguratie (die door de parameter ExpFile in het [!DNL txlogd.conf] dossier wordt bepaald) zou in een folder op de Webserver moeten zijn die voor uw ontwikkelaars van de Webinhoud toegankelijk is of door uw systeem van het inhoudsbeheer wordt gecontroleerd.
   * De waarde in de parameter ExpCookieURL is een virtuele pagina die wordt gebruikt om websites te testen. Een gebruiker die die die pagina bezoekt zal een nieuwe het volgen identiteitskaart worden gegeven.

Voor meer informatie over het werken met [!DNL txlogd.conf], gelieve te contacteren de Raadplegende Diensten van Adobe.
