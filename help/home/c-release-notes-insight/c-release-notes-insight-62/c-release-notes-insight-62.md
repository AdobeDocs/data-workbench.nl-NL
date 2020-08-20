---
description: Data Workbench 6.2 de versienota's omvat nieuwe eigenschappen, verbeteringsvereisten, insectenmoeilijke situaties, en bekende kwesties.
title: Opmerkingen bij de release Data Workbench 6.2
uuid: 8631c936-d53b-493d-9f58-72f541c3ddce
translation-type: tm+mt
source-git-commit: a276b16565634fea9b693206c8a55b528fada977
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 0%

---


# Opmerkingen bij de release Data Workbench 6.2{#data-workbench-release-notes}

Data Workbench 6.2 de versienota&#39;s omvat nieuwe eigenschappen, verbeteringsvereisten, insectenmoeilijke situaties, en bekende kwesties.

## New Features {#section-1225066ea8f44cf68e42e019d0bca816}

Data Workbench 6.2 bevat de volgende nieuwe functies:

| Functies | Beschrijving |
|--- |--- |
| Beslissingsbomen | Beslissingsbomen zijn een voorspellende analytische visualisatie die wordt gebruikt om de kenmerken en relaties van bezoekers te evalueren. De opbouwfunctie voor beslissingsstructuur genereert een visualisatie van de beslissingsstructuur op basis van een opgegeven positief geval en een reeks ingangen. |
| Bijwerken naar binair filter in correlatiematrix | Het Binaire Filter is bijgewerkt met nieuwe eigenschappen, die u vereisen om het even welke Matrijs van de Correlatie met een Binair die Filter te herbouwen in vorige versies wordt gebouwd. |
| Dichtheid-overzicht | De dichtheidskaart is een visualisatie die elementen als gearceerde rechthoeken binnen een vierkante kaart toont. |
| Attributieprofiel | Om attributiewaarden (gebeurtenissen aan attributenverantwoordelijkheid voor een succesvolle omzetting of verkoop) snel te analyseren, verstrekt de Data Workbench een op regels-gebaseerd profiel van de Attributie met eigenschappen voor de Architect aan opstelling de rapporten van de Attributie en de Analyst om de rapporten in werking te stellen. |
| Analytische rapporten | Rapportsjablonen standaardiseren Adobe Analytics-rapporten voor gebruikers van de gegevenswerkbank die gebruikmaken van het Adobe SC-profiel. Deze rapporten zijn identiek aan rapporten die in Marketingrapporten &amp; Analytics (vroeger SiteCatalyst) worden gebruikt. |
| 3D-verstrooiingspunten | Een 3D-spreidingsgrafiek geeft de elementen van een gegevensdimensie (zoals dagen of Referral-site) weer op een driedimensionaal raster waar de x-, y- en z-as verschillende metriek vertegenwoordigen. |


## UI-updates Data Workbench Client{#data-workbench-client-ui-updates}

Data Workbench 6.2 bevat nieuwe updates van de gebruikersinterface naar het venster Bladwijzers, nieuwe pictogrammen in de werkruimtentoolbar, de mogelijkheid om de werkruimte binnen een scherm te slepen, nieuwe sneltoetsen en updates voor de visualisatie van het cirkeldiagram.

## Nieuwe bladwijzerfuncties {#section-e361b605441540ca8213c3fddb5e0718}

U kunt nu bladwijzers maken voor belangrijke werkruimten, zodat u snel kunt schakelen tussen visualisaties en rapporten die in uw workflow worden gebruikt.

**Werken met bladwijzers**

1. U kunt een werkruimte bladwijzer maken door op het pictogram Bladwijzer ![](assets/bookmark_icon.png) in de rechterbovenhoek van de werkbalk te klikken.
1. Klik op **[!UICONTROL Add]** > **[!UICONTROL Bookmarks Panel]** in het linkervenster om een lijst met bladwijzers te openen.

   ![](assets/bookmarks_panel.png)

1. Als u een werkruimte met bladwijzer wilt openen, klikt u op de naam van een werkruimte in de **[!UICONTROL Bookmark Panel]** werkruimte.

   ![](assets/bookmarks_panel_left.png)

   De geselecteerde werkruimte wordt geopend. Wanneer u op een andere werkruimte met bladwijzer klikt, wordt de vorige werkruimte gesloten en wordt de nieuwe geselecteerde werkruimte geopend, zodat u snel door de workflow kunt navigeren.

**Een bladwijzer verwijderen:**

* Klik in het venster Bladwijzer met de rechtermuisknop en selecteer **[!UICONTROL Verwijderen<bookmark title>]**als u een geselecteerde bladwijzer wilt verwijderen of alle bladwijzers wilt verwijderen.**[!UICONTROL Clear All Bookmarks]**

* U kunt ook met de rechtermuisknop op de werkruimte in de miniatuurweergave in de werkbalk klikken en selecteren **[!UICONTROL Clear Bookmark]**.

>[!IMPORTANT]
>
>* U kunt 25 bladwijzers opslaan.
>* Als u een bladwijzer toevoegt en vervolgens de locatie van de werkruimte verplaatst, is de bladwijzer ongeldig en moet deze worden verwijderd uit het venster Bladwijzer en opnieuw worden ingesteld.

>



## Nieuwe pictogrammen in werkruimte {#section-c108bbd1661249e79c146727ff3d2470}

Data Workbench 6.2 vervangt nu de tekst in de werkruimte door pictogrammen. U kunt de aanwijzer nog steeds boven het knopinfo-bericht plaatsen en het pictogram, inclusief **[!UICONTROL File]**, **[!UICONTROL Add]** en **[!UICONTROL Export]**.

![](assets/new_icons.png)

Er wordt een nieuw **[!UICONTROL Help]** pictogram toegevoegd voor toegang tot de documentatie en andere kenniscentra, waaronder de volgende koppelingen:

<table id="table_64BBC67B1BB44B1197FF7E5E7B067696"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Documentatiekoppelingen </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Marketingrapporten en -analyses </td> 
   <td colname="col2">Open op de Help-pagina <span class="uicontrol"> Adobe Marketing Reports &amp; Analytics</span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Idea Exchange </td> 
   <td colname="col2">Open aan login <span class="uicontrol"> van de Uitwisseling van</span>Ideeën. Met dit online portaal kunnen gebruikers updates en verbeteringsideeën aanbieden aan de werkbank van gegevens. Deze klant-gerichte ideeën kunnen dan door alle gebruikers worden gestemd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Help </td> 
   <td colname="col2">Open de documentatie <span class="uicontrol"> van de</span>Data Workbench. <p>U kunt ook op <span class="uicontrol"> &lt;F1&gt;</span> drukken om de Help in een werkruimte te openen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Info </td> 
   <td colname="col2">Openen om de <span class="uicontrol"> clientversie</span> van de gegevenswerkbank te identificeren. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>U kunt ook drukken `<F1>` om de documentatie van een werkruimte te openen.

## Weergaven werkruimte slepen {#section-9129c340c21d45a3864c923884cd4382}

Als een werkruimte groter is dan het zichtbare scherm, kunt u de weergave verplaatsen om alle elementen in de werkruimte weer te geven. U kunt op de achtergrond klikken (buiten de visualisaties en tabellen) en het scherm slepen om het zichtbare gebied binnen de werkruimte te verplaatsen. De cursor verandert in een handje wanneer u de weergave binnen het werkruimteframe sleept.

![](assets/drag_workspace.png)

## Sneltoetsen om werkruimtweergaven te wijzigen {#section-d8322f72423f437aa2e34f2188b1341c}

Met de nieuwe sneltoetsen kunt u de grootte en de grootte van de werkruimten wijzigen tussen de weergaven van vensters en volledige pagina&#39;s.

<table id="table_A01C514C99F043338D183A6839E03DEA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Opdrachten </th> 
   <th colname="col2" class="entry"> Sneltoetsen </th> 
   <th colname="col3" class="entry"> Gecombineerde menuopdrachten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><b>Volledige schermweergave</b>. De werkruimte vult het scherm en past de nieuwe grootte aan. </td> 
   <td colname="col2"><b>Ctrl plus</b> <p>Ctrl + (op toetsenblok) </p> <p><i>of</i> </p> <p>Ctrl Shift + (op toetsenbord) </p> </td> 
   <td colname="col3"> 
    <ul id="ul_C7C731B894D946D9916F50806F015857"> 
     <li id="li_452B4C119B1A40038A408CFFC53653A9">Bestand &gt; Paginaformaat &gt; Scherm vullen <p><i>gevolgd door</i> </p> </li> 
     <li id="li_DE9B8B31B9F24A6AA68A1D0DB886B501">Bestand &gt; Werkruimte verfijnen </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Vensterweergave</b>. De werkruimte wordt weergegeven in een standaardvensterweergave en krijgt de nieuwe grootte. </td> 
   <td colname="col2"><b>Ctrl min</b> <p>Ctrl - </p> </td> 
   <td colname="col3"> 
    <ul id="ul_3474B9EFD69343C09BC84E485D896C28"> 
     <li id="li_820BAED76FF24A5785E6D89C5C692DD5">Bestand &gt; Paginaformaat &gt; Standaard <p><i>gevolgd door</i> </p> </li> 
     <li id="li_337789F282CE4C2C990C67B115782454">Bestand &gt; Werkruimte verfijnen </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Opgeloste problemen {#section-8704a9ac358246cd81233dd0982d534f}

* Bijgewerkt het Visuele de raadplegingsdossier van de Plaats om de veranderingen van de onderzoeksmotor in de termijn van het vraagonderzoek te richten.
* Correctie van onjuist foutbericht &quot;Kan werkruimte niet importeren&quot; bij het importeren van een werkruimte in het clientwerkstation, ook al is het importeren gelukt.
* De fout van de de verbindingsfout van het werkstation die het bericht &quot;412 van het Conflict van de Configuratie&quot;toont wordt nu vervangen met gebruikersvriendelijk bericht dat systeemactie identificeert.
* Het &quot;post&quot;bevel kan nu in de Server van het Rapport worden uitgevoerd.
* Fouten in gebruikersinterface van client voor Vereenvoudigd Chinees opgelost.
* Adobe Analytics heeft de gegevensfeed bijgewerkt die Data Workbench in staat stelt gebruik te maken van profielen en soorten publiek die kunnen worden geïntegreerd met de Adobe Experience Cloud. Alle gebruikers van de Data Workbench moesten hun omgeving voor deze overgang voor 21 april 2014 voorbereiden.

   Profielen en soorten publiek zijn geïntroduceerd om een volledige weergave van klanten in Adobe Analytics te bieden. Deze nieuwe service is beschikbaar in de Adobe Experience Cloud om meer waarde te bieden aan alle analytische hulpmiddelen en de basis voor deze functies in Analytics te leggen. De nieuwe bezoeker-id van de Experience Cloud wordt toegevoegd aan de gegevensfeed, samen met andere verbeteringen en verbeteringen om aan te passen aan de nieuwe gegevensfeed en de algemene bezoeker-id.
* Tijdens het importeren van een werkruimte wordt een foutbericht weergegeven, ook al is het importeren gelukt.

## Upgrade vereist {#section-3cc74d08f7454d698b5a6d3f1dcde282}

* Het attributieprofiel is geconfigureerd voor gebruikers die het Adobe SC-profiel hebben geïmplementeerd, zodat ze de gegevensfeed Analytics (SC/Insight) kunnen gebruiken. Door gebrek, worden de de Marketing en gebeurtenissen van de Omzetting gebruikt als standaardinteractie die in op regel-gebaseerde modellen wordt geëvalueerd.
* Voor gebruikers van het Adobe SC-profiel dat een upgrade uitvoert naar Data Workbench 6.2 en u de standaardconfiguraties niet gebruikt, controleert u of de [!DNL x-bot_id] waarde in het [!DNL SC Fields.cfg] bestand correct wordt gedecodeerd en of het [!DNL x-bot_id] veld op de juiste wijze wordt weergegeven in de bestanden [!DNL Decoding Instructions.cfg] en in de [!DNL Exclude Hit.cfg] bestanden. Dit zal slechts een kwestie zijn als u het configuratiedossier van de standaardconfiguratie hebt gewijzigd.

* Als u ongebruikte velden in het bestand **[!UICONTROL Dataset]** > **[!UICONTROL Log Processing]** > **[!DNL SC Fields.cfg]** voor het Adobe SC-profiel hebt verwijderd, moet u de gegevens bijwerken om de bijgewerkte veldwaarden voor het kenmerk te kunnen gebruiken.

## Bekende problemen {#section-dbb307639835493a83409f5f461932b8}

* Wanneer de Visualisatie van het Plot 3D van de Spreiding callouts omvat, kan het gezoem percelen buiten de grens van de visualisatie tonen.

   Oplossing: Zoom eerst het 3D-spotje in en voeg vervolgens callouts toe aan uw visualisatie.
* Als u de metrische waarde van het deelvenster Finders naar de metrische legenda buiten de metrische kolom sleept, wordt de metrische legenda uit de werkruimte verwijderd.

   Oplossing: Gebruikers die metriek naar Metrische legenda willen slepen, moeten in de eerste kolom (kolom Metriek) neerzetten.
* De werkruimte voor afdrukken met gebruik van de zijbalk en beide opties bevatten geen copyrightinformatie op de afgedrukte pagina.
* Het gebruik van Workstation in een externe desktopsessie loopt vast bij het wijzigen van de naam van werkruimten.
* (In de Vereenvoudigde Chinese versie) Werkelijke rapportuitvoer is geldig in de Server van het Rapport maar de e-mailonderwerpregel en de namen van gehechtheidsdossiers zijn verstoord.
* (In de versie Vereenvoudigd Chinees) Wanneer tekstomloop wordt gebruikt in de werkbladvisualisatie, worden gelokaliseerde woorden niet correct omwikkeld, wat leidt tot ongewenste tekens die aan de tekenreeks worden toegevoegd.
* (In de versie Vereenvoudigd Chinees) Insight.exe kan niet worden gestart als de installatiemap een naam heeft met niet-Engelse tekens.

   Oplossing: Bewaar standaardnamen of wijzig de naam met alleen Engelse tekens in het mappad om uitvoerbare bestanden te starten.

