---
description: Servercomponenten bijwerken voor Data Workbench 6.2 en 6.2.2.
title: DWB Server upgrade 6.1 tot 6.2
uuid: 61ecf2c1-9ced-42d3-a010-4a4fec13b987
exl-id: 094b20f0-bc4a-467a-899e-e1800a624508,20e2cf87-519e-4c27-9201-1275550bb72a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Upgrade van DWB-server: 6.1 t/m 6.2{#dwb-server-upgrade-to}

{{eol}}

Servercomponenten bijwerken voor Data Workbench 6.2 en 6.2.2.

## Problemen met upgrades voor 6.2 {#section-3cc74d08f7454d698b5a6d3f1dcde282}

* Het attributieprofiel is geconfigureerd voor gebruikers die het Adobe SC-profiel hebben geïmplementeerd, zodat ze de gegevensfeed Analytics (SC/Insight) kunnen gebruiken. Door gebrek, worden de de Marketing en gebeurtenissen van de Omzetting gebruikt als standaardinteractie die in op regel-gebaseerde modellen wordt geëvalueerd. Zie [Het kenmerkprofiel implementeren](https://experienceleague.adobe.com/docs/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html?lang=en) voor aanvullende informatie.
* Voor gebruikers van het profiel van Adobe SC die aan Data Workbench 6.2 bevorderen, als u niet de standaardconfiguraties gebruikt, verifieer dat [!DNL x-bot_id] in de [!DNL SC Fields.cfg] wordt gedecodeerd en dat het [!DNL x-bot_id] het veld wordt correct weergegeven in het dialoogvenster [!DNL Decoding Instructions.cfg] en de [!DNL Exclude Hit.cfg] bestanden. Dit zal slechts een kwestie zijn als u het configuratiedossier van de standaardconfiguratie hebt gewijzigd.
* Als u ongebruikte velden in het dialoogvenster [!DNL Dataset > Log Processing > SC Fields.cfg] bestand voor het Adobe SC-profiel, moet u bijwerken om de bijgewerkte veldwaarden voor het kenmerk te kunnen gebruiken (zie [Het kenmerkprofiel implementeren](https://experienceleague.adobe.com/docs/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html?lang=en)).

## Problemen met upgrades voor 6.2.2 {#section-8704a9ac358246cd81233dd0982d534f}

* De **[!UICONTROL Browsers]** en **[!UICONTROL Operating Systems]** opzoekbestanden worden niet bijgewerkt in de verouderde **[!UICONTROL Traffic]** profiel (bijvoorbeeld [!DNL Lookups\Traffic\Browsers.txt)]. In plaats daarvan, configuratie van **[!UICONTROL Traffic]** profiel gebruikt de DeviceAtlas-bundel ( [!DNL Lookups\DeviceAtlas\DeviceAtlas.bundle]) om deze configuratiegegevens te verstrekken.
* Data Workbench 6.2.1 zal de laatste versie zijn om een download van de cliënttoepassing met 32 bits te verstrekken. Alle toekomstige downloads van clienttoepassingen zijn 64-bits en blijven Windows 7 of hoger nodig. Geheugenbeperkingen van de 32-bits toepassing worden verholpen met de introductie van de 64-bits toepassing die begint met de 6.1-release.

>[!NOTE]
>
>De versie met 32 bits van de de cliënttoepassing van de Data Workbench kan potentiële kwesties met betrekking tot geheugenbeperkingen ervaren wanneer het runnen van vooruitlopende modellen gebruikend de het groeperen en het scoren eigenschappen.
