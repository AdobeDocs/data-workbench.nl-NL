---
description: De de lijstvisualisaties van de latentie zijn lijsten die een latentiedimensie omvatten, die een type van afgeleide dimensie is die de tijd meet die sinds een bepaalde gebeurtenis is verstreken.
title: Latentietabellen
uuid: 8081540c-f96c-424e-802d-05d1be5a728d
exl-id: 22f6d52f-e1c2-430a-9e69-3440be0ecdea
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Latentietabellen{#latency-tables}

De de lijstvisualisaties van de latentie zijn lijsten die een latentiedimensie omvatten, die een type van afgeleide dimensie is die de tijd meet die sinds een bepaalde gebeurtenis is verstreken.

U definieert de gebeurtenis door selecties te maken binnen een of meer visualisaties en die selecties in te stellen als de gebeurtenis met de contextmenuoptie Gebeurtenis instellen. De lijsten van de latentie zijn vooral nuttig om activiteit met betrekking tot een campagne of aan een bepaalde klantenorde te volgen waarin u een tijdcorrelatie zoekt.

In [!DNL Site], verstrekken de latentietabellen informatie over de bezoekerszittingen die tot zeven dagen vóór of na de gebeurtenis voorkwamen, maar u kunt latentietabellen vormen om informatie over verschillende telbare en tijddimensies te verstrekken. Zie [Latentietabellen configureren](../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/c-config-ltcy-tbls.md#concept-7175c3defec64556994f0dfcccb7d15c).

Elementen van de bovenliggende dimensie, zoals een sessie, die onderdeel zijn van de specifieke gebeurtenis die u hebt geselecteerd, hebben een latentie van nul. Alle andere elementen krijgen latentie toegewezen die de afstand (in de aangewezen tijddimensie) van de gebeurtenis weerspiegelen.

In het volgende voorbeeld ziet u hoe u de latentietabel kunt gebruiken.

**Waardegebeurtenissen met betrekking tot een campagne identificeren**

Laten we zeggen dat u de activiteiten van klanten gedurende de zeven dagen voor en na de reactie op een bepaalde reclamecampagne wilt volgen. Als u de latentie voor een bepaalde advertentiecampagne wilt bekijken, stelt u de belangencampagne in als de gebeurtenis voor de latentietabel.

De latentie in de werkruimte hieronder is gebaseerd op de selectie van Campagne 11566 (de zittingen in antwoord op deze campagne).

![](assets/vis_Latency.png)

Een vertraging van &quot;+0 dagen&quot; geeft de sessies aan in reactie op Campagne 11566 en alle andere sessies voor dezelfde klanten die op dezelfde dag hebben plaatsgevonden.

Een vertraging van &quot;-2 dagen&quot; identificeert de sessies voor dezelfde klanten die twee dagen voordat de klanten op de campagne reageerden, zijn opgetreden.

Een vertraging van &quot;+7 dagen&quot; geeft de sessies aan voor dezelfde klanten die zeven dagen na hun reactie op de campagne zijn uitgevoerd.

Naast de procedures die in de volgende secties worden vermeld, kunt u alle zelfde taken uitvoeren die u in een lijst kunt uitvoeren, zoals soortelementen, maskerelementen, toevoegen een reeksenlegenda, de uitvoergegevens, etc. Zie [Tabellen](../../../home/c-get-started/c-analysis-vis/c-tables/c-tables.md#concept-c632cb8ad9724f90ac5c294d52ae667f) voor meer informatie.

## Een latentietabel maken {#section-31a03031d9854ef7acc2462d4f37678d}

Als u een latentietabel wilt maken, maakt u eerst een selectie en stelt u vervolgens die selectie in als de gebeurtenis waarvoor u de latentie wilt bijhouden.

1. Klik met de rechtermuisknop in een werkruimte en open de gewenste visualisatie(s), die gebaseerd moet zijn op de aftelbare dimensie die wordt gebruikt om uw latentietabel te configureren.

   In [!DNL Site] moeten de visualisatie(s) bijvoorbeeld op sessies zijn gebaseerd.

1. Open een lege latentietabel.
1. Maak een selectie in uw werkruimte.
1. Klik met de rechtermuisknop in de latentietabel en klik op **[!UICONTROL Set Event]**.

![](assets/vis_Latency_SetEvent.png)

>[!NOTE]
>
>Gebeurtenissen die u selecteert, blijven alleen van kracht als u de selecties opslaat als een latentiedimensie. Zie [Een latentie-Dimension opnieuw gebruiken](../../../home/c-get-started/c-analysis-vis/c-lat-tbls.md#section-29c6483bf9ba476fb1c24ad1df253f46) voor stappen.

## Een latentietabel opnieuw gebruiken {#section-05f741169d204213b6537dce553e4f73}

Als u dezelfde latentietabel opnieuw wilt gebruiken, kunt u de latentietabel lokaal opslaan of als u de juiste machtigingen hebt, kunt u de tabel opslaan op de server zodat alle gebruikers van een bepaald profiel toegang hebben.

**De latentietabel opslaan voor gebruik in andere werkruimten**

1. Klik met de rechtermuisknop op de bovenste rand van de visualisatie en klik op **[!UICONTROL Save]**. Het venster [!DNL Save] verschijnt. De standaardopslaglocatie is de map Gebruiker\*profielnaam*\Work.
1. Typ in het veld [!DNL File name] een beschrijvende naam voor de visualisatie en klik op **[!UICONTROL Save]**.

**De opgeslagen latentietabel ophalen**

1. Klik met de rechtermuisknop in de werkruimte en klik op **[!UICONTROL Open]** > **[!UICONTROL File]**. Het venster [!DNL Open Visualization] verschijnt.
1. Navigeer naar de latentietabel die u hebt opgeslagen.
1. Selecteer het visualisatiebestand voor de latentietabel ( [!DNL *.vw]) en klik op **[!UICONTROL Open]**.

## Een latentiedimensie opnieuw gebruiken {#section-29c6483bf9ba476fb1c24ad1df253f46}

Als u dezelfde latentiedimensie opnieuw wilt gebruiken, kunt u de latentiedimensie lokaal opslaan of als u de juiste machtigingen hebt, kunt u deze opslaan op de server zodat alle gebruikers van een bepaald profiel toegang hebben.

Eventuele latentieafmetingen die u maakt, worden opgeslagen in de map Dimension van het profiel en zijn beschikbaar in de vervolgkeuzelijst [!DNL Change Dimension] in de Data Workbench.

**De latentiedimensie opslaan voor gebruik in andere werkruimten**

1. Klik met de rechtermuisknop op het kolomlabel [!DNL Latency] of op een van de elementen en klik op **[!UICONTROL Save Dimension]**. Het venster [!DNL Save Dimension As] verschijnt.
1. Selecteer of maak de juiste submap in de map Dimension.
1. Typ in het veld [!DNL File name] een beschrijvende naam voor de dimensie (bijvoorbeeld [!DNL Latency for Campaign 11565.dim]) en klik op **[!UICONTROL Save]**.

**De opgeslagen latentiedimensie ophalen**

1. Klik met de rechtermuisknop in de werkruimte en klik op **[!UICONTROL Open]** > **[!UICONTROL File]**. Het venster [!DNL Open Visualization] verschijnt.
1. Navigeer naar de latentie-visualisatie die u hebt opgeslagen in de map Gebruiker\*profile name*\Dimension.
1. Selecteer het bestand met de latentiedimensie ( [!DNL *.dim]) en klik op **[!UICONTROL Open]**.

## Exporteren naar Microsoft Excel {#section-3dffa5c3aab14cdaa40c78b81b08fe53}

Zie [Venstergegevens exporteren](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349) voor informatie over het exporteren van vensters.

## Exporteren naar een TSV-bestand {#section-fd921f351c994ed0a94f63d3bd5b5a87}

Zie [Venstergegevens exporteren](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349) voor informatie over het exporteren van vensters.
