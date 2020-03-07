---
description: Deze sectie verklaart de verschillende types van Afmetingen en hoe te om hen te plaatsen in DWB.
title: Dimension-installatie
uuid: 5b40cb43-7790-4b87-a0bb-be395a420157
translation-type: tm+mt
source-git-commit: ded50c4eeadea80156c17a4cad985d0ceddd5500

---


# Dimension-installatie{#dimension-setup}

Deze sectie verklaart de verschillende types van Afmetingen en hoe te om hen te plaatsen in DWB.

## Wat zijn Afmetingen {#section-dac631943df24706827cedc6f0641543}

Op het meest basisniveau, zijn de afmetingen categorieën waarin de gegevens in de dataset kunnen worden uitgesplitst.

Beste praktijken: De afmetingen in het gegevensschema kunnen om het even welke naam worden verstrekt. De namen van de afmetingen die in deze cursus worden gebruikt en worden verklaard worden beschouwd als beste praktijken. De afmetingen kunnen verschillend worden genoemd. Aangezien u blootstelling aan andere datasets bereikt, zult u beginnen om verschillen in datasets te zien. Het is belangrijk om het doel van de afmetingen te begrijpen in plaats van hun naam. Bijvoorbeeld, of het wordt genoemd &quot;Bezoeker&quot;, &quot;Klant&quot;, &quot;Persoon&quot;, &quot;Consumenten&quot;, of &quot;Gebruiker&quot;, is het belangrijk om te begrijpen dat deze termen algemeen gebruikt zijn om naar de hoogste niveau telbare dimensie te verwijzen die wordt gebruikt om informatie over een enkelvoudige persoon te verzamelen.

Voor volledige informatie, zie de gids van de Configuratie van de [Dataset](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/c-dataset-constr.html) .

## Typen afmetingen in DWB {#section-a4fbb7bf2bde44528ac0f94a96465862}

Er zijn twee soorten afmetingen in de Werkbank van Gegevens: Uitgebreide afmetingen en afgeleide afmetingen.

De uitgebreide Dimensies worden gecreeerd van gebieden in de &quot;ruwe&quot;gegevensdossiers. De uitgebreide afmetingen worden gebruikt om &quot;ruwe&quot;gegevens te categoriseren en de verhoudingen te specificeren die onder de gegevens bestaan. De uitgebreide afmetingen worden gecreeerd door de Architecten van de Werkbank van Gegevens.

De afgeleide Afmetingen worden gecreeerd door een gebruiker &quot;aan de cliëntkant&quot;nadat de dataset gebruikend bestaande Uitgebreide afmetingsdefinities is verwerkt. Bijvoorbeeld, dat op de bestaande dimensie van URI wordt gebaseerd, kan een gebruiker verkiezen om een afgeleide dimensie van de Naam van de Pagina tot stand te brengen, die een gebruikersvriendelijkere paginanaam in plaats van bepaalde URI toont. Alle afmetingen bestaan uit elementen of punten die samen (gegroepeerd) zijn gecategoriseerd om de afmeting te vormen. Hieronder staan drie dimensies en hun elementen.

Vele afgeleide afmetingen worden gecreeerd automatisch om verschillende soorten visualisaties te drijven. Bijvoorbeeld, wanneer een gebruiker een plaats of een proceskaart bouwt, leiden de servers DWB tot een dimensie van de Prefix. Anderen, zoals de rapporteringstijddimensies, worden bepaald door dossiers in de folder van Afmetingen van een profiel.

>[!NOTE]
>
>De elementen die in om het even welke bepaalde afmeting verschijnen zullen slechts die waarden weerspiegelen die in verslagen bestaan die zijn gekozen om in de dataset worden geladen. Bijvoorbeeld, als er geen gegevens voor &quot;Mei &#39;12&quot;zijn, dan zal die maand niet in de &quot;Maand&quot;dimensie verschijnen.

## Uitgebreide afmetingen {#section-5fc51fa539034941a30a2df606f7d727}

Typen uitgebreide afmetingen

**1) Afmetingen tellen**

Op het hoogste niveau zijn er talloze dimensies. De meetbare afmetingen dienen twee belangrijke functies. Eerst, zijn zij afmetingen de waarvan elementen u wilt tellen. Met andere woorden, beantwoordt de tellers de vragen zoals:

* &quot;Hoeveel bezoekers hebben je homepage bezocht?&quot;
* &quot;Hoeveel bezoeken kwamen van google.com?&quot;

Om deze reden, worden de tellers vaak gebruikt als fundamentele bouwsteen om metriek tot stand te brengen.

De tweede belangrijke functie van tellers is dat zij de backbone van uw structuur van het datasetschema vormen. Uw gegevensschema en alle andere dimensies worden georganiseerd om onder worden gegroepeerd en tot een aftelbaar behoren. Met andere woorden, als we dimensies als &quot;categorieën&quot; beschouwen, dan zijn tellen de manier waarop we deze &quot;categorieën&quot; in groepen organiseren.

Wanneer de afmetingen onder een telbare dimensie worden gegroepeerd, zouden zij op het &quot;niveau&quot;van de telbare dimensie zijn. Bijvoorbeeld, kan het &quot;E-mailadres&quot;op het niveau van de Bezoeker zijn en &quot;Browser&quot;is op het niveau van het Bezoek. &quot;Ouder&quot; en &quot;kind&quot; verwijzen naar de relatie tussen de meetbare en de afmetingen die eronder zijn gegroepeerd. Bijvoorbeeld, is de Bezoeker een &quot;ouder&quot;van E-mailadres. Het e-mailadres daarentegen is een &quot;kind&quot; van de bezoeker.

**2) Eenvoudige afmetingen**

De gemeenschappelijkste van alle afmetingen zijn Eenvoudige afmetingen. De eenvoudige afmetingen hebben een één-aan-vele verhouding met een ouder telbare dimensie en worden algemeen gebruikt in visualisaties zodat kunt u hun elementen bekijken. Dit betekent dat een aftelbare afmeting één waarde voor een eenvoudige afmeting kan hebben maar de eenvoudige afmeting kan tot één of meerdere tellers behoren. Bijvoorbeeld, heeft een klant een naam van &quot;John&quot;- die klant kan één voornaam slechts hebben, nochtans, kunnen vele andere klanten de naam &quot;John hebben;. Als ander voorbeeld kan slechts één browser (bijvoorbeeld Firefox) voor om het even welk bepaald bezoek aan een website worden gebruikt maar die browser kan voor vele verschillende bezoeken worden gebruikt.

Als de aftelbare afmetingen &quot;Hoeveel?&quot;beantwoorden, dan beantwoorden de eenvoudige dimensies &quot;Welke?&quot; Het gebruiken van het zelfde hierboven gebruikte voorbeeld in de telbare afmetingssectie; De Naam van de pagina is de eenvoudige afmeting. Gebruikend de lijst en de eenvoudige afmeting, de Naam van de Pagina, kunnen wij vragen zoals beantwoorden:

* &quot;Welke pagina had de meeste paginameningen?&quot;
* &quot;Van alle Shopping Cart-pagina&#39;s, die heb je het meest bezocht?&quot;

**3) Vele aan Vele Afmetingen**

Vele-aan-vele dimensies hebben een veel-aan-vele verhouding met een ouder telbare dimensie. Bijvoorbeeld, als een dimensie genoemd de Externe Termijn van het Onderzoek op het niveau van het Bezoek is; Een bepaalde Externe Termijn van het Onderzoek kan in één of vele Bezoeken worden gebruikt, en een bepaald Bezoek kan één of vele Externe Termen van het Onderzoek omvatten. Aldus, is de Externe Termijn van het Onderzoek een vele-aan-vele dimensie.

**4) Numerieke afmetingen**

De numerieke afmetingen zijn een type van eenvoudige afmeting die een numerieke waarde heeft. De numerieke afmetingen worden vaak gecreeerd om in metriek worden gebruikt. Voorbeelden van numerieke afmetingen zijn &#39;Revenue&#39;, &#39;Orders&#39; en &#39;Units&#39;. In het voorbeeld hierboven, is de &quot;Bestellingen van de Klant&quot;een numerieke dimensie.
**5) Denormale Dimensies** Denormale dimensies zijn dimensies die een één-op-één relatie hebben met een bovenliggende afmeting. Denormale afmetingen worden vaak gebruikt met afmetingen die een hoge kardinaliteit (vele unieke elementen) hebben zoals identificatiegegevens. Een bezoeker kan bijvoorbeeld slechts één gebruikersnaam hebben en een gebruikersnaam kan slechts tot één bezoeker behoren. Dit is dus een één-op-één relatie en kan een denormale dimensie zijn.

Bijvoorbeeld, is de Gebruiker van het Web Geometrixx - identiteitskaart een denormale dimensie op het klantenniveau. Aangezien het ontvormend is, heeft het een één-aan-één verhouding met zijn ouderdimensie, betekenend dat elke Gebruiker van het Web één klant heeft en elke klant slechts één Gebruiker van het Web heeft - identiteitskaart Aldus, kan metrisch &quot;Klanten&quot;slechts &quot;1&quot;voor elk element van de Gebruiker van het Web van Geometrixx zijn - identiteitskaart

**6) Afmetingen tijd**

De afmetingen van de tijd staan u toe om een reeks periodieke of absolute lokale tijddimensies tot stand te brengen die op het timestamp gebied worden gebaseerd dat u specificeert. Voorbeelden van tijddimensies zijn &#39;Dag&#39;, &#39;Uur&#39;, &#39;Week&#39; en &#39;Uur van Dag&#39;. In het voorbeeld hierboven, toont de lijst van het &#39;Uur van Dag&#39; hoeveel bezoeken en paginameningen tijdens de verschillende uren van de dagen werden ontvangen.

>[!NOTE]
>
>De % ontsnapt die voor vertoning het formatteren wordt gebruikt is het zelfde als de standaardC bibliotheek *strftime*.

## Uitgebreide afmetingen definiëren {#section-38ee124ec74b43fb95f13194a9582b97}

Stappen om de uitgebreide dimensie te definiëren:

1. Terwijl het werken in uw datasetprofiel, open de Manager van het Profiel en klik Dataset om zijn inhoud te tonen.
1. Open het Transformation.cfg- dossier of de Dataset van de Transformatie omvatten dossier waarin u de uitgebreide afmeting wilt bepalen.
1. Klik Transformaties met de rechtermuisknop aan en de klik voegt nieuw toe > `<Extended dimension type>`.
1. Voer de juiste informatie in voor uw uitgebreide dimensie. Voor beschrijvingen van de transformatietypen en informatie over hun parameters, zie de volgende secties:

   * [Afmetingen telbaar](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-count-dim.html)
   * [Eenvoudige afmetingen](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-simple-dim.html)
   * [Vele-aan-Vele Afmetingen](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-many-dim.html)
   * [Numerieke afmetingen](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-num-dim.html)
   * [Denormale Afmetingen](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-denormal-dim.html)
   * [Afmetingen tijd](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-time-dim.html)

1. Voor om het even welke uitgebreide afmeting die u bepaalt, kunt u één of meerdere commentaarlijnen aan de parameter van Commentaren toevoegen om de afmeting verder te beschrijven of nota&#39;s over zijn gebruik toe te voegen. Om een commentaar toe te voegen, klik het etiket van *Commentaren* met de rechtermuisknop aan en klik* toevoegen nieuw > de Lijn van de Commentaar*.

1. Nadat u uw uitgebreide dimensie(en) in het configuratiebestand hebt gedefinieerd, slaat u het bestand lokaal op en slaat u het op in uw datasetprofiel op de DWB-server.

## Uitgebreide afmetingen verbergen {#section-02339fb51658418eabc10186cd5957d7}

De uitgebreide Afmetingen kunnen worden verborgen zodat verschijnen zij niet op het Menu van de Dimensie in DWB. Om de afmeting te verbergen, plaats het Verborgen bezit aan &quot;Waar&quot;in de afmetingsdefinitie.
