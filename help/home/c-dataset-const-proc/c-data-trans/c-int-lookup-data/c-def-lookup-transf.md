---
description: Informatie over de transformaties die u kunt gebruiken om raadplegingsgegevens in de dataset op te nemen.
solution: Analytics
title: Het bepalen van de Transformaties van de Raadpleging
topic: Data workbench
uuid: 4f7358b1-9e6a-4d03-b0c6-411e454fc11e
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Het bepalen van de Transformaties van de Raadpleging{#defining-lookup-transformations}

Informatie over de transformaties die u kunt gebruiken om raadplegingsgegevens in de dataset op te nemen.

Merk op dat niet alle types tijdens beide fasen van het proces van de datasetconstructie kunnen worden gebruikt.

* [Categoriseren](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-def-lookup-transf.md#section-8474376c14e54d14ae73749696ada468)
* [FlatFileLookup](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-def-lookup-transf.md#section-e09b2eeb96444a859b14f03cdaab31f2)
* [ODBCLookup](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-def-lookup-transf.md#section-4dcc3747e42e45c0a057e85f308a83cc)

## Categoriseren {#section-8474376c14e54d14ae73749696ada468}

De [!DNL Categorize] transformatie gebruikt een twee-kolom raadplegingslijst die uit patroon-koord/waardeparen wordt samengesteld. Tijdens deze transformatie, leest de server van de gegevenswerkbank elke verslag van gebeurtenisgegevens beurtelings en vergelijkt de inhoud van een aangewezen gebied in het verslag bij elk van de patroonkoorden die in de eerste kolom van de raadplegingslijst worden vermeld. Als het aangewezen gebied één van de patroonkoorden aanpast, schrijft de server van de gegevenswerkbank de waarde (die in de tweede kolom wordt gevonden) die met dat patroonkoord aan een aangewezen outputgebied in het verslag wordt geassocieerd.

De koorden in de eerste kolom van de raadplegingslijst kunnen naar keuze met het ^ karakter en/of eind in het $ karakter beginnen om aanpassing aan het begin en/of eind te dwingen. Deze transformatie keurt geen regelmatige uitdrukkingen voor het bepalen van gelijke voorwaarden in de eerste kolom goed. Als de inputwaarde een vector van koorden is, wordt elk koord in werking gesteld door de transformatie en het (de) resultaat(en) worden toegevoegd aan een vector van het outputkoord.

Een [!DNL Categorize] transformatie is over het algemeen gemakkelijker en sneller dan het gebruiken van een [!DNL Regular Expression] transformatie om het zelfde ding te verwezenlijken.

>[!NOTE]
>
>De in gebruikte substring test [!DNL Categorize] is case-sensitive tenzij anders gespecificeerd gebruikend de [!DNL Case Sensitive] parameter.

<table id="table_1773344FAAE34BD4919CC4414249FDEE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gevallengevoelig </td> 
   <td colname="col2"> Waar of vals. Specificeert of de substring test case-sensitive is. </td> 
   <td colname="col3"> waar </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Standaard </td> 
   <td colname="col2"> De standaardwaarde te gebruiken als de voorwaardentest overgaat en geen ingang in het categorisatiedossier de input aanpast, of het inputgebied wordt niet bepaald in de bepaalde logboekingang. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afbakening </td> 
   <td colname="col2"> <p>Koord dat wordt gebruikt om de kolommen in het raadplegingsdossier te scheiden. Moet één enkel karakter in lengte zijn. </p> <p> Als u de sleutel van CTRL onderdrukt en binnen de parameter van de Afbakening met de rechtermuisknop aanklikt, verschijnt een menu van het <span class="wintitle"> Tussenvoegsel</span> . Dit menu bevat een lijst van speciale karakters die vaak als afbakeningen worden gebruikt. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Meerdere waarden </td> 
   <td colname="col2"> Waar of vals. Als waar, wanneer de veelvoudige rijen in het dossier de input aanpassen, resulteert elke gelijke in een waarde die aan de outputvector van koorden wordt toegevoegd. Als vals, slechts wordt de eerste passende rij in het dossier gebruikt in de output. In het laatste geval, als de input een vector is, is de output ook een vector van gelijkwaardige lengte. Als de input een eenvoudig koord is, is de output ook een eenvoudig koord. </td> 
   <td colname="col3"> vals </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand </td> 
   <td colname="col2"> Pad en bestandsnaam van het categorisatiebestand. De relatieve wegen zijn met betrekking tot de installatiefolder voor de server van de gegevenswerkbank. Dit dossier wordt typisch gevestigd in de folder van Raadplegingen binnen de de installatiefolder van de gegevenswerkbank. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> Het categorisatiedossier past zijn substrings aan tegen de waarde op dit gebied om de passende rij in het dossier te identificeren. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het gebied verbonden aan het resultaat. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

**Overwegingen voor categoriseren**

* De veranderingen in raadplegingsdossiers in [!DNL Categorize] transformaties die in het [!DNL Transformation.cfg] dossier of in een [!DNL Transformation Dataset Include] dossier worden bepaald vereisen retransformation van de dataset. De dossiers van de raadpleging voor [!DNL Categorize] transformaties die in het [!DNL Log Processing.cfg] dossier of een [!DNL Log Processing Dataset Include] dossier worden bepaald zijn niet onderworpen aan deze beperking. Voor informatie over het opnieuw verwerken van uw gegevens, zie [Verwerking en Herschikking](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

* [!DNL Categorize] transformaties die in het [!DNL Log Processing.cfg] dossier of een [!DNL Log Processing Dataset Include] dossier worden bepaald herladen hun raadplegingsdossiers wanneer de raadplegingsdossiers veranderen. De veranderingen worden niet retroactief toegepast, maar zij zijn op alle logboekgegevens van toepassing die na de verandering worden gelezen.

Dit voorbeeld illustreert het gebruik van de [!DNL Categorize] transformatie om raadplegingsgegevens met gebeurtenisgegevens te integreren die van websiteverkeer worden verzameld. Veronderstel dat een bepaalde website bedrijfssecties heeft, en er een vereiste is om te kunnen bekijken en vergelijkingen maken die op verkeersstroom en waarde worden gebaseerd die door de verschillende secties wordt geproduceerd. U kunt een raadplegingsdossier tot stand brengen dat van substrings een lijst maakt die worden gebruikt om deze verschillende secties te identificeren.

Het raadplegingsdossier [!DNL Lookups\custommap.txt] bevat de volgende lijst:

| /producten/ | Producten |
|---|---|
| ^/sport/ | Sport |
| ^/nieuws/ | Nieuws |
| ... | ... |

Dit categoriseringsdossier brengt om het even wat in kaart die de koord &quot;/producten/&quot;bevatten aan de waarde &quot;Producten,&quot;om het even wat beginnend met &quot;/sport/&quot;aan de waarde &quot;Sports,&quot;en om het even wat die met &quot;/nieuws/&quot;aan de waarde &quot;Nieuws&quot;beginnen.&quot; De volgende categorisatie transformatie gebruikt de waarde op het cs-uri-stengebied als koord waarin wij een passende substring zoeken. Het resultaat van de transformatie wordt geplaatst in het x-douanommap gebied.

![](assets/cfg_TransformationType_Categorize.png)

Veronderstellend dat de Veelvoudige parameter van Waarden aan vals wordt geplaatst, zou het voorbeeld de volgende waarden voor x-douaneComap produceren gezien de vermelde waarden voor cs-uri-stem.

| [!DNL cs-uri-stem] | [!DNL x-custommap] |
|---|---|
| [!DNL /sports/news/today.php] | Sport |
| [!DNL /sports/products/buy.php] | Producten |
| [!DNL /news/headlines.php] | Nieuws |
| [!DNL /news/products/subscribe.php] | Producten |

De output is gebaseerd op de orde van substrings in het raadplegingsdossier. Bijvoorbeeld, keert de cs-uri-stem &quot;Producten [!DNL /sports/products/buy.php] &quot;terug.&quot; Hoewel de stam van URI met &quot;/sports/ begint,&quot;is het koord &quot;/products/&quot;vermeld vóór &quot;/sports/&quot;in het raadplegingsdossier. Als de Veelvoudige parameter van Waarden aan waar werd geplaatst, zou er een extra waarde voor x-douanePap zijn, aangezien het laatste voorbeeld twee rijen in de raadplegingslijst zou aanpassen: Producten en nieuws.

## FlatFileLookup {#section-e09b2eeb96444a859b14f03cdaab31f2}

De [!DNL FlatFileLookup] transformatie gebruikt een raadplegingslijst die uit om het even welk aantal kolommen en rijen wordt samengesteld (hoewel, herinner eraan dat het in geheugen verblijft). Tijdens dit type van transformatie, leest de server van de gegevenswerkbank elk verslag van gebeurtenisgegevens beurtelings en vergelijkt de inhoud van een aangewezen gebied in het verslag bij elk van de waarden in een aangewezen kolom van de raadplegingslijst. Als er een gelijke is, schrijft de server van de gegevenswerkbank één of meerdere waarden van de passende rij in de raadplegingslijst aan één of meerdere aangewezen outputgebieden in het verslag van gebeurtenisgegevens.

De raadplegingslijst die tijdens deze transformatie wordt gebruikt is bevolkt van een vlak dossier de waarvan plaats u specificeert wanneer u de transformatie bepaalt.

<table id="table_772B8ABF3B44493F99069010DDB5F77A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Standaard </td> 
   <td colname="col2"> De standaardwaarde aan gebruik als de voorwaarde wordt voldaan aan en als geen ingang in het raadplegingsdossier de input aanpast. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afbakening </td> 
   <td colname="col2"> <p>Koord dat wordt gebruikt om de kolommen in het raadplegingsdossier te scheiden. Moet één enkel karakter in lengte zijn. </p> <p> Als u de sleutel van CTRL onderdrukt en binnen de parameter van de Afbakening met de rechtermuisknop aanklikt, verschijnt een menu van het <span class="wintitle"> Tussenvoegsel</span> . Dit menu bevat een lijst van speciale karakters die vaak als afbakeningen worden gebruikt. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand </td> 
   <td colname="col2"> Weg en dossier - naam van het raadplegingsdossier. De relatieve wegen zijn met betrekking tot de installatiefolder voor de server van de gegevenswerkbank. Dit dossier wordt typisch gevestigd in de folder van Raadplegingen binnen de de installatiefolder van de Server van de gegevenswerkbank. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Koptekst </td> 
   <td colname="col2"> Waar of vals. Wijst erop dat de eerste rij in de lijst een kopbalrij is die in verwerking moet worden genegeerd. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> <span class="wintitle"> De kolomnaam</span> is de naam van de kolom die wordt gebruikt om de invoer aan de rij(len) in het bestand aan te passen. Als de Rij van de Kopbal waar is, kan dit de naam van een kolom in het raadplegingsdossier zijn. Anders, moet dit het op nul-gebaseerde kolomaantal zijn om tegen aan te passen. <span class="wintitle"> De Naam</span> van het gebied is de naam van het gebied dat wordt gebruikt om van de rij in het raadplegingsdossier de plaats te bepalen. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Meerdere waarden </td> 
   <td colname="col2"> <p>Waar of vals. Bepaalt of één enkele waarde (een passende rij) of veelvoudige waarden (voor elke passende rij) zouden moeten zijn teruggekeerd. </p> <p> <p>Opmerking:  Als de <span class="wintitle"> Veelvoudige Waarden</span> aan vals worden geplaatst, moet u ervoor zorgen dat er geen veelvoudige gelijken zijn. Wanneer de veelvoudige gelijken voorkomen, is er geen garantie die zal worden teruggegeven de gelijke. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Resultaten </td> 
   <td colname="col2"> <p>Een vector van kolomvoorwerpen (resultaten) waarin elk voorwerp door kolom en gebiedsnamen wordt bepaald. </p> <p> <span class="wintitle"> De Naam</span> van de kolom is de kolom waarvan de outputwaarde wordt verkregen. Als de Rij <span class="wintitle"></span> van de Kopbal waar is, kan dit de naam van een kolom in het raadplegingsdossier zijn. Anders, moet dit het op nul-gebaseerde kolomaantal zijn om tegen aan te passen. </p> <p> <span class="wintitle"> De Naam</span> van het gebied is de naam van het gebied dat wordt gebruikt om de output te vangen. Merk op dat dit een vector van resultaten kan zijn, voor elke rij die in het geval wordt geïdentificeerd waar de Veelvoudige parameter van Waarden waar is. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

**Overwegingen voor[!DNL FlatFileLookup]**

* Het aanpassen van het inputgebied aan het raadplegingsdossier is altijd case-sensitive.
* De veranderingen in raadplegingsdossiers in [!DNL FlatFileLookup] transformaties die in het [!DNL Transformation.cfg] dossier of de [!DNL Transformation Dataset Include] dossiers worden bepaald vereisen retransformation van de dataset. De dossiers van de raadpleging voor [!DNL FlatFileLookup] transformaties die in het [!DNL Log Processing.cfg] dossier of de [!DNL Log Processing Dataset Include] dossiers worden bepaald zijn niet onderworpen aan deze beperking. Voor informatie over het opnieuw verwerken van uw gegevens, zie [Verwerking en Herschikking](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

* [!DNL FlatFileLookup] de transformaties in het [!DNL Log Processing.cfg] dossier of de [!DNL Log Processing Dataset Include] dossiers laden hun raadplegingsdossiers opnieuw wanneer de raadplegingsdossiers veranderen. De veranderingen worden niet retroactief toegepast, maar zij zijn op alle logboekgegevens van toepassing die na de verandering worden gelezen.

Dit voorbeeld illustreert het gebruik van de [!DNL FlatFileLookup] transformatie om raadplegingsgegevens met gebeurtenisgegevens te integreren die van websiteverkeer worden verzameld. Veronderstel dat u websitepartners wilt isoleren die verkeer aan de website verpletteren en hun partner IDs in gebruikersvriendelijker namen omzetten. U kunt dan de gebruikersvriendelijke namen gebruiken om uitgebreide afmetingen en visualisaties tot stand te brengen die aan de bedrijfsverhouding duidelijker in kaart brengen dan de plaats-aan-plaats verhouding die voor het verpletteren van verkeer wordt gebruikt.

De onderzoeken van de voorbeeldtransformatie het cs (verwijzing-vraag) gebied voor het PartnerID naam-waarde paar, en, indien gevestigd, het raadplegingsdossier [!DNL Lookups\partners.txt] wordt gebruikt om de waarde PartnerID tegen de waarden in de [!DNL Partner] kolom van de lijst te vergelijken. Als een rij wordt gevestigd, wordt de x-partner-naam van het outputgebied gegeven de naam van de [!DNL PrintName] kolom van de geïdentificeerde rij.

![](assets/cfg_TransformationType_FlatFileLookup.png)

Als de raadplegingslijst de volgende informatie bevatte:

| ID | Partner | Begonnen | PrintName |
|---|---|---|---|
| 1 | P154 | 21 aug. 1999 | Yahoo |
| 2 | P232 | 10 juli 2000 | Microsoft |
| 3 | P945 | 12 jan. 2001 | Amazon |

De volgende voorbeelden zouden als volgt omzetten:

* Als cs (referrer) (PartnerID) P232 terugkeerde, zou het gebied x-partner-naam de waarde &quot;Microsoft worden gegeven.&quot;
* Als cs (referrer) (PartnerID) P100 terugkeerde, zou het gebied x-partner-naam de waarde &quot;Geen Partner worden gegeven.&quot;
* Als cs (referrer) (PartnerID) niets terugkeerde, zou het gebied x-partner-naam de waarde &quot;Geen Partner&quot;worden gegeven zoals die door de Standaard parameter wordt gespecificeerd.

## ODBCLookup {#section-4dcc3747e42e45c0a057e85f308a83cc}

De [!DNL ODBCLookup] transformatie werkt als een [!DNL FlatFileLookup] transformatie. Het enige verschil is dat de raadplegingslijst die tijdens deze transformatie wordt gebruikt van een ODBC- gegevensbestand en niet een vlak dossier wordt bevolkt.

>[!NOTE]
>
>[!DNL ODBCLookup] de transformaties kunnen slechts tijdens de transformatiefase van het proces van de datasetconstructie worden uitgevoerd. Wanneer mogelijk, adviseert Adobe dat u de [!DNL FlatFileLookup] transformatie in plaats van de [!DNL ODBCLookup] transformatie gebruikt. [!DNL FlatFileLookup] de transformaties zijn inherent betrouwbaarder omdat zij niet van de beschikbaarheid van een buitensysteem afhangen. Bovendien, is er minder risico dat de raadplegingslijst wordt gewijzigd als het in een vlak dossier verblijft dat u plaatselijk controleert.

<table id="table_B903DB291BCC4F44B09D54300216D288"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam gegevensbron </td> 
   <td colname="col2"> Een DSN, zoals die door een beheerder van de de servermachine van de gegevenswerkbank wordt verstrekt waarop de dataset wordt verwerkt, die naar het gegevensbestand verwijst waarvan het gegeven moet worden geladen. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Database-wachtwoord </td> 
   <td colname="col2">Het wachtwoord dat moet worden gebruikt wanneer het verbinden met het gegevensbestand. Als een wachtwoord voor DSN in de Beheerder <span class="wintitle"> van de</span>Gegevensbron is gevormd, kan dit leeg worden verlaten. Om het even welk hier verstrekt wachtwoord treedt het wachtwoord met voeten dat voor DSN in de Beheerder van de <span class="wintitle"> Gegevensbron</span>wordt gevormd. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikersnaam database </td> 
   <td colname="col2">De gebruiker - identiteitskaart die moet worden gebruikt wanneer het verbinden met het gegevensbestand. Als een gebruiker - identiteitskaart voor DSN in de Beheerder <span class="wintitle"> van de</span>Gegevensbron is gevormd, kan dit leeg worden verlaten. Om het even welke die gebruiker - identiteitskaart hier wordt verstrekt treedt de gebruiker - identiteitskaart met voeten voor DSN in de Beheerder van de <span class="wintitle"> Gegevensbron</span>wordt gevormd die. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Standaard </td> 
   <td colname="col2"> De standaardwaarde te gebruiken als de voorwaarde wordt voldaan aan en geen ingang in het raadplegingsdossier past de input aan. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoerkolom </td> 
   <td colname="col2"> <span class="wintitle"> De Naam</span> van de kolom is de kolomnaam of SQL uitdrukking voor het gegeven dat tegen de input wordt aangepast. <span class="wintitle"> De Naam</span> van het gebied is de naam van het gebied dat de te bekijken gegevens bevat. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Meerdere waarden </td> 
   <td colname="col2"> <p>Waar of vals. Bepaalt of één enkele waarde (een passende rij) of veelvoudige waarden (voor elke passende rij) zouden moeten zijn teruggekeerd. </p> <p> <p>Opmerking:  Als de <span class="wintitle"> Veelvoudige Waarden</span> aan vals worden geplaatst, moet u ervoor zorgen dat er geen veelvoudige gelijken zijn. Wanneer de veelvoudige gelijken voorkomen, is er geen garantie die zal worden teruggegeven de gelijke. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Outputkolommen </td> 
   <td colname="col2"> <p>Een vector van kolomvoorwerpen (resultaten) waar elk voorwerp door kolom en gebiedsnamen wordt bepaald. </p> <p> <span class="wintitle"> De Naam</span> van de kolom is de naam van of SQL uitdrukking voor de kolom waarvan de outputwaarde wordt verkregen. <span class="wintitle"> De Naam</span> van het gebied is de naam van het gebied dat wordt gebruikt om de output te vangen. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Tabelidentificator</span> </td> 
   <td colname="col2"> Een SQL uitdrukking die de lijst of de mening noemt waarvan het gegeven moet worden geladen. Een typisch lijstherkenningsteken is van de vorm SCHEMA.TABLE. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

* De naam van de Gegevensbron, [!DNL Database User ID], [!DNL Database Password]en de parameters van het Herkenningsteken van de Lijst zijn het zelfde als de parameters van de zelfde namen die voor ODBC gegevensbronnen worden beschreven. Zie [ODBC Gegevensbronnen](../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3).

* In tegenstelling tot ODBC gegevensbronnen, vereisen de [!DNL ODBCLookup] transformaties geen stijgende kolom van identiteitskaart. Zie [ODBC Gegevensbronnen](../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3). Dat is omdat de inhoud van de raadplegingslijst op geen enkele manier moet veranderen terwijl de dataset actief is. De veranderingen in een raadplegingslijst of een mening kunnen niet worden ontdekt tot de retransformatie voorkomt. Voor informatie over het opnieuw verwerken van uw gegevens, zie [Verwerking en Herschikking](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

Veronderstel dat u verouderde DNS verslagen in de bijgewerkte verslagen wilt omzetten. Beide reeksen verslagen worden opgeslagen in een SQL gegevensbestand. Om deze taak uit te voeren, zou u een raadplegingslijst van verwijzingen voorzien die van het gegevensbestand wordt geproduceerd en de verouderde DNS verslagen vervangen.

Onze voorbeeldtransformatie zoekt de logboekingangen naar het s-dns gebied, en, indien gevestigd, wordt de raadplegingslijst VISUAL.LOOKUP gebruikt om de s-dns ingang tegen de ingangen in de [!DNL OLDDNS] kolom van de lijst te vergelijken. Als een rij in de lijst wordt gevestigd, wordt het outputgebied s-dns gegeven de bijgewerkte DNS verslagingang van de [!DNL NEWDNS] kolom van de geïdentificeerde rij.

![](assets/cfg_TransformationType_ODBCLookup.png)

