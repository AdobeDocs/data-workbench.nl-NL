---
description: De nieuwe eigenschappen die in Werkbank 6.0.4 van Gegevens worden geïntroduceerd, met inbegrip van insectenmoeilijke situaties en bekende kwesties.
solution: Analytics
title: Data Workbench 6.0 Release Notes
topic: Data workbench
uuid: b348425e-3304-4db7-a280-479a34452bdb
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Data Workbench 6.0 Release Notes

De nieuwe eigenschappen die in Werkbank 6.0.4 van Gegevens worden geïntroduceerd, met inbegrip van insectenmoeilijke situaties en bekende kwesties.

## Nieuwe functies {#section-1225066ea8f44cf68e42e019d0bca816}

De werkbank van gegevens (Inzicht 6.0) omvat deze nieuwe eigenschappen en visualisaties voor toegevoegde rapporteringsmogelijkheden en voorspellende analysehulpmiddelen.

| Functies voor gegevenswerkbanken | Beschrijving |
|---|---|
| [Schaalvisualisatie](../../../home/c-get-started/c-analysis-vis/c-funnel-visualization/c-funnel-visualization.md#concept-79a0854325324bb9a60906cf79ef66da) | De visualisatie van het Kanaal laat u de opeenvolgende processtroom van uw klanten bepalen en verstrekt zicht in de uitval van bezoekers bij elke stap in het proces. |
| [Bezoekersclustering](../../../home/c-get-started/c-analysis-vis/c-visitor-cluster/c-visitor-cluster.md#concept-1c2406ef7b284a56a02daa38eaa2e73d) | Het groeperen van zich laat u hefboomwerking klantenkenmerken om bezoekers dynamisch te categoriseren en clusterreeksen te produceren die op geselecteerde gegevensinput voor klantenanalyse en het richten worden gebaseerd. |
| [Correlatieanalyse](../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-analysis.md#concept-a7c8766b40be43aaa4084612689b630c) | De Analyse van de correlatie laat u snel relevante gegevensverhoudingen identificeren om uw analyse uit te breiden en te verbeteren. |
| [Bijgewerkte Distributie DeviceAtlas](../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-deviceatlas-update.md#concept-28b7bd5c0d854e73834261c431bed1e0) | Het dossier van DeviceAtlas JSON zal nu in een.bundle dossier (anders genoemd .tar.gz) samen met DeviceAtlas.dll en DeviceAtlas64.dll worden verdeeld. |

## Vereisten voor clientupgrade {#section-f316103b48374b6eac77e8feb5c47ecf}

Voltooi deze verbeteringstaken voor de eigenschappen van de gegevenswerkbank (Inzicht 6.0) cliënt:

**Het bijwerken van het .zbin dossier voor de cliënt**

De werkbank van gegevens steunt nu een Redacteur van de Methode van de Input (IME) als secundair proces van de tekstingang dat u toestaat om internationale karakters van uw toetsenbord in te gaan gebruikend een drijvend tekstvakje. De werkbank van gegevens zal Engels door gebrek steunen maar staat u ook toe om andere dossiers te laden om internationale talen, zoals een virtueel Chinees toetsenbord (Pinyin IME) te steunen.

Een nieuw woordenboekdossier (een .zbin dossier) wordt vereist door de cliënttoepassing alvorens aan versie 6.0 bij te werken. U kunt het benodigde .zbin-bestand verkrijgen via het profiel Software en Docs (Softdocs).

Voorwaarden:

* Alvorens aan het Inzicht te bevorderen 6.0 cliënt en Server 6.0 van het Rapport, moet de beheerder van het Inzicht aan Server 6.0 van het Inzicht eerst bevorderen.
* De beheerder van het Inzicht zal een gezoemdossier moeten kiezen dat op taal (en-us.zbin, zh-cn.zbin) wordt gebaseerd, zal het taaldossier kopiëren, dan zal het anders noemen aan insight.zbin, en zal het anders plaatsen genoemd dossier in de wortelfolder van de Server van het Rapport waar uitvoerbaar wordt gevestigd. Dan begin de Server van het Rapport van het Inzicht opnieuw.

Zie de [serverupgradevereisten](../../../home/c-release-notes-insight/release-notes.md) voor aanvullende upgradegegevens aan de serverzijde.

**Om het zbin- dossier voor de cliënt (van versie 5.x aan 6.0 te bevorderen)**

1. Om ervoor te zorgen wordt de cliënt niet bijgewerkt van de Server van het Inzicht tijdens deze verbetering, plaats uw argument Insight.cfg aan vals.

   ```
   Update Software = bool: false
   ```

1. Start de Insight-client opnieuw.
1. Navigeer naar het profiel Software en Docs (SoftDocs-profiel) en download het vereiste **[!UICONTROL Insight.zbin]** bestand: [!DNL Software\Insight Client\v6.00\Insight_6.00.zip]

1. Kopieer het dossier Insight.zbin aan de zelfde omslag zoals het dossier Insight.exe.
1. Om ervoor te zorgen wordt de cliënt van het Inzicht nu bijgewerkt van de Server van het Inzicht, verander het Insight.cfg- dossierargument in waar:

   ```
   Update Software = bool: true
   ```

1. Start de client opnieuw.

   Uw cliënt zal met de server synchroniseren en u zult een bericht zien verklarend dat uw cliënt downloadt. Aan het eind van de download, zult u een bericht krijgen vragend of wilt uw cliënt van het Inzicht opnieuw beginnen.
1. Klik op **OK** om de client opnieuw te starten.

   De client start en upgrade naar versie 6.0.

1. Begin opnieuw de cliënt opnieuw voor de de cliëntsynchronisatie van Insight.zbin om van kracht te worden.

   Als u het volgende bericht krijgt, dan betekent het dat zbin niet in de correcte omslagplaats naast het Insight.exe- dossier werd geplaatst.

   ```
   Insight Terminated: The backup dictionary file insight.zbin 
   is missing.
   ```

   Om de kwestie te verbeteren, schrap Insight.exe en noem de recentste versie van Insight.exe.old aan Insight.exe anders, en begin dan opnieuw met Stap 1 hierboven.

## Serverupgradevereisten {#section-d6edba8b36234957ba8d06b555667a5a}

Voltooi deze verbeteringstaken voor Insight 6.0 servereigenschappen:

**Werk al Server 6.0 van het Inzicht pakketten** bij. Inzicht 6.0 omvat serverpakketten die moeten worden bijgewerkt, met inbegrip van het nieuwe profiel van de Analytics van de Predictive.

>[!IMPORTANT]
>
>Het wordt geadviseerd dat de gebruikers hun serverclusters met verse installaties van Server 6.0 van het Inzicht wanneer het bijwerken bevorderen.

Het wordt ook geadviseerd dat de cliënt hun serverclusters met verse installatie van Server 6.0 van het Inzicht bevordert.

## Servercluster upgraden

**Bereid het taaldossier (.zbin dossier) voor.** De beheerder van het Inzicht selecteert het `<language>.zbin` dossier voor de vereiste taal (bijvoorbeeld: en-us.zbin, zh-cn.zbin) gevestigd in de `/localization/<language>.zbin` omslag. De beheerder kopieert dan het taaldossier en noemt het aan &quot;inzicht.zbin&quot;anders.

Na het voorbereiden van het taaldossier (.zbin), zowel de Cliënt van het Inzicht als de Server van het Rapport moeten worden bijgewerkt. De cliënt van het Inzicht wordt bijgewerkt tijdens het proces [van de](../../../home/c-release-notes-insight/release-notes.md)cliëntverbetering, maar in de meeste gevallen zal de beheerder van het Inzicht de Server van het Rapport bijwerken.

**De Server van het Rapport van de update met een taaldossier (.zbin dossier)**.

Voor alle talen, vereist Server 6.0 van het Rapport het &quot;inzicht.zbin&quot;dossier dat aan de de wortelomslag van de Server van het Rapport wordt gekopieerd.

Werk de de taaldossiers van de Server van het Rapport bij:

1. Voeg het anders genoemde &quot;inzicht.zbin&quot;dossier aan de folder van wortelReportServer toe.
1. Het de configuratiedossier van de Server van het Rapport (reportserver.cfg) vereist doopvontmontages voor dubbel-byte talen. Bijvoorbeeld, vereist het Chinees de toevoeging van doopvonten gebruikend SimSun:

   ```
   Report Server.cfg - Add Fonts 
   
   Fonts = vector: 2 items 
     0 = string: SimSun 
     1 = string: Arial
   ```

1. Een parameter voor Server 6.0 van het Rapport moet in de bevellijn voor localisatie worden overgegaan, bijvoorbeeld:

   ```
   ReportServer.exe -Locale -zh-cn 
   ReportServer.exe -Locale -en-us
   ```

   >[!NOTE]
   >
   >Als een scène niet wordt gespecificeerd, dan blijft de Server van het Rapport aan de taal in het inzicht.zbin- dossier wordt geselecteerd in gebreke.

   Volg de stappen om ReportServer als dienst met de parameters van de Scène te lanceren:

   1. Lanceer een Herinnering van het Bevel als Beheerder.
   1. Navigeer aan ReportServer installeert omslag.
   1. Typ het volgende bevel om de dienst te beginnen:

      * Voor het Engels: [!DNL ReportServer.exe -RegServer -Locale -en-us]
      * Voor Chinees: [!DNL ReportServer.exe -RegServer -Locale -zh-cn]

1. Om te verifiëren als ReportServer met de correcte parameters loopt:

   1. Open Windows Service Manager.
   1. Klik met de rechtermuisknop [!DNL Adobe Insight Report Server - Properties].
   De weg aan uitvoerbaar zal de parameters bevatten:

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```

**Het dossier van de Configuratie van het Profiel voor Predictive Analytics** wijzigen. De beheerder van het inzicht zal het dossier van het douaneprofiel.cfg moeten wijzigen om het Predictive Analytics profiel te omvatten dat in Insight beschikbaar moet zijn.

Voorbeeld van de vermelding profile.cfg:

```
Example ("profile.cfg"): 
Profile = profileInfo:  
  Active = bool: true 
  Directories = vector: 5 items 
    0 = string: Base\\  
    1 = string: Predictive Analytics\\ 
    2 = string: Geography\\ 
    3 = string: Adobe SC\\ 
    4 = string: Custom Profile\\ 
```

**Werk het PAServer.cfg- dossier** bij. Als u Predictive Analytics wilt voorleggen die banen groeperen zich aan de Servers van het Inzicht, dan zult u het PAServer.cfg- dossier voor de behandeling van server-zij groeperende indieningen moeten vormen.

Het douaneprofiel zou PAServer.cfg van het Predictive Analytics profiel (Server\Profiles\Predictive Analytics\Dataset) moeten erven. Vorm en sla PAServer.cfg per uw implementatieplaats op.

>[!NOTE]
>
>Zodra PAServer.cfg wordt gevormd en aan douaneprofiel wordt bewaard, wordt een nieuw begin van de Server van het Inzicht vereist over de plaats.

**De Server van het Rapport van de verbetering.** U zult de doopvonten en de aanloopparameters voor de Server van het Rapport moeten bijwerken.

Voorwaarden:

* Alvorens Server 6.0 van het Rapport te bevorderen, moet de beheerder van het Inzicht eerst aan Server 6.0 van het Inzicht bevorderen.
* Voor alle talen, vereist Server 6.0 van het Rapport de toevoeging van Insight.zbin aan de de wortelomslag van de Server van het Rapport. Zorg ervoor `base/localization/<language>.zbin` wordt gekopieerd en aan &quot;inzicht.zbin&quot;anders genoemd. Kopieer het aan de wortel van de folder van de Server van het Rapport.

Werk de Doopvonten en de parameters van het Begin bij:

1. De Server van het rapport vereist doopvont het plaatsen voor dubbele byte om aan output aan verschillende talen te leiden,

   bijvoorbeeld :

   Rapportserver.cfg - Lettertypen toevoegen

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial
   ```

1. De parameter voor Server 6.0 van het Rapport moet in de bevel-lijn voor localisatiedoeleinden worden overgegaan.

   Om de Server van het Rapport als dienst met de parameters van de Scène te lanceren:

   1. Stop de Dienst van de Server van het Rapport.
   1. Lanceer een Herinnering van het Bevel als Beheerder.
   1. Navigeer aan de Server van het Rapport installeert omslag.
   1. Typ het volgende bevel om de dienst te beginnen:

      ```
      ReportServer.exe -RegServer -Locale -en-us
      ```

Om te verifiëren als de Server van het Rapport met de correcte parameters loopt:

1. Windows Service Manager openen
1. Klik met de rechtermuisknop [!DNL Adobe Insight Report Server - Properties].
1. De weg aan uitvoerbaar zal de parameters bevatten:

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```

**Bevorder het de gegevensvoer van SiteCatalyst voor Inzicht 6.0**. Het filename formaat van het de gegevensvoer van SiteCatalyst voor Inzicht 6.0 is veranderd.

Huidige bestandsindeling:

```
 RSID_YYYYMMDD_HH0000.tsv.gz
```

Nieuwe bestandsindeling:

```
YYYYMMDD-RSID_HH0000.tsv.gz
```

>[!NOTE]
>
>Deze verandering beïnvloedt momenteel geen gebruikers die met de *wbench/van het Centrum* versie van het de gegevensvoer van SiteCatalyst worden opgesteld.

De filename formaatverandering zal voor het volledige gebruik van de de tijdverklaringen van het Begin en van het Eind van het Inzicht tijdens logboekverwerking toestaan. Dit laat het proces toe om te evalueren of zou de inhoud van het dossier, eerder dan filter alle brondossiers moeten worden gelezen gebruikend een rij door rijonderzoek.

In de meeste gevallen, werd een anders noemen proces uitgevoerd na ontvangst van het dossier om het volledige gebruik van dit vermogen te verstrekken. Deze wijziging verstrekt de vereiste noemende overeenkomst door gebrek zonder de behoefte en de overheadkosten van een secundair proces.

Om de nieuwe gegevens te gebruiken SiteCatalyst voer:

1. Bepaal hoe het ontvangende proces het nieuwe filename formaat zal behandelen.

   De norm noemt/beweegt manuscripten die tijdens implementatie worden opgesteld beweegt de dossiers met een &quot;.gz&quot;uitbreiding anders, en voert slechts een nieuwe naam uit als filename het filename formaat met voorafgaande RSID aanpast.

   Het nieuwe filename formaat:

   ```
    YYYYMMDD-RSID_HH0000.tsv.gz
   ```

1. Evalueer de bepaalde van de logboekbron wegen om te bevestigen dat alle dossiers zullen worden gelezen.

   Als u reeds een anders genoemd uitgevoerd manuscript hebt, dan bepaalt u reeds uw logboekbronnen om dit nieuwe filename formaat te lezen.

## Fixes {#section-203f917dd6224114a1f801309c4c2cee}

* Nu, is de belangrijkste combinatie om een werkruimte te verlaten zonder veranderingen te bewaren bijgewerkt aan **[!UICONTROL `<Ctrl>`+`<Backspace>`]**. Eerder, voideerde u veranderingen en sloot een werkruimte door`<Ctrl>`+ te drukken`<Delete>`.

## Gegevens Workbench 6.0.4 Release Notes{#data-workbench-release-notes}

De nieuwe eigenschappen die in Werkbank 6.0.4 van Gegevens worden geïntroduceerd, met inbegrip van insectenmoeilijke situaties en bekende kwesties.

Om vorige eigenschappen en moeilijke situaties te bekijken die voor elke vroegere versie worden gebaseerd, zie de archieven [van de](https://docs.adobe.com/content/help/en/data-workbench/using/release-notes/release-notes.html)versiennota.

## Nieuwe functies {#section-2-1225066ea8f44cf68e42e019d0bca816}

De Werkbank 6.0.4 van gegevens omvat deze nieuwe eigenschappen en visualisaties voor toegevoegde rapporteringsmogelijkheden en voorspellende analysehulpmiddelen.

**Propensity Scoring visualisatie**. De werkbank van gegevens berekent scores voor elke bezoeker als geschatte waarschijnlijkheid dat een gespecificeerde gebeurtenis kan gebeuren. De bezoeker die visualisatie scant staat u toe om een scoredimensie tot stand te brengen die een waarschijnlijkheid van een gespecificeerde gebeurtenis voor elke bezoeker van belang geeft die op de inputvariabelen wordt gebaseerd.

![](assets/visitor_scoring_visual.png)

Zie [Waarschuwing](../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-visitor-propensity.md#concept-2958f4640dd44b9d86ad51c4f6165f40) voor meer informatie over deze functie.

## Upgradevereisten {#section-08bd6fe3da8740fcb19688e8cac6f223}

**Logbron-ID moet worden gedefinieerd**. Beginnend in versie 6.04, als identiteitskaart van de Bron van het Logboek niet wordt bepaald dan zult u de volgende fout krijgen:

```
Missing Log Souce ID in log processing.cfg. Log Source ID must be  
defined for all log sources.
```

De opname van Rijen per de Bron van het Logboek werd toegevoegd in Werkbank 6.0 van Gegevens en kan in het Logboek van het douaneprofiel worden bepaald Processing.cfg door een uniek genoemde identiteitskaart van de Bron van het Logboek toe te voegen. Als u een lege Van het Bron logboek identiteitskaart hebt, dan kon u de kwesties van de Verwerking van het Logboek zoals onvolledige lezing van de logboekbrongegevens en andere discrepanties zien.

```
Log Processing.cfg 
Log Sources = vector: 2 items 
  0 = VisualSensor: 
    Compressed = bool: false 
    Log Paths = vector: 1 items 
      0 = Path: \some path\ 
    Log Server = serverInfo:  
      Address = string:  
      Name = string:  
      Port = int: 80 
      Proxy Address = string:  
      Proxy Password = string:  
      Proxy Port = int: 8080 
      Proxy User Name = string:  
      SSL Client Certificate = string: Certificates\\server_cert.pem 
      SSL Server Common Name = string:  
      Use SSL = bool: false 
     
Log Source ID = string: <Name your ID Here>
    Name = string:  
    Recursive = bool: false
```

**Capaciteit om de Middelen van FSU te delegeren**

In [!DNL Profiles/`<profilename>`/dataset/Cluster.cfg], kunt u de afzonderlijke Eenheden van de Server van het Dossier (FSU) voor Normalize en BronLijst nu specificeren servers. Deze diensten zijn niet langer gebonden aan de Master FSU.

>[!NOTE]
>
>Als de Server van de Lijst niet wordt gespecificeerd, dan zal de Server van de Lijst de Normalize de configuratiemontages van de Server erven.

Voorbeeld in het [!DNL cluster.cfg] dossier.

```
Cluster = ClusterConfig: 
  Normalize Server = serverInfo: 
    Address = string: normalizeserver.domain.com 
    Port = int: 80 
    Use SSL = bool: false 
  List Server = serverInfo: 
    Address = string: sourcelistserver.domain.com 
    Port = int: 80 
    Use SSL = bool: false
```

## Vaste hulzen {#section-3b4b85a35f534288adf8a5246ef028cc}

* In Werkbank 6.0 van Gegevens, steunden de Matrijs van de Correlatie en de Bouwer van de Cluster geen Compute in Achtergrond. Dit is nu vastgelegd in versie 6.0.4.
* Eerder, als u een selectie op de Funnel had en een stap verwijderde, kon een toegangsschending voorkomen. Dit is opgelost.
* Vast een potentiële sluitingsvoorwaarde in de Uitvoer van het Segment die problemen onder zware ladingsvoorwaarden kan veroorzaken.
