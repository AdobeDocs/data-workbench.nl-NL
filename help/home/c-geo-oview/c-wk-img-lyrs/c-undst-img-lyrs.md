---
description: De conceptuele Informatie over de het profiellagen van de Geografie, types van beeldlagen, en het creëren van nieuwe lagen.
solution: Analytics
title: Beeldlagen begrijpen
topic: Data workbench
uuid: 8f4618bf-d8bd-4d21-a29e-ab2871d781ca
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Beeldlagen begrijpen{#understanding-imagery-layers}

De conceptuele Informatie over de het profiellagen van de Geografie, types van beeldlagen, en het creëren van nieuwe lagen.

## Typen afbeeldingslagen {#section-ce25364651a04cd1b83f9ac7c231fa41}

De werkbank van gegevens [!DNL Geography] laat u toe om de volgende types van beeldlagen in gegevenswerkbank te bekijken:

* **Afbeeldingslaag voor terrein:** Dit type van laag toont terreinbeelden van de Aarde, waarover geografische gegevens kunnen worden getoond. De globe visualisatie in gegevenswerkbank is een voorbeeld van een laag van het terreinbeeld. Zie [Werken met Afbeeldingslagen](../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf)voor Terrain.

* **Element puntlaag:** Dit type van laag toont één punt op de bol voor elk element van een afmeting. Zie het [Werken met de Lagen](../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs.md#concept-52b3262ab4e042a18956be8809638af9)van het Punt van het Element.

* **Vectorlaag:** Dit type van laagvertoningen vectorgegevens (lijnkunst) op de bol. Zie [Werken met vectorlagen](../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-wk-vctr-lyrs.md#concept-a2c9e8155f554cbe96ee3aaf44f2d620).

In gegevenswerkbank, kunt u selecteren welke van deze lagen u voor een bepaalde analysetaak wilt tonen.

## Lagen geografisch profiel {#section-4d9fb9b357764493a4d97d2b4068bb67}

Het [!DNL Geography] profiel voorziet u van een reeks standaardbeeldlagen, die in Profiles\Geography\Maps folder within the data workbench server installation directory worden opgeslagen:

* **Blauwe marmer 2 km:** Deze laag van het terreinbeeld leidt tot een kaart 3-D van de wereld, die is wat toont wanneer u de globe visualisatie aan een werkruimte toevoegt. Wanneer deze laag niet wordt geselecteerd, is de bol niet zichtbaar maar de andere lagen tonen nog. De [!DNL Blue Marble 2km.layer] dossierverwijzingen het [!DNL Blue Marble 2km.tsi] dossier.

   Voor informatie over het werken met de globale visualisatie, zie de Gids van de Gebruiker van de Werkbank van *Gegevens*.

* **Zip-punten:** Deze laag van het elementenpunt laat u toe om plaatsen in uw dataset in kaart te brengen gebruikend een Code van het PIT van Verenigde Staten. Het [!DNL Zip Points.txt] raadplegingsdossier (dat door Adobe wordt verstrekt) bevat een lijst van alle Codes van het ZIP van de Verenigde Staten en de breedte en de lengtegraad van elke Code van het PIT. De [!DNL Zip Points.layer] dossierverwijzingen het [!DNL Zip Points.txt] dossier en het [!DNL Zipcode.dim] dossier en bevatten de configuratieparameters nodig om de plaatsen op de bol te tonen. Elk element van de dimensie van de Code van het PIT ( [!DNL Zipcode.dim]) dat u binnen uw dataset bepaalt wordt in kaart gebracht op de bol gebruikend de breedte en de lengtegraad die voor die Code van het PIT in het [!DNL Zip Points.txt] raadplegingsdossier worden vermeld.

   Voor informatie over het bepalen van afmetingen, zie de Gids van de Configuratie van de *Dataset.*

* **Grenzen:** Deze vectorlaag biedt de belangrijkste politieke wereldgrenzen, zoals landen, en de grenzen van natuurlijke fysieke kenmerken van de aarde, zoals meren en eilanden. De [!DNL Boundaries.layer] dossierverwijzingen één of meer van [!DNL mwcoast.vec], [!DNL mwisland.vec], [!DNL mwlake.vec], [!DNL mwnation.vec], [!DNL mwriver.vec], [!DNL mwstate.vec], [!DNL US states.vec], en [!DNL world boundaries.vec] dossiers.

* **IP-coördinaten:** Deze laag van het elementenpunt gebruikt dynamische punten om u toe te laten om plaatsen in uw dataset in kaart te brengen gebruikend IP adressen. De [!DNL IP Coordinates.layer] dossierverwijzingen de afmeting van Coördinaten ( [!DNL Coordinates.dim]) en specificeert metrisch de Bezoekers als metrisch om de grootte van de punten op de bol voor elke coördinaat te bepalen te gebruiken.

Uw [!DNL Geography] profiel of andere profielen in uw installatie kunnen extra beeldlagen bevatten die Adobe verstrekte of uw bedrijf creeerde.

## Nieuwe lagen maken {#section-dc5a2f31d5fc46f58b865b9bb89fcfd4}

U kunt nieuwe beeldlagen tot stand brengen door het aangewezen type van laagdossier te kopiëren inbegrepen in het [!DNL Geography] profiel in om het even welke omslag van Profielen \*profielnaam* \ van Kaarten, dan het anders noemen en het uitgeven van het dossier zoals aangewezen. Alle nieuwe lagen moeten aan de volgende eisen voldoen:

* Het [!DNL .layer] dossier moet aan het formaat van één van de gesteunde laagtypes houden.
* Het [!DNL .layer] dossier moet de aangewezen raadpleging en de afmetingsdossiers van verwijzingen voorzien, indien nodig.
* Het referenced raadplegingsdossier moet ook binnen de de installatiefolder van de gegevenswerkbank worden opgeslagen, en zijn weg moet nauwkeurig in het [!DNL .layer] dossier worden gespecificeerd.

Voor meer informatie over het formaat en de parameters voor elk type van laagdossier en zijn bijbehorende dossiers, zie de sectie in dit hoofdstuk voor het aangewezen laagtype.
