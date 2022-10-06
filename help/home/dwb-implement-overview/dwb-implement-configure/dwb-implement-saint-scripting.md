---
description: In dit gedeelte wordt het script van Saint Scrubber uitgelegd.
title: Een script maken voor de SAINT-scrubber
uuid: 2e5aa6f2-dadb-48a6-8443-69396530587c
exl-id: 5f6d92b1-baaa-4d67-a1c2-ce7d51affb17
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Een script maken voor de SAINT-scrubber{#scripting-for-the-saint-scrubber}

{{eol}}

In dit gedeelte wordt het script van Saint Scrubber uitgelegd.

## Overzicht van de classificatie van SAINT {#section-b840a99f10684bb4b58e844a515d0d79}

De classificatie is ook gekend door acroniem SAINT voor het Importeren van Attributen van SiteCatalyst en het Namen Hulpmiddel.

Wanneer wij &quot;classificeren&quot;een variabele van de SiteCatalyst, u een verband tussen een variabele en meta-gegevens met betrekking tot die variabele vestigen. Classificaties worden het vaakst gebruikt in het gebied Campagnes, dus zal ik dat als manier gebruiken om hen te verklaren. De meeste cliënten verzenden campagneverkeer naar hun plaats gebruikend een volgende code. Deze volgcode is een id die een specifiek trefwoord kan vertegenwoordigen dat op Google is aangeschaft, zoals &quot;goog123&quot;. Deze id wordt doorgegeven aan de variabele s.campagnes, zodat u kunt zien welke gebeurtenissen met betrekking tot het succes van de site plaatsvinden nadat bezoekers vanuit die campagnecode naar uw site zijn gekomen.

Maar wat als u, in plaats van het bekijken van Campagnes enkel door het volgen code, campagneresultaten door de Motor van het Onderzoek, Trefwoord of het Kanaal van de Campagne wilt zien? Moet u een nieuwe omzettingsvariabele voor de Motor van het Onderzoek, een andere voor Sleutelwoord en een andere voor het Kanaal van de Campagne tot stand brengen? Als dat het geval is, zou u veel van uw vijftig variabelen alleen op Campagnes gebruiken! Gelukkig kun je classificaties gebruiken om je leven makkelijker te maken. Aangezien elke volgende code een de motor van het Onderzoek, Trefwoord of Kanaal van de Campagne kon hebben, kunt u drie Classificaties van de variabele van Campagnes eenvoudig creëren om elk te vertegenwoordigen. U vertelt in wezen SiteCatalyst dat er een directe relatie is tussen de variabele Campagnes en deze drie andere waarden van de ‘meta-data&#39;. Op deze manier kunt u met SiteCatalyst gebeurtenissen voor het voltooien van sites segmenteren en segmenteren met alle vier de variabelen zonder extra tags.

## SAINT scrubberscript in DWB {#section-a42bb9236d7d49bfabdc48d39ece3c3b}

Dit script wordt gebruikt wanneer u indelingsgegevens voor SAINT in DWB plaatst. Het script *SaintScrubber.dat* normaliter onder de *\Scripts\Scripts* op de FSU.

Het belangrijkste doel van dit script is het verwijderen van de koptekst in de `<discoiqbr>` SAINT Classificatiebestanden. Ook, telt het het aantal als de kolom die in de lijn van de kolomkopbal wordt vermeld en alle gegevensrijen controleert. Als er rijen zijn met minder of meer kolommen, worden deze rijen uit het bestand verwijderd.

De *SaintScrubber.dat* roept intern *saint_scrubber.pl *script. Hieronder vindt u de details voor dit scriptbestand:

Pad: *E:\Scripts\Scripository\Library\Perl*

Scriptargumenten:

1. Invoermap (verplicht): source_directory
1. Uitvoermap (verplicht): destination_directory
1. Scheidingsteken (verplicht) : scheidingsteken
1. Map afwijzen (optioneel) (parameter kan leeg blijven of uit de opdrachtregel worden weggelaten)
1. Logmap (optioneel) (parameter kan leeg blijven of uit de opdrachtregel worden weggelaten)

Stappen die worden uitgevoerd in het Perl-script:

1. Vervang escaped form feeds, newlines, carterreturns, tabs met spaties.
1. Verwijder die dubbele bytes die als controlekarakter in UTF-8 BMP (Standaard Meertalig Vlak) behalve worden geïnterpreteerd:

   * 9 horizontale tab
   * 10-lijnfeed
   * 12 formulierfeed
   * 13 terugreis
   * Gebruik het trefwoord pipe als scheidingsteken voor | bijv. scheidingsleiding
   * Andere storende tekens verwijderen
   * Na bovenstaande scrubben zet u regels neer met een aantal kolommen dat afwijkt van de eerste gegevensregel (niet leeg of opmerking)
   * Ondersteuning voor optionele verwerpingsbestanden voor het vasthouden van geweigerde regels in plaats van deze gewoon over te slaan
   * Recursieve invoermap ondersteunen; uitvoermappen met dezelfde structuur genereren
   * Verplaats verwerkte invoerbestanden naar verwerkte submappen zodat het script de bewerking niet herhaalt wanneer het opnieuw wordt uitgevoerd in dezelfde bestaande invoermap
   * Datum herkennen in werkbankbestandsnamen; sorteerbewerking eerst op datum en vervolgens alpha, ongeacht de mapnaam. Dit zal ervoor zorgen dat de opeenvolging ongeacht het werkbench dossiertype (ecom, niet-ecom) of rapportreeks identiteitskaart (als u veelvoudige rapportreeksen in één enkele dataset van het Inzicht verwerkt) correct is.
   * E-mailwaarschuwingen voor ondersteuning `<discoiqbr>`
