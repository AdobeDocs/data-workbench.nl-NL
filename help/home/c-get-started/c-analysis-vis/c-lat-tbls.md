---
description: De de lijstvisualisaties van de latentie zijn lijsten die een latentiedimensie omvatten, die een type van afgeleide dimensie is die de tijd meet die sinds een bepaalde gebeurtenis is verstreken.
solution: Analytics
title: Latentietabellen
topic: Data workbench
uuid: 8081540c-f96c-424e-802d-05d1be5a728d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Latentietabellen{#latency-tables}

De de lijstvisualisaties van de latentie zijn lijsten die een latentiedimensie omvatten, die een type van afgeleide dimensie is die de tijd meet die sinds een bepaalde gebeurtenis is verstreken.

U bepaalt de gebeurtenis door selecties binnen één of meerdere visualisaties te maken en die selecties te plaatsen als gebeurtenis gebruikend de Vastgestelde optie van het de contextmenu van de Gebeurtenis. De lijsten van de latentie zijn vooral nuttig om activiteit te volgen met betrekking tot een campagne of tot een bepaalde klantenorde waarin u een tijdcorrelatie zoekt.

In [!DNL Site], verstrekken de latentietabellen informatie over de bezoekerszittingen die zo vele zeven dagen vóór of na de gebeurtenis voorkwamen, maar u kunt latentietabellen vormen om informatie over verschillende telbare en tijddimensies te verstrekken. Zie Latentietabellen [configureren](../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/c-config-ltcy-tbls.md#concept-7175c3defec64556994f0dfcccb7d15c).

De elementen van de ouderafmeting, zoals een zitting, die deel van de specifieke gebeurtenis uitmaken die u selecteerde, hebben een latentie van nul. Alle andere elementen worden toegewezen latenties die op de afstand (in de aangewezen tijddimensie) van de gebeurtenis wijzen.

Het volgende voorbeeld illustreert hoe u de latentielijst zou kunnen gebruiken.

**Omgaan met waardegebeurtenissen met betrekking tot een campagne**

Laten we zeggen dat u de activiteiten van klanten wilt volgen in de zeven dagen voor en nadat zij op een bepaalde reclamecampagne hebben gereageerd. Om de latentie voor een bepaalde reclamecampagne te bekijken, zou u de belangencampagne als gebeurtenis voor de latentietabel plaatsen.

De latentie in de werkruimte hieronder is gebaseerd op selectie van Campagne 11566 (de zittingen in antwoord op deze campagne).

![](assets/vis_Latency.png)

Een latentie van &quot;+0 dagen&quot;identificeert de zittingen in antwoord op Campagne 1566, evenals alle andere zittingen voor die zelfde klanten die op de zelfde dag voorkwamen.

Een latentie van &quot;-2 dagen&quot;identificeert de zittingen voor die zelfde klanten die twee dagen voorkwamen alvorens de klanten op de campagne antwoordden.

Een latentie van &quot;+7 dagen&quot;identificeert de zittingen voor die zelfde klanten die zeven dagen plaatsvonden nadat zij op de campagne antwoordden.

Naast de procedures die in de volgende secties worden vermeld, kunt u alle zelfde taken uitvoeren die u in een lijst, zoals soortelementen, maskerelementen kunt uitvoeren, een reeksenlegende, de uitvoergegevens toevoegen, etc. Voor meer informatie, zie [Lijsten](../../../home/c-get-started/c-analysis-vis/c-tables/c-tables.md#concept-c632cb8ad9724f90ac5c294d52ae667f).

## Een latentietabel maken {#section-31a03031d9854ef7acc2462d4f37678d}

Om een latentietabel te creëren, begint u door een selectie te maken, dan plaatsend die selectie als gebeurtenis waarvoor u latentie wilt volgen.

1. Klik met de rechtermuisknop binnen een werkruimte en open de gewenste visualisatie(s), die gebaseerd moet zijn op de aftelbare dimensie die wordt gebruikt om uw latentietabel te configureren.

   Bijvoorbeeld, in [!DNL Site] de visualisatie(s) zou(en) op zittingen-gebaseerd moeten zijn.

1. Open een lege latentietabel.
1. Maak een selectie in uw werkruimte.
1. Klik binnen de latentietabel met de rechtermuisknop aan en klik **[!UICONTROL Set Event]**.

![](assets/vis_Latency_SetEvent.png)

>[!NOTE]
>
>De gebeurtenissen die u selecteert duren niet voort tenzij u sparen de selecties als latentiedimensie. Zie Een [latentiedimensie](../../../home/c-get-started/c-analysis-vis/c-lat-tbls.md#section-29c6483bf9ba476fb1c24ad1df253f46)opnieuw gebruiken voor stappen.

## Hergebruik een latentietabel {#section-05f741169d204213b6537dce553e4f73}

Als u de zelfde latentietabel wilt opnieuw gebruiken, kunt u de latentietabel plaatselijk bewaren of als u de juiste toestemmingen hebt kunt u het aan de server voor alle gebruikers van een bepaald profiel aan toegang bewaren.

**Om de latentietabel op te slaan voor gebruik in andere werkruimten**

1. Klik de hoogste grens van de visualisatie met de rechtermuisknop aan en klik **[!UICONTROL Save]**. Het [!DNL Save] venster wordt weergegeven. De standaardbewaarplaats is de omslag van het Werk van de Gebruiker \*profiel naam* \.
1. Typ in het [!DNL File name] veld een beschrijvende naam voor de visualisatie en klik op **[!UICONTROL Save]**.

**Om de bewaarde latentietabel terug te winnen**

1. Klik binnen de werkruimte met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL File]**. Het [!DNL Open Visualization] venster wordt weergegeven.
1. Navigeer aan de latentielijst die u bewaarde.
1. Selecteer het visualisatiedossier van de latentielijst ( [!DNL *.vw]) en klik **[!UICONTROL Open]**.

## Hergebruik een latentiedimensie {#section-29c6483bf9ba476fb1c24ad1df253f46}

Als u de zelfde latentiedimensie wilt opnieuw gebruiken, kunt u de latentiedimensie plaatselijk bewaren of als u de juiste toestemmingen hebt kunt u het aan de server voor alle gebruikers van een bepaald profiel aan toegang bewaren.

Om het even welke latentiedimensies die u creeert worden bewaard in de folder van de Afmetingen van het profiel en zijn beschikbaar in de [!DNL Change Dimension] drop-down lijst binnen de Werkbank van Gegevens.

**Om de latentiedimensie voor gebruik in andere werkruimten te bewaren**

1. Klik het [!DNL Latency] kolometiket of één van zijn elementen met de rechtermuisknop aan en klik **[!UICONTROL Save Dimension]**. Het [!DNL Save Dimension As] venster wordt weergegeven.
1. Selecteer of creeer de aangewezen subfolder binnen de folder van Afmetingen.
1. Op het [!DNL File name] gebied, typ een beschrijvende naam voor de afmeting (bijvoorbeeld, [!DNL Latency for Campaign 11565.dim]) en klik **[!UICONTROL Save]**.

**Om de bewaarde latentiedimensie terug te winnen**

1. Klik binnen de werkruimte met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL File]**. Het [!DNL Open Visualization] venster wordt weergegeven.
1. Navigeer aan de latentievisualisatie die u in de omslag van de Afmetingen van de Naam van het Profiel \*van de Gebruiker \*opgeslagen.
1. Selecteer het dossier van de latentiedimensie ( [!DNL *.dim]) en klik **[!UICONTROL Open]**.

## Exporteren naar Microsoft Excel {#section-3dffa5c3aab14cdaa40c78b81b08fe53}

Voor informatie over het uitvoeren van vensters, zie het [Uitvoeren van de Gegevens](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349)van het Venster.

## Exporteren naar een TSV-bestand {#section-fd921f351c994ed0a94f63d3bd5b5a87}

Voor informatie over het uitvoeren van vensters, zie het [Uitvoeren van de Gegevens](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349)van het Venster.
