---
description: Servercomponenten bijwerken voor Data Workbench 6.2 en 6.2.2.
title: DWB Server upgrade 6.1 tot 6.2
uuid: 61ecf2c1-9ced-42d3-a010-4a4fec13b987
exl-id: 094b20f0-bc4a-467a-899e-e1800a624508,20e2cf87-519e-4c27-9201-1275550bb72a
source-git-commit: 050468bf6a9ef9c07719ded79c8ab68753d58647
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Upgrade van DWB-server: 6.1 t/m 6.2{#dwb-server-upgrade-to}

Servercomponenten bijwerken voor Data Workbench 6.2 en 6.2.2.

## Problemen met upgrades voor 6.2 {#section-3cc74d08f7454d698b5a6d3f1dcde282}

* Het attributieprofiel is geconfigureerd voor gebruikers die het Adobe SC-profiel hebben geïmplementeerd, zodat ze de gegevensfeed Analytics (SC/Insight) kunnen gebruiken. Door gebrek, worden de de Marketing en gebeurtenissen van de Omzetting gebruikt als standaardinteractie die in op regel-gebaseerde modellen wordt geëvalueerd. Zie [Het Attributieprofiel](https://experienceleague.adobe.com/docs/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html?lang=en) implementeren voor meer informatie.
* Voor gebruikers van het Adobe SC-profiel dat een upgrade uitvoert naar Data Workbench 6.2 en u de standaardconfiguraties niet gebruikt, controleert u of de [!DNL x-bot_id]-waarde in het [!DNL SC Fields.cfg]-bestand correct wordt gedecodeerd en of het veld [!DNL x-bot_id] correct wordt weergegeven in de [!DNL Decoding Instructions.cfg]- en [!DNL Exclude Hit.cfg]-bestanden. Dit zal slechts een kwestie zijn als u het configuratiedossier van de standaardconfiguratie hebt gewijzigd.
* Als u ongebruikte velden in het [!DNL Dataset > Log Processing > SC Fields.cfg]-bestand voor het Adobe SC-profiel hebt verwijderd, moet u deze bijwerken om de bijgewerkte veldwaarden voor het kenmerk te kunnen gebruiken (zie [Het kenmerk Profile](https://experienceleague.adobe.com/docs/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html?lang=en) implementeren).

## Problemen met upgrades voor 6.2.2 {#section-8704a9ac358246cd81233dd0982d534f}

* De **[!UICONTROL Browsers]** en **[!UICONTROL Operating Systems]** raadplegingsdossiers zullen niet binnen het erfenis **[!UICONTROL Traffic]** profiel (bijvoorbeeld, [!DNL Lookups\Traffic\Browsers.txt)] worden bijgewerkt. In plaats daarvan gebruikt de configuratie van het **[!UICONTROL Traffic]** profiel de bundel DeviceAtlas ( [!DNL Lookups\DeviceAtlas\DeviceAtlas.bundle]) om deze configuratieinformatie te verstrekken.
* Data Workbench 6.2.1 zal de laatste versie zijn om een download van de cliënttoepassing met 32 bits te verstrekken. Alle toekomstige downloads van clienttoepassingen zijn 64-bits en blijven Windows 7 of hoger nodig. Geheugenbeperkingen van de 32-bits toepassing worden verholpen met de introductie van de 64-bits toepassing die begint met de 6.1-release.

>[!NOTE]
>
>De versie met 32 bits van de de cliënttoepassing van de Data Workbench kan potentiële kwesties met betrekking tot geheugenbeperkingen ervaren wanneer het runnen van vooruitlopende modellen gebruikend de het groeperen en het scoren eigenschappen.
