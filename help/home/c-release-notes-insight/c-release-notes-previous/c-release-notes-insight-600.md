---
description: Nieuwe functies die zijn geïntroduceerd in Data Workbench 6.0.4, waaronder opgeloste problemen en bekende problemen.
title: Opmerkingen bij de release Data Workbench 6.0
uuid: b348425e-3304-4db7-a280-479a34452bdb
exl-id: be69b3be-24e7-4a8c-9dc8-1360a9b6fb3a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1679'
ht-degree: 0%

---

# Opmerkingen bij de release Data Workbench 6.0

Nieuwe functies die zijn geïntroduceerd in Data Workbench 6.0.4, waaronder opgeloste problemen en bekende problemen.

## Nieuwe functies {#section-1225066ea8f44cf68e42e019d0bca816}

De werkbank van gegevens (Insight 6.0) omvat deze nieuwe eigenschappen en visualisaties voor toegevoegde rapporteringsmogelijkheden en voorspellende analysehulpmiddelen.

| Data Workbench-functies | Beschrijving |
|---|---|
| [Trechter visualisatie](../../../home/c-get-started/c-analysis-vis/c-funnel-visualization/c-funnel-visualization.md#concept-79a0854325324bb9a60906cf79ef66da) | De visualisatie van het Kanaal laat u de opeenvolgende processtroom van uw klanten bepalen en verstrekt zicht in de reserve van bezoekers bij elke stap in het proces. |
| [Bezoekersclustering](../../../home/c-get-started/c-analysis-vis/c-visitor-cluster/c-visitor-cluster.md#concept-1c2406ef7b284a56a02daa38eaa2e73d) | Met clustering kunt u klantkenmerken gebruiken om bezoekers dynamisch te categoriseren en clustersets te genereren op basis van geselecteerde gegevensinvoer voor analyse en doelgerichtheid van klanten. |
| [Correlatieanalyse](../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-analysis.md#concept-a7c8766b40be43aaa4084612689b630c) | Met Correlatieanalyse kunt u snel relevante gegevensrelaties identificeren om uw analyse uit te breiden en te verbeteren. |
| [Bijgewerkte DeviceAtlas-distributie](../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-deviceatlas-update.md#concept-28b7bd5c0d854e73834261c431bed1e0) | Het DeviceAtlas JSON-bestand wordt nu samen met DeviceAtlas.dll en DeviceAtlas64.dll gedistribueerd in een .bundle-bestand (een hernoemd .tar.gz). |

## Vereisten voor upgrade van client {#section-f316103b48374b6eac77e8feb5c47ecf}

Voltooi deze verbeteringstaken voor gegevens werkbank (Insight 6.0) cliënteigenschappen:

**Het .zbin-bestand voor de client bijwerken**

De werkbank Gegevens ondersteunt nu een invoermethode-editor (IME) als een secundair tekstinvoerproces waarmee u internationale tekens van het toetsenbord kunt invoeren met behulp van een zwevend tekstvak. De werkbank voor gegevens biedt standaard ondersteuning voor Engels, maar u kunt ook andere bestanden laden die internationale talen ondersteunen, zoals een virtueel Chinees toetsenbord (Pinyin IME).

Een nieuw woordenboekbestand (een .zbin-bestand) wordt vereist door de clienttoepassing voordat het wordt bijgewerkt naar versie 6.0. U kunt het benodigde .zbin-bestand verkrijgen via het Software- en Docs-profiel (Softdocs).

Vereisten:

* Alvorens aan Insight 6.0 cliënt en Server 6.0 van het Rapport te bevorderen, moet de beheerder van het Inzicht eerst aan Server 6.0 van het Inzicht bevorderen.
* De beheerder van het Inzicht zal een dossier moeten kiezen zbin dat op taal (en-us.zbin, zh-cn.zbin) wordt gebaseerd, dan het taaldossier kopiëren, dan het anders noemen aan insight.zbin, en het anders genoemde dossier in de wortelfolder van de Server van het Rapport plaatsen waar uitvoerbaar is gevestigd. Start vervolgens de Insight Report Server opnieuw.

Zie [Vereisten voor serverupgrade](../../../home/c-release-notes-insight/release-notes.md) voor aanvullende informatie over upgrades aan de serverzijde.

**Het zbin-bestand voor de client upgraden (van versie 5.x naar 6.0)**

1. Om ervoor te zorgen de cliënt niet van de Server van het Inzicht tijdens deze verbetering wordt bijgewerkt, plaats uw argument Insight.cfg aan vals.

   ```
   Update Software = bool: false
   ```

1. Start de Insight-client opnieuw.
1. Navigeer naar het profiel Software en Docs (SoftDocs-profiel) en download het vereiste **[!UICONTROL Insight.zbin]**-bestand: [!DNL Software\Insight Client\v6.00\Insight_6.00.zip]

1. Kopieer het bestand Insight.zbin naar dezelfde map als het bestand Insight.exe.
1. Om ervoor te zorgen de cliënt van het Inzicht nu van de Server van het Inzicht wordt bijgewerkt, verander het Insight.cfg- dossierargument in waar:

   ```
   Update Software = bool: true
   ```

1. Start de client opnieuw.

   Uw client wordt gesynchroniseerd met de server. Er wordt een bericht weergegeven dat de client downloadt. Aan het einde van het downloaden ontvangt u een bericht met de vraag of u de Insight-client opnieuw wilt starten.
1. Klik **OK** om de client opnieuw te starten.

   De client start en upgrade naar versie 6.0.

1. Start de client opnieuw om de clientsynchronisatie Insight.zbin in werking te laten treden.

   Als u het volgende bericht krijgt, dan betekent het dat zbin niet in de correcte omslagplaats naast het Insight.exe- dossier werd geplaatst.

   ```
   Insight Terminated: The backup dictionary file insight.zbin 
   is missing.
   ```

   Om de kwestie te verbeteren, schrap Insight.exe en noem de recentste versie van Insight.exe.old aan Insight.exe anders, en begin dan opnieuw met Stap 1 hierboven.

## Vereisten voor serverupgrade {#section-d6edba8b36234957ba8d06b555667a5a}

Voltooi deze verbeteringstaken voor Insight 6.0 servereigenschappen:

**Werk alle pakketten** van de Server 6.0 van het Inzicht bij. Inzicht 6.0 omvat serverpakketten die moeten worden bijgewerkt, met inbegrip van het nieuwe Predictive Analytics profiel.

>[!IMPORTANT]
>
>Adobe raadt gebruikers aan hun serverclusters bij te werken met nieuwe installaties van Insight Server 6.0.

Het wordt ook geadviseerd dat de cliënt hun serverclusters met nieuwe installatie van Server 6.0 van het Inzicht bevordert.

## Servercluster upgraden

**Bereid het taalbestand (.zbin-bestand) voor.** De beheerder van het Inzicht selecteert het  `<language>.zbin` dossier voor de vereiste taal (bijvoorbeeld: en-us.zbin , zh-cn.zbin) in de  `/localization/<language>.zbin` map. De beheerder kopieert dan het taaldossier en hernoemt het aan &quot;insight.zbin&quot;.

Na het voorbereiden van het taaldossier (.zbin), zowel moeten de Cliënt van het Inzicht als de Server van het Rapport worden bijgewerkt. De cliënt van het Inzicht wordt bijgewerkt tijdens [cliëntverbeteringsproces](../../../home/c-release-notes-insight/release-notes.md), maar in de meeste gevallen zal de beheerder van het Inzicht de Server van het Rapport bijwerken.

**Werk de Server van het Rapport met een taaldossier (.zbin dossier)** bij.

Voor alle talen, vereist Server 6.0 van het Rapport het &quot;inzicht.zbin&quot;dossier dat aan de de wortelomslag van de Server van het Rapport wordt gekopieerd.

Werk de de taaldossiers van de Server van het Rapport bij:

1. Voeg het anders genoemde &quot;inzicht.zbin&quot;dossier aan de folder van root ReportServer toe.
1. Voor het configuratiebestand Report Server (reportServer.cfg) zijn fontinstellingen voor double-bytetalen vereist. Chinees vereist bijvoorbeeld de toevoeging van lettertypen met SimSun:

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
   >Als een scène niet wordt gespecificeerd, dan blijft de Server van het Rapport aan de taal in het insight.zbin- dossier geselecteerd.

   Volg de stappen om ReportServer als dienst met de parameters van de Landinstelling te lanceren:

   1. Start een opdrachtprompt als beheerder.
   1. Navigeer naar de installatiemap van ReportServer.
   1. Typ het volgende bevel om de dienst te beginnen:

      * Voor het Engels: [!DNL ReportServer.exe -RegServer -Locale -en-us]
      * Voor Chinees: [!DNL ReportServer.exe -RegServer -Locale -zh-cn]

1. Om te verifiëren als ReportServer met de correcte parameters loopt:

   1. Open Windows Service Manager.
   1. Klik met de rechtermuisknop [!DNL Adobe Insight Report Server - Properties].

   Het pad naar het uitvoerbare bestand bevat de parameters:

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```

**Profielconfiguratiebestand wijzigen voor voorspellende analyse**. De beheerder van het inzicht zal het dossier van het douaneprofiel.cfg moeten wijzigen om het Predictive Analytics profiel te omvatten om in Insight beschikbaar te zijn.

Voorbeeld van het item profile.cfg:

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

**Werk het bestand** PAServer.cfg bij. Als u de Predictive Analytics die banen groeperen aan de Servers van het Inzicht wilt voorleggen, dan zult u het PAServer.cfg- dossier voor de behandeling van server-zij groeperen indieningen moeten vormen.

Het aangepaste profiel moet PAServer.cfg overnemen van het profiel voor voorspellende analyse (Server\Profiles\Predictive Analytics\Dataset). Configureer en sla het bestand PAServer.cfg per implementatiesite op.

>[!NOTE]
>
>Zodra PAServer.cfg wordt gevormd en aan douaneprofiel wordt bewaard, wordt een nieuw begin van de Server van het Inzicht vereist over de plaats.

**Upgraderapportserver.** U zult de doopvonten en de opstellingsparameters voor de Server van het Rapport moeten bijwerken.

Vereisten:

* Alvorens Server 6.0 van het Rapport te bevorderen, moet de beheerder van het Inzicht eerst aan Server 6.0 van het Inzicht bevorderen.
* Voor alle talen, vereist Server 6.0 van het Rapport de toevoeging van Insight.zbin aan de de wortelomslag van de Server van het Rapport. Zorg ervoor dat `base/localization/<language>.zbin` wordt gekopieerd en hernoemd naar &quot;insight.zbin&quot;. Kopieer het naar de wortel van de folder van de Server van het Rapport.

Werk de parameters Lettertypen en Start bij:

1. De Server van het rapport vereist doopvontinstelling voor dubbel-byte om aan verschillende talen uit te voeren.

   bijvoorbeeld:

   Rapportserver.cfg - Lettertypen toevoegen

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial
   ```

1. De parameter voor Server 6.0 van het Rapport moet in bevel-lijn voor lokalisatiedoeleinden worden overgegaan.

   Om de Server van het Rapport als dienst met de parameters van de Plaats te lanceren:

   1. Stop de Dienst van de Server van het Rapport.
   1. Start een opdrachtprompt als beheerder.
   1. Navigeer naar de installatiemap van Rapportserver.
   1. Typ het volgende bevel om de dienst te beginnen:

      ```
      ReportServer.exe -RegServer -Locale -en-us
      ```

Om te verifiëren als de Server van het Rapport met de correcte parameters loopt:

1. Windows Service Manager openen
1. Klik met de rechtermuisknop [!DNL Adobe Insight Report Server - Properties].
1. Het pad naar het uitvoerbare bestand bevat de parameters:

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```

**Voer een upgrade uit van de gegevensfeed SiteCatalyst voor Insight 6.0**. De bestandsindeling van de gegevensfeed SiteCatalyst voor Insight 6.0 is gewijzigd.

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
>Deze wijziging is niet van invloed op gebruikers die momenteel zijn geïmplementeerd met de *wbench/ecom*-versie van de gegevensfeed SiteCatalyst.

De filename formaatverandering zal voor het volledige gebruik van de de tijdverklaringen van het Begin en van het Eind van het Inzicht tijdens logboekverwerking toestaan. Hierdoor kan tijdens het proces worden beoordeeld of de inhoud van het bestand moet worden gelezen, in plaats van alle bronbestanden te filteren met een zoekopdracht rij voor rij.

In de meeste gevallen werd na ontvangst van het bestand een hernoemingsproces uitgevoerd om te zorgen dat deze mogelijkheid volledig werd benut. Deze wijziging biedt standaard de vereiste naamgevingsconventie zonder de noodzaak en overhead van een secundair proces.

De nieuwe gegevensfeed SiteCatalyst gebruiken:

1. Bepaal hoe het ontvangende proces het nieuwe filename formaat zal behandelen.

   De standaard anders noemen/bewegen manuscripten die tijdens implementatie worden opgesteld bewegen de dossiers met &quot;.gz&quot;uitbreiding, en voert slechts een anders naam uit als filename het filename formaat met voorafgaande RSID aanpast.

   De nieuwe bestandsindeling:

   ```
    YYYYMMDD-RSID_HH0000.tsv.gz
   ```

1. Evalueer de bepaalde logboekbronwegen om te bevestigen dat alle dossiers zullen worden gelezen.

   Als u al een script voor het wijzigen van de naam hebt geïmplementeerd, definieert u al uw logbronnen voor het lezen van deze nieuwe bestandsindeling.

## Oplossingen {#section-203f917dd6224114a1f801309c4c2cee}

* De toetsencombinatie om een werkruimte te verlaten zonder wijzigingen op te slaan is nu bijgewerkt naar **[!UICONTROL `<Ctrl>`+`<Backspace>`]**. Eerder hebt u wijzigingen doorgevoerd en een werkruimte gesloten door op `<Ctrl>` + `<Delete>` te drukken.

## Opmerkingen bij de release van Data Workbench 6.0.4{#data-workbench-release-notes}

Nieuwe functies die zijn geïntroduceerd in Data Workbench 6.0.4, waaronder opgeloste problemen en bekende problemen.

Als u vorige functies en oplossingen wilt bekijken die zijn gebaseerd op elke eerdere release, raadpleegt u de [releasearchieven](https://docs.adobe.com/content/help/en/data-workbench/using/release-notes/release-notes.html).

## Nieuwe functies {#section-2-1225066ea8f44cf68e42e019d0bca816}

Data Workbench 6.0.4 omvat deze nieuwe functies en visualisaties voor extra rapporteringsmogelijkheden en voorspellende analysehulpmiddelen.

**Vormgeving** met dichtheid voor scores. De werkbank Gegevens berekent de scores voor elke bezoeker als een geschatte waarschijnlijkheid dat een bepaalde gebeurtenis kan gebeuren. Met de visualisatie Weergavescore kunt u een score-dimensie maken die een kans biedt op een opgegeven gebeurtenis voor elke bezoeker van interesse op basis van de invoervariabelen.

![](assets/visitor_scoring_visual.png)

Zie [Propensiteitsscore](../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-visitor-propensity.md#concept-2958f4640dd44b9d86ad51c4f6165f40) voor aanvullende informatie over deze functie.

## Upgradevereisten {#section-08bd6fe3da8740fcb19688e8cac6f223}

**Logbron-id moet worden gedefinieerd**. Vanaf versie 6.04 krijgt u de volgende fout als de Logbron-id niet is gedefinieerd:

```
Missing Log Souce ID in log processing.cfg. Log Source ID must be  
defined for all log sources.
```

De opname van Rijen per Bron van het Logboek werd toegevoegd in Data Workbench 6.0 en kan in het Logboek van het douaneprofiel worden bepaald Processing.cfg door een uniek genoemde Bron identiteitskaart van het Logboek toe te voegen. Als u een lege Bron identiteitskaart van het Logboek hebt, dan kon u de kwesties van de Verwerking van het Logboek zoals onvolledig lezing van de logboekbrongegevens en andere discrepanties zien.

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

**Mogelijkheid om FSU-bronnen te delegeren**

In [!DNL Profiles/`<profilename>`/dataset/Cluster.cfg], kunt u afzonderlijke Eenheden van de Server van het Dossier (FSU) voor Normalize en de servers van de BronLijst nu specificeren. Deze diensten zijn niet langer gebonden aan de Master FSU.

>[!NOTE]
>
>Als de Server van de Lijst niet wordt gespecificeerd, dan zal de Server van de Lijst de de configuratiemontages van de Server normaliseren.

Voorbeeld in het [!DNL cluster.cfg]-bestand.

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

## Vaste bugs {#section-3b4b85a35f534288adf8a5246ef028cc}

* In Data Workbench 6.0, steunden de Matrijs van de Correlatie en de Bouwer van de Cluster niet Berekenen op Achtergrond. Dit is nu opgelost in versie 6.0.4.
* Eerder, als u een selectie op de Trechter had en een stap verwijderde, kon een toegangsschending voorkomen. Dit is opgelost.
* Oplossing voor een mogelijke vergrendelingsvoorwaarde in Segment Export die problemen kan veroorzaken bij zware belasting.
