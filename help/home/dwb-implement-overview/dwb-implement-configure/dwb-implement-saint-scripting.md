---
description: In deze sectie wordt het script van Saint Scrubber uitgelegd.
title: Scripting voor de SAINT-rubber
uuid: 2e5aa6f2-dadb-48a6-8443-69396530587c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Scripting voor de SAINT-rubber{#scripting-for-the-saint-scrubber}

In deze sectie wordt het script van Saint Scrubber uitgelegd.

## Overzicht van de SAINT-classificatie {#section-b840a99f10684bb4b58e844a515d0d79}

De classificatie is ook gekend door acroniem SAINT voor de Attributen die van de Katalysator SiteCatalyst en het Noemen Hulpmiddel invoeren.

Wanneer wij &quot;classificeren&quot;een variabele SiteCatalyst, u een verband tussen een variabele en meta-gegevens met betrekking tot die variabele vestigt. De classificaties worden het vaakst gebruikt in het gebied van Campagnes zodat zal ik dat als manier gebruiken om hen te verklaren. De meeste cliënten verzenden campagneverkeer naar hun plaats gebruikend een volgende code. Deze volgcode is een identificator die een specifiek sleutelwoord kan vertegenwoordigen dat op Google wordt gekocht, zoals &quot;goog123.&quot; Dit herkenningsteken wordt overgegaan in de variabele s.campagnes zodat kunt u zien welke gebeurtenissen van het plaatssucces plaatsvinden nadat de bezoekers aan uw plaats van die campagnecode komen.

Maar wat als, in plaats van het bekijken van Campagnes enkel door de volgende code, u campagneresultaten door de Motor van het Onderzoek of het Sleutelwoord of het Kanaal van de Campagne wilt zien? Moet u een nieuwe omzettingsvariabele voor de Motor van het Onderzoek, een andere voor Sleutelwoord en een andere voor het Kanaal van de Campagne tot stand brengen? Zo ja, dan zou u veel van uw vijftig variabelen alleen al op Campaigns gebruiken! Gelukkig kunt u Classificaties gebruiken om uw leven gemakkelijker te maken! Aangezien elke volgende code een Motor van het Onderzoek, een Sleutelwoord of Kanaal van de Campagne kon hebben, kunt u drie Classificaties van de variabele van Campagnes eenvoudig tot stand brengen om elk te vertegenwoordigen. U vertelt hoofdzakelijk SiteCatalyst dat er een direct verband tussen de variabele van Campagnes en deze drie andere &quot;meta-gegevens&quot;waarden is. Door dit te doen, zal SiteCatalyst u toestaan om de Gebeurtenissen van het Succes van de plaats door alle vier variabelen zonder extra het etiketteren te snijden en te ontdoen.

## SAINT scrubber Manuscript in DWB {#section-a42bb9236d7d49bfabdc48d39ece3c3b}

Dit manuscript wordt gebruikt wanneer u om het even welke gegevens van de Classificatie van SAINT in DWB brengt. Het manuscript *SaintScrubber.dat* wordt normaal geplaatst onder de *\Scripts\Scripository* omslag op FSU.

Het belangrijkste doel van dit manuscript is de kopbal in de dossiers van de Classificatie van `<discoiqbr>` SAINT te verwijderen. Ook, telt het het aantal als de kolom die in de lijn van de kolomkopbal wordt vermeld en controleert alle gegevensrijen. Als er rijen met minder of meer aantal kolommen zijn, dan verwijdert het deze rijen uit het dossier.

De *SaintScrubber.dat* roept intern *saint_scrubber.pl *script. Hieronder zijn de details voor dit manuscriptdossier:

Pad: *E:\Scripts\Scripository\Library\Perl*

Scriptargumenten:

1. Invoermap (verplicht): source_directory
1. Uitvoermap (verplicht) : destination_directory
1. Afbakening (verplicht) : afbakening
1. De Omslag van de verwerping (Facultatief) (De Parameter kan leeg worden verlaten of van de bevellijn worden weggelaten)
1. De Omslag van het logboek (Facultatieve) (De Parameter kan leeg worden verlaten of van de bevellijn worden weggelaten)

Stappen die in het Perl manuscript worden uitgevoerd:

1. Vervang ontsnapte vormvoer, newlines, wagenterugloop, lusjes met ruimten.
1. Verwijder die dubbele bytes die als controlekarakter in UTF-8 BMP (Basis Meertalige Vliegtuig) behalve worden geïnterpreteerd:

   * 9 horizontale tab
   * 10 lijnvoer
   * 12 formulier diervoeder
   * 13 terugreis
   * Gebruik het pijpsleutelwoord, als afbakening voor| bijvoorbeeld: scheidingsleiding
   * Andere storende tekens verwijderen
   * Na het bovengenoemde schrobben laat vallen om het even welke lijnen met een aantal kolommen verschillend van de eerste gegevenslijn (niet leeg of commentaar)
   * De facultatieve verwerpingsdossiers van de steun om verworpen lijnen te houden in plaats van enkel hen te overslaan
   * Steun recursieve inputomslag; produceer outputomslagen van de zelfde structuur
   * Verplaats verwerkte inputdossiers naar verwerkte subfolders zodat herhaalt het manuscript niet de inspanning wanneer opnieuw in werking gesteld op de zelfde bestaande inputomslag
   * Datum in werkbankbestandsnamen herkennen; sorteerbewerking eerst op datum en dan alpha- - ongeacht omslagnaam. Dit zal ervoor zorgen dat de opeenvolging correct is geen kwestie het type van werkbankdossier (om, niet-om) of identiteitskaart van de rapportreeks (als u veelvoudige rapportreeksen in één enkele dataset van het Inzicht verwerkt).
   * E-mailwaarschuwingen ondersteunen `<discoiqbr>`

