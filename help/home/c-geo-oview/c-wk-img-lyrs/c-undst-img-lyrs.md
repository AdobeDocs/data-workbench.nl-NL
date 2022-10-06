---
description: Conceptuele informatie over de het profiellagen van de Geografie, types van beeldlagen, en het creëren van nieuwe lagen.
title: Werken met afbeeldingslagen
uuid: 8f4618bf-d8bd-4d21-a29e-ab2871d781ca
exl-id: ffe084ec-db8b-46f4-8266-0f1b771b3349
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%

---

# Werken met afbeeldingslagen{#understanding-imagery-layers}

{{eol}}

Conceptuele informatie over de het profiellagen van de Geografie, types van beeldlagen, en het creëren van nieuwe lagen.

## Typen afbeeldingslagen {#section-ce25364651a04cd1b83f9ac7c231fa41}

Gegevenswerkbank [!DNL Geography] kunt u de volgende typen afbeeldingslagen weergeven in de werkbank voor gegevens:

* **Terreinafbeeldingslaag:** Dit type laag geeft terreinbeelden van de aarde weer, waarover geografische gegevens kunnen worden weergegeven. De wereldwijde visualisatie in de werkbank voor gegevens is een voorbeeld van een achtergrondafbeeldingslaag. Zie [Werken met Terrain Image Layers](../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf).

* **Elementpuntlaag:** Dit type van laag toont één punt op de bol voor elk element van een afmeting. Zie [Werken met elementpuntlagen](../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs.md#concept-52b3262ab4e042a18956be8809638af9).

* **Vectorlaag:** Bij dit type laag worden vectorgegevens (lijntekeningen) over de hele wereld weergegeven. Zie [Werken met vectorlagen](../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-wk-vctr-lyrs.md#concept-a2c9e8155f554cbe96ee3aaf44f2d620).

In de werkbank Gegevens kunt u selecteren welke van deze lagen u voor een bepaalde analystaak wilt tonen.

## Geografische profiellagen {#section-4d9fb9b357764493a4d97d2b4068bb67}

De [!DNL Geography] profiel biedt u een set standaardafbeeldingslagen, die zijn opgeslagen in de map Profiles\Geography\Maps in de installatiemap van de gegevenswerkbench-server:

* **Blauwe marmer 2 km:** Met deze achtergrondafbeeldingslaag maakt u een 3D-kaart van de wereld. Dit is wat wordt weergegeven wanneer u de wereldvisualisatie toevoegt aan een werkruimte. Als deze laag niet is geselecteerd, is de bol niet zichtbaar, maar worden de andere lagen wel weergegeven. De [!DNL Blue Marble 2km.layer] bestand verwijst naar de [!DNL Blue Marble 2km.tsi] bestand.

   Voor informatie over het werken met de wereldvisualisatie raadpleegt u de *Gebruikershandleiding voor Data Workbench*.

* **Zip-punten:** Deze laag van het elementenpunt laat u toe om plaatsen in uw dataset in kaart te brengen gebruikend een Code van het PIT van Verenigde Staten. De [!DNL Zip Points.txt] Het opzoekbestand (opgegeven door Adobe) bevat een lijst met alle ZIP-codes van de Verenigde Staten en de breedte en lengte van elke ZIP-code. De [!DNL Zip Points.layer] bestand verwijst naar de [!DNL Zip Points.txt] en de [!DNL Zipcode.dim] en bevat de configuratieparameters die nodig zijn om de locaties op de wereldbol weer te geven. Elk element van de dimensie van de Postcode ( [!DNL Zipcode.dim]) die u in uw gegevensset definieert, wordt op de wereld toegewezen met behulp van de lengte- en breedtegraad die voor die ZIP-code in de [!DNL Zip Points.txt] opzoekbestand.

   Voor informatie over het definiëren van afmetingen raadpleegt u de *De configuratiehandleiding voor de gegevensset.*

* **Grenzen:** Deze vectorlaag zorgt voor de belangrijkste politieke wereldgrenzen, zoals landen, en voor de grenzen van natuurlijke fysieke kenmerken van de aarde, zoals meren en eilanden. De [!DNL Boundaries.layer] verwijst naar een of meer van de [!DNL mwcoast.vec], [!DNL mwisland.vec], [!DNL mwlake.vec], [!DNL mwnation.vec], [!DNL mwriver.vec], [!DNL mwstate.vec], [!DNL US states.vec], en [!DNL world boundaries.vec] bestanden.

* **IP-coördinaten:** Deze elementpuntlaag gebruikt dynamische punten om u toe te laten om plaatsen in uw dataset in kaart te brengen gebruikend IP adressen. De [!DNL IP Coordinates.layer] bestand verwijst naar de coördinaatdimensie ( [!DNL Coordinates.dim]) en geeft de metrische waarde van de bezoekers op als de metrische waarde die moet worden gebruikt om de grootte van de punten op de bol voor elke coördinaat te bepalen.

Uw [!DNL Geography] profiel of andere profielen in uw installatie kunnen extra afbeeldingslagen bevatten die door Adobe zijn verschaft of die uw bedrijf heeft gemaakt.

## Nieuwe lagen maken {#section-dc5a2f31d5fc46f58b865b9bb89fcfd4}

U kunt nieuwe afbeeldingslagen maken door het juiste type laagbestand te kopiëren dat is opgenomen in het dialoogvenster [!DNL Geography] profiel in om het even welke Profielen \*profielnaam* \ van Kaarten, dan hernoemen en het dossier uitgeven zoals aangewezen. Alle nieuwe lagen moeten aan de volgende vereisten voldoen:

* De [!DNL .layer] bestand moet de indeling van een van de ondersteunde laagtypen hebben.
* De [!DNL .layer] het bestand moet verwijzen naar de juiste opzoekings- en dimensiebestanden, indien nodig.
* Het referentieopzoekbestand moet ook worden opgeslagen in de installatiemap van de gegevenswerkbench-server en het pad ervan moet nauwkeurig worden opgegeven in de [!DNL .layer] bestand.

Voor meer informatie over het formaat en de parameters voor elk type van laagdossier en zijn bijbehorende dossiers, zie de sectie in dit hoofdstuk voor het aangewezen laagtype.
