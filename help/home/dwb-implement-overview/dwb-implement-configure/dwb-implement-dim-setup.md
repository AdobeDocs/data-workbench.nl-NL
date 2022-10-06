---
description: In deze sectie worden de verschillende typen Dimension beschreven en wordt uitgelegd hoe u deze instelt in DWB.
title: Dimension instellen
uuid: 5b40cb43-7790-4b87-a0bb-be395a420157
exl-id: 04afd773-e938-49f7-83c9-1d706a6dc525
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# Dimension instellen{#dimension-setup}

{{eol}}

In deze sectie worden de verschillende typen Dimension beschreven en wordt uitgelegd hoe u deze instelt in DWB.

## Wat zijn Dimension? {#section-dac631943df24706827cedc6f0641543}

Op het meest basisniveau zijn dimensies categorieën waarin de gegevens in de gegevensset kunnen worden opgesplitst.

Beste praktijken: Dimension in het gegevensschema kunnen elke naam hebben. De namen van Dimension die in deze cursus worden gebruikt en uitgelegd, worden beschouwd als een beste praktijk. Dimension kunnen een andere naam krijgen. Aangezien u blootstelling aan andere datasets krijgt, zult u beginnen verschillen in datasets te zien. Het is belangrijk om het doel van de dimensies te begrijpen in plaats van hun naam. Of het bijvoorbeeld &quot;Bezoeker&quot;, &quot;Klant&quot;, &quot;Persoon&quot;, &quot;Consumenten&quot; of &quot;Gebruiker&quot; wordt genoemd, het is belangrijk om te begrijpen dat deze termen vaak worden gebruikt om naar de hoogste aftelbare dimensie te verwijzen die wordt gebruikt om informatie over een enkelvoudige persoon te verzamelen.

Voor volledige informatie raadpleegt u de [Configuratie gegevensset](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/c-dataset-constr.html) hulplijn.

## Typen Dimension in DWB {#section-a4fbb7bf2bde44528ac0f94a96465862}

Er zijn twee soorten dimensies in Data Workbench: Uitgebreide Dimension en afgeleide Dimension.

Uitgebreide Dimension worden gemaakt van velden in de &quot;Raw&quot;-gegevensbestanden. De uitgebreide afmetingen worden gebruikt om &quot;ruwe&quot;gegevens te categoriseren en de verhoudingen te specificeren die onder de gegevens bestaan. De uitgebreide dimensies worden gecreeerd door de Architecten van de Data Workbench.

Afgeleide Dimension worden gecreeerd door een gebruiker &quot;op de cliënt-kant&quot;nadat de dataset gebruikend bestaande Uitgebreide afmetingsdefinities is verwerkt. Bijvoorbeeld, gebaseerd op de bestaande afmeting van URI, kan een gebruiker verkiezen om een afgeleide afmeting van de Naam van de Pagina tot stand te brengen, die een gebruikersvriendelijkere paginanaam in plaats van bepaalde URI toont. Alle dimensies bestaan uit elementen of items die samen zijn gecategoriseerd (gegroepeerd) om de dimensie te vormen. Hieronder staan drie dimensies en hun elementen.

Vele afgeleide dimensies worden gecreeerd automatisch om verschillende types van visualisaties te drijven. Wanneer een gebruiker bijvoorbeeld een site of een proceskaart maakt, maken DWB-servers een prefix-dimensie. Andere bestanden, zoals de afmetingen van de rapportagetijd, worden gedefinieerd door bestanden in de map Dimension van een profiel.

>[!NOTE]
>
>De elementen die in om het even welke bepaalde afmeting verschijnen zullen slechts die waarden weerspiegelen die in verslagen bestaan die zijn gekozen om in de dataset te worden geladen. Als er bijvoorbeeld geen gegevens zijn voor &#39;12 mei&#39;, wordt die maand niet weergegeven in de &#39;maand&#39;-dimensie.

## Uitgebreide Dimension {#section-5fc51fa539034941a30a2df606f7d727}

Typen uitgebreide Dimension

**1) Tegenstrijdige Dimension**

Op het hoogste niveau zijn de dimensies te tellen. De telbare afmetingen hebben twee belangrijke functies. Ten eerste zijn het dimensies waarvan u de elementen wilt tellen. Met andere woorden, tellen beantwoorden de vragen zoals:

* &quot;Hoeveel bezoekers hebben je homepage bezocht?&quot;
* &quot;Hoeveel bezoeken kwamen van google.com?&quot;

Om deze reden, worden teletabellen vaak gebruikt als fundamentele bouwsteen om metriek tot stand te brengen.

De tweede belangrijkste functie van tellingslijsten is dat zij de backbone van uw structuur van het datasetschema vormen. Uw gegevensschema en alle andere dimensies worden georganiseerd om onder worden gegroepeerd en tot een telbare lijst behoren. Met andere woorden, als we dimensies beschouwen als &quot;categorieën&quot;, dan zijn teletabellen de manier waarop we deze &quot;categorieën&quot; organiseren in groepen.

Wanneer dimensies worden gegroepeerd onder een aftelbare dimensie, worden ze geacht zich op het &quot;niveau&quot; van de aftelbare dimensie te bevinden. Het e-mailadres kan bijvoorbeeld het niveau van de bezoeker hebben en Browser het niveau van het Bezoek. &quot;Bovenliggend&quot; en &quot;onderliggend&quot; hebben betrekking op de relatie tussen de telbare en de onderliggende dimensies. Bezoeker is bijvoorbeeld een &#39;bovenliggend&#39; e-mailadres. Het e-mailadres is daarentegen een &quot;onderliggend&quot; lid van de Bezoeker.

**2) Eenvoudige Dimension**

De meest gangbare van alle dimensies zijn Eenvoudige afmetingen. De eenvoudige dimensies hebben een één-aan-vele verhouding met een oudertelbare dimensie en zijn algemeen gebruikt in visualisaties zodat kunt u hun elementen bekijken. Dit betekent dat een aftelbare dimensie één waarde voor een eenvoudige dimensie kan hebben maar de eenvoudige dimensie kan tot één of meerdere teletabellen behoren. Bijvoorbeeld, heeft een klant een naam van &quot;John&quot;- die klant kan slechts één voornaam hebben, nochtans, kunnen vele andere klanten de naam &quot;John hebben;. In een ander voorbeeld kan slechts één browser (bijvoorbeeld Firefox) worden gebruikt voor een bepaald bezoek aan een website, maar die browser kan worden gebruikt voor vele verschillende bezoeken.

Als de aftelbare dimensies &quot;Hoeveel?&quot;beantwoorden, dan de eenvoudige dimensies &quot;Welke degenen?&quot;beantwoorden. Gebruikend het zelfde bovenstaande voorbeeld dat in de telbare afmetingssectie wordt gebruikt; Paginanaam is de eenvoudige dimensie. Met behulp van de tabel en de eenvoudige dimensie, Paginanaam, kunnen we vragen beantwoorden zoals:

* &quot;Welke pagina had de meeste paginaweergaven?&quot;
* &quot;Van alle pagina&#39;s met winkelwagentjes, die je het meest hebt bezocht?&quot;

**3) Veel tot veel Dimension**

Vele-aan-vele dimensies hebben een vele-aan-vele verhouding met een oudertelbare dimensie. Bijvoorbeeld, als een dimensie genoemd Externe Term van het Onderzoek op het niveau van het Bezoek is; Een bepaalde externe zoekterm kan in een of meerdere bezoeken worden gebruikt en een bepaald bezoek kan een of meer externe zoektermen bevatten. De externe zoekterm is dus een veel-op-veel-dimensie.

**4) Numerieke Dimension**

Numerieke afmetingen zijn een type eenvoudige afmeting met een numerieke waarde. De numerieke afmetingen worden vaak gecreeerd om in metriek te worden gebruikt. Voorbeelden van numerieke afmetingen zijn &#39;Revenue&#39;, &#39;Orders&#39; en &#39;Units&#39;. In het bovenstaande voorbeeld is &#39;Bestellingen van klanten&#39; een numerieke dimensie.
**5) Denormale Dimension** De formele afmetingen zijn dimensies die een één-aan-één verhouding met een oudertelbare dimensie hebben. Denormale afmetingen worden vaak gebruikt met dimensies die een hoge kardinaliteit hebben (veel unieke elementen), zoals identificatiegegevens. Een bezoeker kan bijvoorbeeld slechts één gebruikersnaam hebben en een gebruikersnaam kan slechts bij één bezoeker horen. Dit is dus een één-op-één relatie en kan een denormale dimensie hebben.

Bijvoorbeeld, is de Gebruiker van het Web van de Geometrixx - identiteitskaart een denormale dimensie op het klantenniveau. Aangezien het ontkennend is, heeft het een één-aan-één verhouding met zijn ouderafmeting, betekenend dat elke Gebruiker van het Web één klant heeft en elke klant slechts één identiteitskaart van de Gebruiker van het Web heeft. Aldus, kan metrische &quot;Klanten&quot;slechts &quot;1&quot;voor elk element van de Gebruiker van het Web van de Geometrixx zijn - identiteitskaart

**6) Dimension van de tijd**

Met tijdafmetingen kunt u een set periodieke of absolute lokale tijdafmetingen maken op basis van het tijdstempelveld dat u opgeeft. Voorbeelden van tijddimensies zijn &#39;Dag&#39;, &#39;Uur&#39;, &#39;Week&#39; en &#39;Uur van Dag&#39;. In het bovenstaande voorbeeld toont de tabel &#39;Uur van dag&#39; hoeveel bezoeken en paginaweergaven er zijn ontvangen tijdens de verschillende uren van de dagen.

>[!NOTE]
>
>De escape-waarde van % die wordt gebruikt voor weergave-opmaak is gelijk aan de standaard C-bibliotheek *strftime*.

## Uitgebreide Dimension definiëren {#section-38ee124ec74b43fb95f13194a9582b97}

Stappen voor het definiëren van de uitgebreide Dimension:

1. Open tijdens het werken in uw gegevenssetprofiel de Manager van het Profiel en klik Dataset om zijn inhoud te tonen.
1. Open het bestand Transformation.cfg of het bestand Transformation Dataset Include waarin u de uitgebreide dimensie wilt definiëren.
1. Klik met de rechtermuisknop op Transformaties en klik op Nieuw toevoegen > `<Extended dimension type>`.
1. Voer de juiste gegevens in voor de uitgebreide dimensie. Zie de volgende secties voor beschrijvingen van de transformatietypen en informatie over de parameters ervan:

   * [Vertelbare Dimension](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-count-dim.html)
   * [Eenvoudige Dimension](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-simple-dim.html)
   * [Veel-tot-veel Dimension](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-many-dim.html)
   * [Numerieke Dimension](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-num-dim.html)
   * [Denormale Dimension](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-denormal-dim.html)
   * [Dimension tijd](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-time-dim.html)

1. Voor om het even welke uitgebreide afmeting die u bepaalt, kunt u één of meerdere commentaarlijnen aan de parameter van Commentaren toevoegen om de afmeting verder te beschrijven of nota&#39;s over zijn gebruik toe te voegen. Als u een opmerking wilt toevoegen, klikt u met de rechtermuisknop op de knop *Opmerkingen* label en klik op* Nieuwe toevoegen > Opmerkingsregel*.

1. Nadat u uw uitgebreide afmeting(en) in het configuratiebestand hebt gedefinieerd, slaat u het bestand lokaal op en slaat u het op in uw gegevenssetprofiel op de DWB-server.

## Uitgebreide Dimension verbergen {#section-02339fb51658418eabc10186cd5957d7}

Uitgebreide Dimension kunnen worden verborgen, zodat ze niet worden weergegeven in het menu Dimension in de DWB. Als u de dimensie wilt verbergen, stelt u de eigenschap Verborgen in op &quot;Waar&quot; in de dimensie-definitie.
