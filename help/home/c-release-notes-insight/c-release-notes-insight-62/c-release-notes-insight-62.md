---
description: De werkbank 6.2 van gegevens de versienota's omvatten nieuwe eigenschappen, verbeteringsvereisten, insectenmoeilijke situaties, en bekende kwesties.
title: Data Workbench 6.2 Release Notes
uuid: 8631c936-d53b-493d-9f58-72f541c3ddce
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Data Workbench 6.2 Release Notes{#data-workbench-release-notes}

De werkbank 6.2 van gegevens de versienota&#39;s omvatten nieuwe eigenschappen, verbeteringsvereisten, insectenmoeilijke situaties, en bekende kwesties.

## Nieuwe functies {#section-1225066ea8f44cf68e42e019d0bca816}

De Werkbank 6.2 van gegevens omvat deze nieuwe eigenschappen:

| Kenmerken | Beschrijving |
|--- |--- |
| Beslissingsbomen | Beslissingsbomen zijn een voorspellende beeldvorming die wordt gebruikt om de kenmerken en relaties van de bezoeker te evalueren. De bouwer van de Boom van de Beslissing produceert een visualisatie van de beslissingsboom die op een gespecificeerd positief geval en een reeks input wordt gebaseerd. |
| Update naar Binair Filter in de Matrix van de Correlatie | De Binaire Filter is bijgewerkt met nieuwe eigenschappen, die u vereisen om het even welke Matrijs van de Correlatie met een Binaire Filter te herbouwen die in vorige versies wordt gebouwd. |
| Dichtheid-kaart | De dichtheidskaart is een visualisatie die elementen als gearceerde rechthoeken binnen een vierkante kaart toont. |
| Attributieprofiel | Om attributiewaarden (gebeurtenissen om verantwoordelijkheid voor een succesvolle omzetting of verkoop toe te schrijven) snel te analyseren, verstrekt de Werkbank van Gegevens een op regels-gebaseerd profiel van de Attributie met eigenschappen voor de Architect aan opstelling de rapporten van de Attributie en de Analyst om de rapporten in werking te stellen. |
| Analytische rapporten | De malplaatjes van het rapport standaardiseren de rapporten van de Analyse van Adobe voor gebruikers van de gegevenswerkbank die het profiel van Adobe SC gebruiken. Deze rapporten zijn identiek aan rapporten die in de Rapporten van de Marketing &amp; Analytics (vroeger SiteCatalyst) worden gebruikt. |
| 3D-sccatterpercelen | Een 3D Plot van de Drager grafieken de elementen van een gegevensdimensie (zoals Dagen of de Plaats van de Verwijzing) op een driedimensionaal net waar de x, y, en z assen diverse metriek vertegenwoordigen. |


## Updates voor UI-updates voor datacWorkbench-client{#data-workbench-client-ui-updates}

Werkbank 6.2 van gegevens omvat nieuwe gebruikersinterfaceupdates aan het bladwijzerpaneel, nieuwe pictogrammen in de werkruimtekoolbar, de capaciteit om de werkruimte binnen het scherm te slepen, nieuwe snelle sleutels, en updates aan de visualisatie van het cirkeldiagram.

## Nieuwe bladwijzekenmerken {#section-e361b605441540ca8213c3fddb5e0718}

U kunt bladwijzer significante werkruimten nu snel tussen visualisaties en rapporten bewegen die in uw werkschema worden gebruikt.

**Werken met bladwijzers**

1. Referentie een werkruimte door het pictogram van de Referentie ![](assets/bookmark_icon.png) in de hogere juiste hoek van de toolbar te klikken.
1. Klik **[!UICONTROL Add]** > **[!UICONTROL Bookmarks Panel]** in de linkerruit om een lijst van referenties te openen.

   ![](assets/bookmarks_panel.png)

1. Om een bookmark werkruimte te openen, klik een werkruimtenaam in **[!UICONTROL Bookmark Panel]**.

   ![](assets/bookmarks_panel_left.png)

   De geselecteerde werkruimte wordt geopend. Wanneer u op een andere werkruimte met favorieten klikt, wordt de vorige werkruimte gesloten en wordt de nieuw geselecteerde werkruimte geopend, zodat u snel door uw werkstroom kunt navigeren.

**Een bladwijzer verwijderen:**

* In het Comité van de Referentie, klik en selecteer **[!UICONTROL verwijderen met de rechtermuisknop aan<bookmark title>]**om een geselecteerde referentie te schrappen, of te selecteren **[!UICONTROL Clear All Bookmarks]**om alle referenties te schrappen.

* U kunt ook op de werkruimte in de duimnagelmening binnen de werktop met de rechtermuisknop klikken en selecteren **[!UICONTROL Clear Bookmark]**.

>[!IMPORTANT]
>
>* 25 bladwijzers kunnen worden opgeslagen.
>* Als u een referentie toevoegt en dan de plaats van de werkruimte beweegt, zal de referentie ongeldig zijn en moet van het Comité van de Referentie worden geschrapt en worden teruggesteld.
>



## Nieuwe pictogrammen in werkruimte {#section-c108bbd1661249e79c146727ff3d2470}

De Werkbank 6.2 van gegevens vervangt nu de tekst in de werkruimte met pictogrammen. U kunt nog over hangen en het bericht van het hulpmiddeluiteinde zien identificerend het pictogram, met inbegrip van, **[!UICONTROL File]**, **[!UICONTROL Add]** en **[!UICONTROL Export]**.

![](assets/new_icons.png)

Een nieuw **[!UICONTROL Help]** pictogram wordt toegevoegd om tot de documentatie en andere kenniscentra, met inbegrip van de volgende verbindingen toegang te hebben:

<table id="table_64BBC67B1BB44B1197FF7E5E7B067696"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Documentkoppelingen </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Marketingrapporten en -analyses </td> 
   <td colname="col2">Open aan de de <span class="uicontrol"> Hulp pagina van de Rapporten &amp; van de Analyse</span> van Adobe van de Marketing van de Rapporten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ideëenuitwisseling </td> 
   <td colname="col2">Open aan login <span class="uicontrol"> van de Uitwisseling van</span>Ideeën. Dit online portaal staat gebruikers toe om updateveranderingen en verbeteringsideeën aan gegevenswerkbank te verstrekken. Deze klant-gerichte ideeën kunnen dan door alle gebruikers worden gestemd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hulp </td> 
   <td colname="col2">Open de documentatie <span class="uicontrol"> van de Werkbank van</span>Gegevens. <p>U kunt <span class="uicontrol"> &lt;F1&gt;</span> ook drukken om hulp binnen een werkruimte te openen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Informatie </td> 
   <td colname="col2">Open om de <span class="uicontrol"> cliëntversie</span> van gegevenswerkbank te identificeren. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>U kunt ook drukken `<F1>` om de documentatie van een werkruimte te openen.

## Werkruimteweergaven slepen {#section-9129c340c21d45a3864c923884cd4382}

Als een werkruimte groter is dan het viewable scherm, kunt u de mening bewegen om alle elementen binnen de werkruimte te zien. U kunt op de achtergrond (buiten de visualisaties en lijsten) klikken en het scherm slepen om het viewable gebied binnen de werkruimte te bewegen. De curseur zal in een handpictogram veranderen wanneer het slepen van de mening binnen het werkruimtekader.

![](assets/drag_workspace.png)

## Sneltoetsen om werkruimteweergaven te wijzigen {#section-d8322f72423f437aa2e34f2188b1341c}

De nieuwe snelle sleutels laten u resize en werkruimten tussen venster en volledige paginameningen aanpassen.

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
   <td colname="col1"><b>Volledige het schermmening</b>. De werkruimte vult het scherm en past aan de nieuwe grootte terug. </td> 
   <td colname="col2"><b>Ctrl plus</b> <p>CTRL + (op toetsenbord) </p> <p><i>of</i> </p> <p>Ctrl Shift + (op toetsenbord) </p> </td> 
   <td colname="col3"> 
    <ul id="ul_C7C731B894D946D9916F50806F015857"> 
     <li id="li_452B4C119B1A40038A408CFFC53653A9">Bestand &gt; Paginaformaat &gt; Scherm vullen <p><i>gevolgd door</i> </p> </li> 
     <li id="li_DE9B8B31B9F24A6AA68A1D0DB886B501">Bestand &gt; Werkruimte verfijnen </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>De mening</b>van het venster. De vertoningen van de werkruimte in een standaardvenstermening en passen aan de nieuwe grootte terug. </td> 
   <td colname="col2"><b>Ctrl min</b> <p>Ctrl - </p> </td> 
   <td colname="col3"> 
    <ul id="ul_3474B9EFD69343C09BC84E485D896C28"> 
     <li id="li_820BAED76FF24A5785E6D89C5C692DD5">Bestand &gt; Paginagrootte &gt; Standaard <p><i>gevolgd door</i> </p> </li> 
     <li id="li_337789F282CE4C2C990C67B115782454">Bestand &gt; Werkruimte verfijnen </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Bug Fixes {#section-8704a9ac358246cd81233dd0982d534f}

* Bijgewerkt het Visuele de raadplegingsdossier van de Plaats om de veranderingen van de onderzoeksmotor in de termijn van het vraagonderzoek te richten.
* Vast onnauwkeurige foutenmelding, &quot;er is niet in geslaagd werkruimte&quot;in te voeren, wanneer het invoeren van een werkruimte in het cliëntwerkstation alhoewel de invoer succesvol was.
* De fout van de werkstationverbinding die &quot;412 het bericht van het Conflict van de Configuratie&quot;toont wordt nu vervangen met gebruikersvriendelijk bericht dat systeemactie identificeert.
* Het &quot;post&quot;bevel kan nu in de Server van het Rapport worden uitgevoerd.
* Vaste gebruikersinterfacefouten in cliëntgebruikersinterface voor Vereenvoudigd Chinees.
* De Analyse van Adobe werkte de gegevensvoer bij dat de Werkbank van machtsgegevens om uit Profielen en Publiek voordeel te halen dat met de Wolk van de Ervaring van Adobe integreert. Alle gebruikers van de Werkbank van Gegevens moesten hun milieu voor deze overgang uiterlijk 21 april 2014 voorbereiden.

   De profielen en het Publiek werden geïntroduceerd om een volledige mening van klanten over de Analyse van Adobe te verstrekken. Deze nieuwe dienst is beschikbaar binnen de Wolk van de Ervaring van Adobe om verdere waarde over analysehulpmiddelen te drijven beginnen de stichting voor deze eigenschappen binnen Analytics te vestigen. De nieuwe Experience Cloud Bezoeker-id wordt toegevoegd aan de gegevensinvoer, samen met andere verbeteringen en verbeteringen om zich aan te passen aan de nieuwe gegevensinvoer en de wereldwijde bezoekersidentificatie.
* Wanneer het invoeren van een werkruimte, wordt een foutenmelding getoond alhoewel de invoer succesvol was.

## Upgradevereiste {#section-3cc74d08f7454d698b5a6d3f1dcde282}

* Het profiel van de Attributie wordt gevormd voor gebruikers die het profiel van Adobe SC hebben uitgevoerd om het de gegevensvoer van de Analytics (SC/Insight) aan te wenden. Door gebrek, worden de de Marketing en gebeurtenissen van de Omzetting gebruikt als standaardinteractie die in de op regels-gebaseerde modellen wordt geëvalueerd.
* Voor gebruikers van de het profielbevordering van Adobe SC aan Werkbank 6.2 van Gegevens, als u niet de standaardconfiguraties gebruikt, verifieer dat de [!DNL x-bot_id] waarde in het [!DNL SC Fields.cfg] dossier behoorlijk wordt gedecodeerd en dat het [!DNL x-bot_id] gebied behoorlijk in de [!DNL Decoding Instructions.cfg] en de [!DNL Exclude Hit.cfg] dossiers vermeld is. Dit zal slechts een kwestie zijn als u het configuratiedossier van de standaardconfiguratie hebt gewijzigd.

* Als u ongebruikte gebieden in **[!UICONTROL Dataset]** > **[!UICONTROL het Verwerkingsdossier van het Logboek >** **[!DNL SC Fields.cfg]** voor het profiel van Adobe SC hebt geschrapt, zult u moeten bijwerken om bijgewerkte gebiedswaarden aan te passen die voor het profiel van de Attributie worden gebruikt.

## Bekende problemen {#section-dbb307639835493a83409f5f461932b8}

* Wanneer de 3D Visualisatie van het Plot van de Scatter callouts omvat, kan het gezoem percelen buiten de grens van de visualisatie tonen.

   Werkruimte: Zoem eerst het 3D Plot van de Scatter en voeg dan callouts aan uw visualisatie toe.
* Het slepen metrisch van het paneel van Vinden aan de Strische Legende buiten de metrische kolom zal de Statische Legende van de werkruimte schrappen.

   Werkruimte: De gebruikers die wensen om metriek aan de Metrische Legende te slepen zouden in de eerste kolom (metriekkolom) moeten vallen.
* De Werkruimte van de druk die Sidebar en Beide opties gebruiken zal niet de informatie van Copyright op de gedrukte pagina omvatten.
* Het gebruiken van Werkstation in verre Desktopzitting zal vertragen wanneer het anders noemen van werkruimten.
* (In Vereenvoudigde Chinese versie) De daadwerkelijke rapportoutput is geldig in de Server van het Rapport maar e-mail onderwerplijnen en de namen van het gehechtheidsdossier worden verdrievoudigd.
* (In Vereenvoudigde Chinese versie) Wanneer het gebruiken van woordomslag in de visualisatie van het Aantekenvel, worden de gelokaliseerde woorden niet correct verpakt resulterend in troepenkarakters die aan het koord worden toegevoegd.
* (In Vereenvoudigde Chinese versie) Kan Insight.exe niet starten als de installatiefolder met niet-Engelse tekens is benoemd.

   Werkruimte: Houd standaardnamen of noem het gebruiken van slechts Engelse karakters in de omslagweg anders om uitvoerbare lijsten te lanceren.

