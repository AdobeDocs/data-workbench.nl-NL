---
description: De verschillende types van Afgeleide (de Kant van de Cliënt) Afmetingen en hoe te om die in de Werkbank van Gegevens te plaatsen.
title: Voortgekomen de Opstelling van Afmetingen
uuid: 9d2416fb-1c29-45a8-91d0-ddca575224ad
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Voortgekomen de Opstelling van Afmetingen{#derived-dimensions-setup}

De verschillende types van Afgeleide (de Kant van de Cliënt) Afmetingen en hoe te om die in de Werkbank van Gegevens te plaatsen.

## Typen afgeleide afmetingen {#section-33e6dcc9ab9745de9b830cecb2427ca3}

**Metrische afmetingen**

De metrische Dimensie staat u toe om metrische tellingen door een specifiek Niveau te groeperen. Het staat u ook toe om metrische tellingen door een specifiek niveau te groeperen. Zodra, wordt een Metrische Dimensie gecreeerd, kunt u gegevens segmenteren die op de metrische waarde worden gebaseerd.

Voorbeeld 1: U bent een Reisbedrijf en u wilt het verschil begrijpen van gedragsactiviteiten op de website tussen uw frequente vliegers en klanten die minder dan vijf keer per vlucht hebben geboekt.

Allen u is telling van Boekingen als metrisch hebt, hoe u klanten segmenteert die op metrisch - hier, boekend - worden gebaseerd om hun gedrag op de website te begrijpen?

Voorbeeld 2: U bent een Financiële Bank en u wilt uw klanten groeperen die op aantal CDs worden gebaseerd zij hebben geïnvesteerd in. U wilt uw klanten in 3 Lagen segmenteren. Niveau 1 - Klanten met 10+ CDs, Laag 2 - Klanten met >5 en &lt;10 CDs en Laag 3 - Klanten met >0 en &lt;5 CDs

De informatie u hebt is metrisch die u tellingen van CD investeringen geeft - hoe zult u de Verband Segmenten van de Klant voor uw analyse creëren?

*Metrische dimensie maken - via werkstation*

Merk één van de metrische afmetingen OOB zoals lokaal en noem die afmeting met een douanenaam anders / maak lokaal exemplaar van RenameDim.example en noem het aan de juiste afmetingsnaam met .dim uitbreiding anders

Open de pas gecreëerde dimensie in het werkstation om veranderingen aan te brengen. Verandering volgende parameters van de metrische dimensie die op de vereisten wordt gebaseerd: ![](assets/dwb_impl_derived_dims1.png)

Metrisch - Te groeperen metrisch

Niveau - Niveau waarop de metriek zal worden gegroepeerd

Het Begin van de Emmer - Beginnend element van de Metrische Dimensie. Ga de zelfde waarde in compensatie in.

De Grootte van de Emmer - de grootte van de groepering van metrisch. Voer dezelfde waarde in op schaal

Emmertelling - Maximum aantal elementen dat in de afmeting moet worden getoond

Sparen de pas gecreëerde dimensie op de server als u het met anderen wilt delen.

**Afmetingen voorfixen**

Het belangrijkste doel van de afmeting van de Prefix is elementen van de originele afmeting te groeperen en gebruikersvriendelijke namen aan de gegroepeerde elementen te verstrekken.

Bijvoorbeeld, bezit u een detailhandelplaats en uw plaats heeft diverse plaatssecties zoals de Klein van de Vrouwen, Mannen Apparel, Speelgoed en Spelen, het Decor van het Huis, enz. en elk van deze plaatssecties heeft verscheidene pagina&#39;s verbonden aan het. U wilt weganalyse doen en inzicht krijgen over het verkeer dat van één plaatssectie aan andere gaat etc. Als u de afmeting van URI gebruikt, zult u elke pagina van elk van de plaatssectie in Browser van de Weg of de Kaart van het Proces moeten trekken en de analyse voortzetten.

De zelfde analyse kan gemakkelijk worden gedaan als er een dimensie van de Prefix is die pagina&#39;s van een plaatssectie heeft die samen als één enkel element wordt gegroepeerd.

Afmetingen prefix maken:

Open een 2D proceskaart van het menu van de Visualisatie.

Verandering volgende parameters van de prefixafmeting die op de vereisten wordt gebaseerd.

De Afmeting van de Kaart van de verandering - de Afmeting die u voor 2D proceskaart wilt gebruiken (Ex: SMS-typologie)

Afmetingen van kaartniveau wijzigen - Niveau van de bovengenoemde dimensie

De Afmeting van de Klem van de Kaart van de verandering - het telbare niveau waarop u de gegevens wilt bekijken.

Metrisch van de Kaart van de verandering - metrisch die u wilt bekijken.

Zodra de 2D kaart van het Proces wordt geplaatst, open de afmeting die u in de parameter van de Afmeting van de Kaart van de Verandering vermeldde.

Selecteer de elementen u wilt groeperen. Gebruik CTRL+ALT en sleep en laat vallen de elementen op aan proceskaart.

Klik met de rechtermuisknop op het punt dat wordt weergegeven en noem de naam van de groep. Als u 3 elementen aan groep hebt geselecteerd, zal de standaardnaam 3 Geselecteerd zijn.

Klik op de contouren van de visualisatie met de rechtermuisknop en sla dimensie op in het menu dat wordt weergegeven.

**Naam van afmetingen wijzigen**

Noem Dimensies anders wordt gecreeerd van een reeds bestaande dimensie. Het belangrijkste doel van de nieuwe dimensie is gebruikersvriendelijke namen aan de elementen van de dimensie te verstrekken. Uit de doos noemt afmeting anders is de afmeting van de Pagina die van de afmeting van URI wordt gecreeerd. De dimensie van URI kan voor een persoon verwarrend zijn die geen technische namen van de pagina&#39;s kent en dat is waarom de dimensie van de Pagina u toestaat om elementen van de dimensie van URI anders te noemen.

AFMETINGEN VAN DE DOUANE-RENAME MAKEN:

De elementen van de anders genoemde afmeting houden een afbeelding van één op één met de elementen van de originele basisafmeting. U kunt dit verifiëren door het .dim dossier van Rename Dimensie in het werkstation/de stootkussen van de Nota te openen. U zult opmerken dat elk element van de originele afmeting slechts één waarde (noem Koord anders) tegen het in het dossier heeft.

Als u minder elementen voor anders noemt doel hebt; u kunt een .dim dossier in het werkstation tot stand brengen en elke individuele elementen anders noemen door de hieronder verklaarde stappen.

Stappen om een .dim dossier voor te creëren anders noemen Dimensie - Gebruikend het Werkstation

Gebruik deze optie als de aantallen te hernoemen elementen minder zijn.

1. Open een lege werkruimte en open de Manager van Afmetingen. Klik met de rechtermuisknop op>Beheer>Profiel>Profielbeheer.
1. Breid de Omslag van Afmetingen in de Kolom van het Dossier uit.
1. Breid de Omslag van de Pagina in de Kolom van het Dossier uit en klik op het Page.dim- dossier in de Tweede aan Laatste kolom met de rechtermuisknop aan (Deze kolom vertegenwoordigt gewoonlijk de Naam van het Profiel) en klik op de &quot;maak Lokale&quot;optie.
1. Klik op Page.dim in de kolom &quot;Gebruiker&quot;met de rechtermuisknop aan en klik op de optie van het Exemplaar en kleef het gekopieerde.dim- dossier binnen aan de gewenste omslag onder de folder van Afmetingen.
1. Klik op OK in het foutbericht.
1. Nu, zult u opmerken dat er twee Page.dim- dossiers onder de omslag van Afmetingen zijn. Één is het originele dossier onder de folder van de Pagina van Afmetingen \ en tweede is die u enkel gekleefd in stap 4 kopieert.
1. Klik op het onlangs gekleefde Page.dim- dossier onder de kolom van de Gebruiker met de rechtermuisknop aan en klik op het blauwe/grijze inputvakje dat Page.dim zegt. De inputdoos zal groen met de curseur het knipperen worden, erop wijzend dat het kan worden gewijzigd. Typ de naam van de Rename dimensie die u wilt creëren.
1. U zult opmerken dat het Page.dim- dossier in de Kolom van het Dossier werd veranderd in het nieuwe dossier - naam u in stap 7 gaf. Klik met de rechtermuisknop op het bestand new.dim in de kolom Gebruiker (Laatste kolom) en selecteer Open>In werkstation.
1. Zodra het .dim dossier in het werkstation wordt geopend; klik op het plusteken (+) naast de entiteit en breid het uit. Neem waar de waarde aanwezig tegen het gebied van de &quot;Ouder&quot;is, wijst het op &quot;URI&quot;dimensie. Het toont &quot;gegevens/model/dim/URI&quot;Klik op de blauwe/grijze inputdoos om URI in de naam van de afmeting te veranderen de waarvan elementen u wilt anders noemen.
1. Verzeker de afmeting die u wilt anders noemen in de dataset bestaat. De namen van de afmeting zijn gevoelig geval zodat behouden het geval van de originele afmeting.
1. Neem de &quot;gewijzigde&quot;verschijning naast de afmetingsnaam waar. Dit wijst erop dat de originele afmeting is gewijzigd. de in stap 9 aangebrachte wijzigingen te ondersteunen; Klik met de rechtermuisknop op new.dim (gewijzigd) en klik op de optie &quot;Opslaan als&quot;.
1. Zodra de afmeting per stap 10 wordt bewaard, is pas gecreeerd anders noemen afmeting voor de Campagnes nu beschikbaar aan u voor het anders noemen van het doel. Dit is slechts beschikbaar plaatselijk aan u.
1. om anderen te kunnen zien de afmeting door u wordt gecreeerd, moet het op het profiel worden bewaard dat. Klik met de rechtermuisknop op het .dim-bestand van de nieuwe dimensie in de kolom &quot;Gebruiker&quot; (Laatste kolom) en klik op de naam &quot;Opslaan naar>Profiel&quot; waarin u de dimensie wilt opslaan.
1. Na het bewaren van het dossier aan het profiel, zullen alle gebruikers van het Werkstation die toegang tot dit profiel hebben dimensie voor de Campagnes kunnen zien anders noemen.

De prefix en noemt het hulpmiddel van de schepper van de schemering anders

Adobe heeft een hulpmiddel van Excel om Voorvoegsel te produceren en Afmetingen anders te noemen.

Hieronder zijn de stappen om de Afmetingen van de Prefix te produceren/anders te noemen gebruikend het hulpmiddel:

1. Sparen het hulpmiddel van Excel *Adobe_DWB_Dimension_Generator.xlsm* in een omslag. De Zorg van de Klant van Adobe van het contact om het hulpmiddel te downloaden.
1. Open het hulpmiddel en laat macro&#39;s toe: ![](assets/dwb_impl_derived_dims2.png)

1. Vul het gegevensblad met de te gebruiken kleppen in.

   Bijvoorbeeld, creëren wij de Afmeting van de Prefix van het Merk van het Product die op de Afmeting van het Product wordt gebaseerd. In het gegevensblad wordt de volgende informatie vastgelegd: ![](assets/dwb_impl_derived_dims3.png)

   Elk product wordt in het gegevensblad aan een merk toegewezen.

1. In het lusje van de Configuratie, vul de informatie met betrekking tot de te creëren afmeting. Voor de onderstaande steekproefgegevens wordt informatie gegeven: ![](assets/dwb_impl_derived_dims4.png)

   Naam: Naam voor de Afmeting Prefix/anders noemen

   Type: Voorvoegsel/Naam wijzigen

   Bron: Dim: Oorspronkelijke afmeting

   Kolom van de gelijke: Te matchen kolom

   Resultaatkolom: Waarde die voor nieuwe dimensie moet worden gebruikt.

1. Klik op de knop met de titel *Klik hier*. ![](assets/dwb_impl_derived_dims5.png)

1. Het schemerdossier zal in de zelfde omslag worden geproduceerd waar het hulpmiddel werd opgeslagen. ![](assets/dwb_impl_derived_dims6.png)

   Met Profielbeheer slaat u het dimbestand op in de map Dimension.

**Shift-afmetingen**

De dimensies van de verschuiving staan u toe om het Negende element van om het even welke afmeting bij binnen om het even welke bepaalde Vertelbare Dimensie te bekijken.

Zij geven u ook de capaciteit om terug te kijken naar - het element van de Ne van om het even welke afmeting binnen om het even welke bepaalde Vertelbare Dimensie

Voorbeeld 1:

* De negende pagina binnen een sessie - Volgende paginadimensie
* De negende pagina voor een bezoeker - Volgende Pagina voor Bezoeker - over alle Zittingen
* De Negende vraag naar een gebruiker

Waarom is het belangrijk om het Nth-element van de aftelbare dimensie te kennen?

* U wilt 5thPage kennen die in een Zitting wordt bekeken.
* U wilt pathing op Campaigns doen om te begrijpen wat 2ndCampaign na het bekijken van de campagne van de &quot;Vrije Rekening van de Controle&quot;werd bekeken?
* U wilt begrijpen welke verbindingsbezoeker alvorens &quot;Chat met een Agent&quot;verbinding te klikken klikte te klikken? ![](assets/dwb_impl_derived_dims7.png)

Volgende URI is één van de dimensies van de Verschuiving OOB die als malplaatje kunnen worden gebruikt. Het voorbeeld hierboven geeft u 2nd (Compensatie = 1) element van de Campagne (Dim = Campagne) in de Gebeurtenis van de Overeenkomst (Klem = de Gebeurtenis van de Overeenkomst)

Hier staat offset 1 betekent kijk op de rechterkant - voorwaarts in de Gebeurtenis

Sommige andere OOB Afmetingen van de Verschuiving

*Volgende pagina:*

De volgende pagina die wordt weergegeven in een sessie nadat de pagina is geselecteerd in de paginadimensie

Hier wordt gecompenseerd 1, is het Niveau de Mening van de Pagina, Mam is Pagina en de Klem is Zitting

*Vorige pagina:*

De vorige pagina die in een zitting vóór momenteel geselecteerde Pagina in de Afmeting van de Pagina wordt bekeken

Hier offset is -1, Niveau is Paginaweergave, Dim is Pagina en Clip is Sessie

Wat zal de vorige Campagne zijn die vóór momenteel geselecteerde Campagne door een bezoeker wordt bekeken?

Hier compensatie is -1, is het Niveau de Reactie van de Campagne, Dim is de Waarde van de Attributen van de Reactie van de Campagne en de Klem is Bezoeker

*Shift-dimensie maken - Via werkstation*

* Merk één van de OOB verschuivingsdimensie als lokaal
* Noem die dimensie met een douanenaam anders
* Open pas gecreëerde dimensie in het werkstation om veranderingen aan te brengen
* Verandering volgende parameters van de metrische dimensie die op de vereisten wordt gebaseerd.

   * Veelzijdige dimensie
   * Offset-Je wilt achteruit kijken
   * Dim - Dimension waarvan elementen u wilt analyseren
   * De klem-tellende in u wilt bekijken.

* Sparen de pas gecreëerde dimensie op de server als u het met anderen wilt delen.

**Laatste N-dimensie**

De laatste afmetingen van N werken alleen op de tijddimensie en op het moment van gebruik van het systeem. OOB-tijddimensies zijn Dag, Week, Uur en Maand. Je kunt de laatste N-dimensie maken voor elk van deze basetijddimensies, zoals Afgelopen 10 dagen, Afgelopen 72 uur, Afgelopen 8 weken, Afgelopen 6 maanden, enz. De laatste N Dimensie berekent Laatste N die op de huidige &quot;Metrische Tijd van het Rapport&quot;wordt gebaseerd of vanaf Tijd van het systeem. ![](assets/dwb_impl_derived_dims8.png)

Telling - Totaal aantal elementen dat in de afmeting moet worden getoond

De compensatie van de waaier - compensatiewaarde om het uitgangspunt (Dag/Week) aan te geven om de laatste Dag/Week van N te berekenen.

**Geen.dim**

None.dim is een Alias-dimensie. Het wordt gebruikt om alias van uitgebreide afmetingen tot stand te brengen.

Voorbeeld:

In None.dim wordt de entiteit gedefinieerd als &quot;gegevens/model/dim/ouder/+name&quot; (het kan worden veranderd) wat betekent creeer de afmeting zoals per de naam van het afmetingsdossier. Zo als wij een exemplaar van het dossier van None.dim onder de omslag van de Dimensie (bijvoorbeeld, die het dossier van None.dim onder de omslag van het Profiel van de Bezoeker kopieert en anders noemt) creëren en het aan &quot;Logbron ID.dim&quot;anders noemen, zal een nieuwe afgeleide afmeting met Van het Bron logboek identiteitskaart verschijnen in het Menu onder het Profiel van de Bezoeker zoals hieronder getoond:

Voor wijzigingen: ![](assets/dwb_impl_derived_dims9.png)

Na niets.dim veranderingen: ![](assets/dwb_impl_derived_dims10.png)

De entiteit kan in de uitgebreide afmetingsnaam worden veranderd, in dit geval een andere afmeting met andere naam die aan de zelfde afmeting richt zoals hieronder getoond:

In dit voorbeeld heeft de &quot;Bron Name.dim&quot;de volgende inhoud: ![](assets/dwb_impl_derived_dims11.png)

Zo zal een andere Van de Bron dimensie Naam die aan Van het Bron logboek identiteitskaart richt verschijnen. ![](assets/dwb_impl_derived_dims12.png)

**Afgeleide afmetingen verbergen**

Om de Afgeleide Dimensie te verbergen, plaats het bezit van de *Show* aan &quot;vals&quot;. ![](assets/dwb_impl_derived_dims13.png)

