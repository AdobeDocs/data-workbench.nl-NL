---
description: De informatie over Web-specifieke montages die in de Dataset van de Verwerking van het Logboek worden bepaald omvat dossiers die met de profielen van Adobe voor Plaats worden geleverd.
solution: Analytics
title: Web-specifieke Montages voor de Verwerking van het Logboek
topic: Data workbench
uuid: dea861a6-3f78-4cb9-8108-ecf397b37667
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Web-specifieke Montages voor de Verwerking van het Logboek{#web-specific-settings-for-log-processing}

De informatie over Web-specifieke montages die in de Dataset van de Verwerking van het Logboek worden bepaald omvat dossiers die met de profielen van Adobe voor Plaats worden geleverd.

Het filtreren dat door deze montages wordt bepaald komt voor nadat de logboekingangen de decoders verlaten en de transformaties worden toegepast maar vóór evaluatie door [!DNL Log Entry Condition]de.

* [HTTP-statusfiltering](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-log-proc.md#section-ac66acdcb6aa467d81c3721199e540fd)
* [Robotfiltering](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-log-proc.md#section-7f43681dfbc64b969619cb88f97d5ad5)

## HTTP-statusfiltering {#section-ac66acdcb6aa467d81c3721199e540fd}

U kunt uw implementatie van vormen [!DNL Site] om logboekingangen met sc-statuscodes van 400 of hierboven uit de dataset te verwijderen. De succesvolle verzoeken hebben statuscodes die minder dan 400 zijn. Uw standaardimplementatie omvat een [!DNL Log Processing Dataset Include] dossier waarin de status van HTTP het filtreren wordt gevormd.

**Om de configuratiemontages voor de status van HTTP uit te geven het filtreren**

1. Open het [!DNL Profile Manager] binnen uw datasetprofiel en open het [!DNL Dataset\Log Processing\Traffic\HTTP Status Filter.cfg] dossier.

   >[!NOTE]
   >
   >Als u uw implementatie van hebt aangepast, kan het dossier waarin deze configuratiemontages bestaan van de beschreven plaats verschillen. [!DNL Site]

1. Herzie of geef de waarden van de parameters van het dossier uit zoals gewenst. Gebruik het volgende voorbeeld als gids.

   ![](assets/cfg_WebParameters_HTTPStatusFilter.png)

   Voor informatie over de [!DNL Range] aandoening, zie [Voorwaarden](../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md).

1. Sparen het [!DNL HTTP Status Filter.cfg] dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## Robotfiltering {#section-7f43681dfbc64b969619cb88f97d5ad5}

U kunt uw implementatie van vormen [!DNL Site] om raadplegingsdossiers te gebruiken om logboekingangen te verwijderen die door bekende robots, testmanuscripten, en IP adressen voor interne gebruikers uit uw dataset worden geproduceerd. Uw standaardimplementatie omvat een [!DNL Log Processing Dataset Include] dossier waarin robot het filtreren wordt gevormd.

**Om de configuratiemontages voor het filtreren van de robot uit te geven**

1. Open het [!DNL Profile Manager] binnen uw datasetprofiel en open het [!DNL Dataset\Log Processing\Traffic\Robot Filter.cfg] dossier.

   >[!NOTE]
   >
   >Als u uw implementatie van hebt aangepast, kan het dossier waarin deze configuratiemontages bestaan van de beschreven plaats verschillen. [!DNL Site]

1. Herzie of geef de parameters van het dossier uit gebruikend het volgende voorbeeld en de informatie als gidsen:

   ![](assets/cfg_WebParameters_RobotFilter.png)

   Het dossier omvat een dossier [!DNL NotRobotCondition] dat door de volgende drie parameters wordt bepaald:

   * **Gevallenafhankelijke robotfiltering:** Waar of vals. Indien waar, wordt de brievenbus (bovenaan/onderaan) niet in overweging genomen bij het filtreren van robot.
   * **Robot Lookup File, Basislijn:** De weg en filename van het tekstdossier dat een lijst van browser gebruikersagenten bevat die bekende robots zijn en uit de dataset moeten worden gefiltreerd. Adobe verstrekt het de raadplegingsdossier van de basislijn robot. Als u geen weg specificeert, zoekt de server van de gegevenswerkbank dit dossier in de folder van Raadplegingen binnen de de installatiefolder van de gegevenswerkbank.
   * **Het Dossier van de Raadpleging van Robot, Uitgebreid:** De weg en filename van een facultatief tekstdossier dat een lijst van browser gebruikersagenten of IP adressen bevat die robots specifiek voor uw implementatie bepalen. Deze lijst kan interne controlerobots, testmanuscripten, en IP adressen voor interne gebruikers omvatten die uit de dataset zouden moeten worden gefiltreerd. Als u geen weg specificeert, zoekt de server van de gegevenswerkbank dit dossier in de folder van Raadplegingen binnen de de installatiefolder van de gegevenswerkbank.
   Als de browser van een logboekingang gebruikersagent niet vermeld in of raadplegingsdossier is, wordt de logboekingang beschouwd om door een echte bezoeker worden geproduceerd en niet van de dataset gefiltreerd.

   >[!NOTE]
   >
   >Het aanpassen in de dossiers van de robotraadpleging gebruikt substrings om tegen c-ip en de cs (gebruiker-agent) logboekgebieden te vergelijken. Als de zoektekenreeks begint met &quot;$&quot;, moet deze overeenkomen met de voorzijde van de tekenreeks die wordt getest, en als de tekenreeks eindigt met &quot;$&quot;, moet de zoektekenreeks overeenkomen met het einde van de tekenreeks die wordt getest. Als de zoektekenreeks begint met en eindigt met &quot;$&quot;, moeten de tekenreeksen exact overeenkomen met de logitems die moeten worden gefilterd. Bijvoorbeeld, om voor alle IP adressen in een blok van klasseC te testen, zou u een koord zoals $231.78.123 gebruiken. om een gelijke bij de voorzijde van het koord te dwingen. Dit zou adressen 231.78.123.0 door 231.78.123.255 aanpassen.

1. Sparen het dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

   Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

   >[!NOTE]
   >
   >Als het kritiek is dat de onderliggende logboekingangen die worden gebruikt om een dataset te construeren niet veranderen (zelfs als de transformaties die worden gebruikt om de dataset en zijn dimensieverandering te construeren en bij te werken), zouden het Dossier van de Raadpleging van de Robot, Basislijn, en het Uitgebreide Dossier van de Raadpleging van de Robot, versie moeten worden gecontroleerd. Het plaatsen van een versieaantal op deze dossiers zorgt ervoor dat de updates aan de dossiers van de standaardraadpleging van robot niet onbedoeld veranderen eerder geconstrueerde rapporteringsdatasets door ingangen in deze dossiers toe te voegen of te schrappen.

