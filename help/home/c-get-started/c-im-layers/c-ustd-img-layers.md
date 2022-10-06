---
description: Conceptuele informatie over afbeeldingslagen.
title: Informatie over afbeeldingslagen
uuid: a8b00bda-c5b2-4f27-8c15-2d319b3bfa70
exl-id: c6d30747-70d2-4489-ad64-fd131e76a7a2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# Informatie over afbeeldingslagen{#about-imagery-layers}

{{eol}}

Conceptuele informatie over afbeeldingslagen.

## Typen afbeeldingslagen {#section-891cbf61e8334690bd203a2bb9761b25}

U kunt de volgende typen afbeeldingslagen weergeven in Data Workbench:

* **[!UICONTROL Terrain image layer]:** Dit type laag geeft terreinbeelden van de aarde weer, waarover geografische gegevens kunnen worden weergegeven. De wereldwijde visualisatie in is een voorbeeld van een achtergrondafbeeldingslaag. Zie [Werken met Terrain Image Layers](../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f).

* **[!UICONTROL Element point layer]:** Dit type van laag toont één punt op de bol voor elk element van een afmeting. Zie [Werken met elementpuntlagen](../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-layers.md#concept-7c93c54552844a20bd6014ae8446b3fd).

* **[!UICONTROL Vector layer]:** Bij dit type laag worden vectorgegevens (lijntekeningen) over de hele wereld weergegeven. Zie [Werken met vectorlagen](../../../home/c-get-started/c-im-layers/c-vctr-layers/c-vctr-layers.md#concept-a9b9cb7fc33b4aa5ae1646fab202dcc9).

* **[!UICONTROL Presentation layer]** Annoteer en verbeter visualisaties met behulp van een presentatie-overlay. Voeg tekstcall-outs, pijlen, beelden, en kleurencodering toe om uw gegevens te benadrukken en te verduidelijken, en dan met anderen te delen.

In Data Workbench, kunt u selecteren welke van deze lagen u voor een bepaalde analystaak wilt tonen.

## Geografische profiellagen {#section-d04ab9f1a8cd4c6580e48ce44ac51898}

De [!DNL Geography] profiel biedt u een set standaardafbeeldingslagen, die zijn opgeslagen in de map Profiles\Geography\Maps in de installatiemap van de Data Workbench-server:

* **[!UICONTROL Blue Marble 2km]:** Met deze achtergrondafbeeldingslaag maakt u een 3D-kaart van de wereld. Dit is wat wordt weergegeven wanneer u de wereldvisualisatie toevoegt aan een werkruimte. Als deze laag niet is geselecteerd, is de bol niet zichtbaar, maar worden de andere lagen wel weergegeven. De [!DNL Blue Marble 2km.layer] bestand verwijst naar de [!DNL Blue Marble 2km.tsi] bestand.

* **[!UICONTROL Zip Points]:** Deze laag van het elementenpunt laat u toe om plaatsen in uw dataset in kaart te brengen gebruikend een Code van het PIT van Verenigde Staten. De [!DNL Zip Points.txt] Het opzoekbestand (opgegeven door Adobe) bevat een lijst met alle ZIP-codes van de Verenigde Staten en de breedte en lengte van elke ZIP-code. De [!DNL Zip Points.layer] bestand verwijst naar de [!DNL Zip Points.txt] en de [!DNL Zipcode.dim] en bevat de configuratieparameters die nodig zijn om de locaties op de wereldbol weer te geven. Elk element van de dimensie van de Postcode ( [!DNL Zipcode.dim]) die u in uw gegevensset definieert, wordt op de wereld toegewezen met behulp van de lengte- en breedtegraad die voor die ZIP-code in de [!DNL Zip Points.txt] opzoekbestand.

   Voor informatie over het definiëren van afmetingen raadpleegt u de *Configuratie-handleiding voor gegevensset*.

* **[!UICONTROL Boundaries]:** Deze vectorlaag zorgt voor de belangrijkste politieke wereldgrenzen, zoals landen, en voor de grenzen van natuurlijke fysieke kenmerken van de aarde, zoals meren en eilanden. De [!DNL Boundaries.layer] verwijst naar een of meer van de [!DNL mwcoast.vec], [!DNL mwisland.vec], [!DNL mwlake.vec], [!DNL mwnation.vec], [!DNL mwriver.vec], [!DNL mwstate.vec], [!DNL US states.vec], en [!DNL world boundaries.vec] bestanden.

* **[!UICONTROL IP Coordinates]:** Deze elementpuntlaag gebruikt dynamische punten om u toe te laten om plaatsen in uw dataset in kaart te brengen gebruikend IP adressen. De [!DNL IP Coordinates.layer] bestand verwijst naar de coördinaatdimensie ( [!DNL Coordinates.dim]) en geeft de metrische waarde van de bezoekers op als de metrische waarde die moet worden gebruikt om de grootte van de punten op de bol voor elke coördinaat te bepalen.

Uw [!UICONTROL NL Geography] profiel of andere profielen in uw installatie kunnen extra afbeeldingslagen bevatten die door Adobe zijn verschaft of die uw bedrijf heeft gemaakt.

## Een nieuwe laag maken {#section-b5313773316c4e0fa748f7376a8e7f0b}

U kunt nieuwe afbeeldingslagen maken door het juiste type laagbestand te kopiëren dat is opgenomen in het dialoogvenster [!DNL Geography] profiel in om het even welke Profielen \*profielnaam* \ van Kaarten, dan hernoemen en het dossier uitgeven zoals aangewezen. Alle nieuwe lagen moeten aan de volgende vereisten voldoen:

* De [!DNL .layer] bestand moet de indeling van een van de ondersteunde laagtypen hebben.
* De [!DNL .layer] het bestand moet verwijzen naar de juiste opzoekings- en dimensiebestanden, indien nodig.
* Het referenced raadplegingsdossier moet ook binnen de de installatiemap van de server van de Data Workbench worden opgeslagen, en zijn weg moet nauwkeurig in worden gespecificeerd [!DNL .layer] bestand.

Voor meer informatie over het formaat en de parameters voor elk type van laagdossier en zijn bijbehorende dossiers, zie de sectie in dit hoofdstuk voor het aangewezen laagtype.
