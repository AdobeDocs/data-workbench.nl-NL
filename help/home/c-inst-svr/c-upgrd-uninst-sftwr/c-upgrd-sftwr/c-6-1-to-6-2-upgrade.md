---
description: Serveronderdelen voor gegevenswerkbank 6.2 en 6.2.2 upgraden.
title: DWB-serverupgrade 6.1 naar 6.2
uuid: 61ecf2c1-9ced-42d3-a010-4a4fec13b987
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# DWB-serverupgrade: 6.1 t/m 6.2{#dwb-server-upgrade-to}

Serveronderdelen voor gegevenswerkbank 6.2 en 6.2.2 upgraden.

## Problemen met upgraden voor 6.2 {#section-3cc74d08f7454d698b5a6d3f1dcde282}

* Het profiel van de Attributie wordt gevormd voor gebruikers die het profiel van Adobe SC hebben uitgevoerd om het de gegevensvoer van de Analytics (SC/Insight) aan te wenden. Door gebrek, worden de de Marketing en gebeurtenissen van de Omzetting gebruikt als standaardinteractie die in de op regels-gebaseerde modellen wordt geëvalueerd. Zie Het [Attributieprofiel](https://docs.adobe.com/help/en/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html) implementeren voor meer informatie.
* Voor gebruikers van de het profielbevordering van Adobe SC aan Werkbank 6.2 van Gegevens, als u niet de standaardconfiguraties gebruikt, verifieer dat de [!DNL x-bot_id] waarde in het [!DNL SC Fields.cfg] dossier behoorlijk wordt gedecodeerd en dat het [!DNL x-bot_id] gebied behoorlijk in de [!DNL Decoding Instructions.cfg] en de [!DNL Exclude Hit.cfg] dossiers vermeld is. Dit zal slechts een kwestie zijn als u het configuratiedossier van de standaardconfiguratie hebt gewijzigd.
* Als u ongebruikte gebieden in het [!DNL Dataset > Log Processing > SC Fields.cfg] dossier voor het profiel van Adobe SC hebt geschrapt, zult u moeten bijwerken om bijgewerkte gebiedswaarden aan te passen die voor het profiel van de Attributie worden gebruikt (zie het [Opstellen van het Profiel](https://docs.adobe.com/help/en/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html)van de Attributie).

## Problemen met upgraden voor 6.2.2 {#section-8704a9ac358246cd81233dd0982d534f}

* De **[!UICONTROL Browsers]** en **[!UICONTROL Operating Systems]** raadplegingsdossiers zullen niet binnen het erfenisprofiel (bijvoorbeeld, **[!UICONTROL Traffic]** [!DNL Lookups\Traffic\Browsers.txt)]worden bijgewerkt. In plaats daarvan, zal de configuratie van het **[!UICONTROL Traffic]** profiel de bundel DeviceAtlas ( [!DNL Lookups\DeviceAtlas\DeviceAtlas.bundle]) gebruiken om deze configuratieinformatie te verstrekken.
* De Werkbank 6.2.1 van gegevens zal de laatste versie zijn om een download van de cliënttoepassing met 32 bits te verstrekken. Alle toekomstige downloads van de cliënttoepassing zullen met 64 bits zijn en blijven Vensters 7 of nieuwer vereisen. De beperkingen van het geheugen van de toepassing met 32 bits worden behandeld met de introductie van de toepassing met 64 bits die met de versie met 6.1 begint.

>[!NOTE]
>
>De 32 beetjeversie van de de cliënttoepassing van de Werkbank van Gegevens kan potentiële kwesties met betrekking tot geheugenbeperkingen ervaren wanneer het runnen van vooruitlopende modellen die de het groeperen en het noteren eigenschappen gebruiken.

