---
description: Informatie over webspecifieke instellingen die zijn gedefinieerd in de gegevensset voor logverwerking. Dit zijn bestanden die worden geleverd met Adobe-profielen voor site.
title: Webspecifieke instellingen voor logverwerking
uuid: dea861a6-3f78-4cb9-8108-ecf397b37667
exl-id: abb6e6a7-011f-40d6-b778-16da2332af72
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# Webspecifieke instellingen voor logverwerking{#web-specific-settings-for-log-processing}

{{eol}}

Informatie over webspecifieke instellingen die zijn gedefinieerd in de gegevensset voor logverwerking. Dit zijn bestanden die worden geleverd met Adobe-profielen voor site.

Filteren die door deze instellingen wordt gedefinieerd, vindt plaats nadat de logitems de decoders verlaten en de transformaties zijn toegepast, maar voordat de gegevens door de [!DNL Log Entry Condition].

* [HTTP-statusfilters](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-log-proc.md#section-ac66acdcb6aa467d81c3721199e540fd)
* [Robot filteren](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-log-proc.md#section-7f43681dfbc64b969619cb88f97d5ad5)

## HTTP-statusfilters {#section-ac66acdcb6aa467d81c3721199e540fd}

U kunt uw implementatie van vormen [!DNL Site] om logingangen met sc-statuscodes van 400 of hoger uit de dataset te verwijderen. Succesvolle aanvragen hebben statuscodes die kleiner zijn dan 400. Uw standaardimplementatie bevat een [!DNL Log Processing Dataset Include] bestand waarin HTTP-statusfiltering is geconfigureerd.

**De configuratie-instellingen voor HTTP-statusfiltering bewerken**

1. Open de [!DNL Profile Manager] in uw gegevenssetprofiel en open [!DNL Dataset\Log Processing\Traffic\HTTP Status Filter.cfg] bestand.

   >[!NOTE]
   >
   >Als u uw implementatie van [!DNL Site]kan het bestand waarin deze configuratie-instellingen aanwezig zijn, afwijken van de beschreven locatie.

1. Controleer of bewerk de waarden van de parameters van het bestand naar wens. Gebruik het volgende voorbeeld als richtlijn.

   ![](assets/cfg_WebParameters_HTTPStatusFilter.png)

   Voor informatie over de [!DNL Range] voorwaarde, zie [Voorwaarden](../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md).

1. Sla de [!DNL HTTP Status Filter.cfg] bestand door met de rechtermuisknop te klikken **[!UICONTROL (modified)]** boven aan het venster en klikken op **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## Robot filteren {#section-7f43681dfbc64b969619cb88f97d5ad5}

U kunt uw implementatie van vormen [!DNL Site] om raadplegingsdossiers te gebruiken om logboekingangen te verwijderen die door bekende robots, testmanuscripten, en IP adressen voor interne gebruikers van uw dataset worden geproduceerd. Uw standaardimplementatie bevat een [!DNL Log Processing Dataset Include] bestand waarin robot filtering is geconfigureerd.

**De configuratie-instellingen voor robotfiltering bewerken**

1. Open de [!DNL Profile Manager] in uw gegevenssetprofiel en open [!DNL Dataset\Log Processing\Traffic\Robot Filter.cfg] bestand.

   >[!NOTE]
   >
   >Als u uw implementatie van [!DNL Site]kan het bestand waarin deze configuratie-instellingen aanwezig zijn, afwijken van de beschreven locatie.

1. Bekijk of bewerk de parameters van het bestand met behulp van het volgende voorbeeld en informatie als hulplijnen:

   ![](assets/cfg_WebParameters_RobotFilter.png)

   Het bestand bevat een [!DNL NotRobotCondition] dat wordt gedefinieerd door de volgende drie parameters:

   * **Niet-hoofdlettergevoelige robot filteren:** Waar of onwaar. Indien waar (true), wordt lettergebruik (boven/onder) niet meegenomen bij het filteren van robot.
   * **Robot Lookup File, Baseline:** Het pad en de bestandsnaam van het tekstbestand dat een lijst bevat met bekende robots voor browsers die uit de gegevensset moeten worden gefilterd. Adobe geeft het basisbestand voor het opzoeken van robot weer. Als u geen pad opgeeft, zoekt de gegevenswerkbankserver naar dit bestand in de map Lookups in de installatiemap van de gegevenswerkbankserver.
   * **Robot Lookup File, Extended:** Het pad en de bestandsnaam van een optioneel tekstbestand dat een lijst bevat met browsergebruikersagents of IP-adressen die robots definiëren die specifiek zijn voor uw implementatie. Deze lijst kan interne controlerobots, testmanuscripten, en IP adressen voor interne gebruikers omvatten die uit de dataset zouden moeten worden gefiltreerd. Als u geen pad opgeeft, zoekt de gegevenswerkbankserver naar dit bestand in de map Lookups in de installatiemap van de gegevenswerkbankserver.

   Als de browser van een logboekingang browser gebruikersagent niet in één van beide raadplegingsdossier vermeld is, wordt de logboekingang beschouwd om door een echte bezoeker worden geproduceerd en niet van de dataset gefiltreerd.

   >[!NOTE]
   >
   >Bij afstemmen in de opzoekbestanden voor robot worden subtekenreeksen gebruikt om te vergelijken met de logvelden c-ip en cs (user-agent). Als de zoektekenreeks begint met &quot;$&quot;, moet deze overeenkomen met de voorzijde van de tekenreeks die wordt getest en als de tekenreeks eindigt met &quot;$&quot;, moet de zoektekenreeks overeenkomen met het einde van de tekenreeks die wordt getest. Als de zoektekenreeks begint met en eindigt met &quot;$&quot;, moeten de tekenreeksen exact overeenkomen voordat de logbestandvermelding wordt uitgefilterd. Bijvoorbeeld, om voor alle IP adressen in een blok van klasse C te testen, zou u een koord zoals $231.78.123 gebruiken. om een overeenkomst aan de voorzijde van de tekenreeks af te dwingen. Dit zou adressen 231.78.123.0 door 231.78.123.255 aanpassen.

1. Sla het bestand op door met de rechtermuisknop te klikken **[!UICONTROL (modified)]** boven aan het venster en klikken op **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

   Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

   >[!NOTE]
   >
   >Als het kritiek is dat de onderliggende logboekingangen die worden gebruikt om een dataset te construeren niet veranderen (zelfs als de transformaties die worden gebruikt om de dataset en zijn dimensies te construeren en bij te werken veranderen), het Dossier van de Opzoekmachine van Robot, Basislijn, en het Dossier van de Opzoeken van Robot, Uitgebreid, zou versiecontroleerd moeten zijn. Door een versienummer op deze bestanden te plaatsen, zorgt u ervoor dat updates van de standaardbestanden voor het opzoeken van robot niet per ongeluk eerder geconstrueerde rapportgegevenssets wijzigen door items in deze bestanden toe te voegen of te verwijderen.
