---
description: Conceptuele informatie over afbeeldingslagen.
solution: Analytics
title: Informatie over afbeeldingslagen
topic: Data workbench
uuid: a8b00bda-c5b2-4f27-8c15-2d319b3bfa70
translation-type: tm+mt
source-git-commit: f4b37f50b115a1e1d2c9d000897a8fa47b03b233
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---


# Informatie over afbeeldingslagen{#about-imagery-layers}

Conceptuele informatie over afbeeldingslagen.

## Typen afbeeldingslagen {#section-891cbf61e8334690bd203a2bb9761b25}

U kunt de volgende typen afbeeldingslagen weergeven in Data Workbench:

* **[!UICONTROL Terrain image layer]:** Dit type laag geeft terreinbeelden van de aarde weer, waarover geografische gegevens kunnen worden weergegeven. De wereldwijde visualisatie in is een voorbeeld van een achtergrondafbeeldingslaag. Zie [Werken met Terrain Image Layers](../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f).

* **[!UICONTROL Element point layer]:** Dit type van laag toont één punt op de bol voor elk element van een afmeting. Zie [Werken met elementpuntlagen](../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-layers.md#concept-7c93c54552844a20bd6014ae8446b3fd).

* **[!UICONTROL Vector layer]:** Bij dit type laag worden vectorgegevens (lijntekeningen) over de hele wereld weergegeven. Zie [Werken met vectorlagen](../../../home/c-get-started/c-im-layers/c-vctr-layers/c-vctr-layers.md#concept-a9b9cb7fc33b4aa5ae1646fab202dcc9).

* **[!UICONTROL Presentation layer]** Annoteer en verbeter visualisaties met behulp van een presentatie-overlay. Voeg tekstcall-outs, pijlen, beelden, en kleurencodering toe om uw gegevens te benadrukken en te verduidelijken, en dan met anderen te delen.

In Data Workbench, kunt u selecteren welke van deze lagen u voor een bepaalde analystaak wilt tonen.

## Geografische profiellagen {#section-d04ab9f1a8cd4c6580e48ce44ac51898}

Het [!DNL Geography] profiel voorziet u van een reeks standaardbeeldlagen, die in Profiles\Geography\Maps folder within the Data Workbench server installation directory worden opgeslagen:

* **[!UICONTROL Blue Marble 2km]:** Met deze achtergrondafbeeldingslaag maakt u een 3D-kaart van de wereld. Dit is wat wordt weergegeven wanneer u de wereldvisualisatie toevoegt aan een werkruimte. Als deze laag niet is geselecteerd, is de bol niet zichtbaar, maar worden de andere lagen wel weergegeven. Het [!DNL Blue Marble 2km.layer] bestand verwijst naar het [!DNL Blue Marble 2km.tsi] bestand.

* **[!UICONTROL Zip Points]:** Deze laag van het elementenpunt laat u toe om plaatsen in uw dataset in kaart te brengen gebruikend een Code van het PIT van Verenigde Staten. Het [!DNL Zip Points.txt] opzoekbestand (opgegeven door Adobe) bevat een lijst met alle ZIP-codes van de Verenigde Staten en de breedte en lengte van elke ZIP-code. Het [!DNL Zip Points.layer] dossier verwijst naar het [!DNL Zip Points.txt] dossier en het [!DNL Zipcode.dim] dossier en bevat de configuratieparameters nodig om de plaatsen op de bol te tonen. Elk element van de dimensie van de Code van het PIT ( [!DNL Zipcode.dim]) dat u binnen uw dataset bepaalt wordt in kaart gebracht op de wereldbol gebruikend de breedte en lengtegraad die voor die Code van het PIT in het [!DNL Zip Points.txt] raadplegingsdossier worden vermeld.

   Voor informatie over het bepalen van afmetingen, zie de Gids *van de Configuratie van de* Dataset.

* **[!UICONTROL Boundaries]:** Deze vectorlaag zorgt voor de belangrijkste politieke wereldgrenzen, zoals landen, en voor de grenzen van natuurlijke fysieke kenmerken van de aarde, zoals meren en eilanden. Het [!DNL Boundaries.layer] bestand verwijst naar een of meer [!DNL mwcoast.vec], [!DNL mwisland.vec], [!DNL mwlake.vec], [!DNL mwnation.vec], [!DNL mwriver.vec], [!DNL mwstate.vec], [!DNL US states.vec], en [!DNL world boundaries.vec] bestanden.

* **[!UICONTROL IP Coordinates]:** Deze elementpuntlaag gebruikt dynamische punten om u toe te laten om plaatsen in uw dataset in kaart te brengen gebruikend IP adressen. Het [!DNL IP Coordinates.layer] dossier verwijst naar de afmetingen van Coördinaten ( [!DNL Coordinates.dim]) en specificeert metrisch bezoekers als metrisch om de grootte van de punten op de bol voor elke coördinaat te bepalen.

Uw [!UICONTROL NL Geography] profiel of andere profielen in uw installatie kunnen extra afbeeldingslagen bevatten die door Adobe zijn verschaft of die uw bedrijf heeft gemaakt.

## Een nieuwe laag maken {#section-b5313773316c4e0fa748f7376a8e7f0b}

U kunt nieuwe afbeeldingslagen maken door het juiste type laagbestand dat in het [!DNL Geography] profiel is opgenomen, te kopiëren naar een willekeurige map Profielen\*profielnaam*\Maps, en vervolgens de naam van het bestand te wijzigen en het bestand te bewerken. Alle nieuwe lagen moeten aan de volgende vereisten voldoen:

* Het [!DNL .layer] bestand moet de indeling van een van de ondersteunde laagtypen hebben.
* Het [!DNL .layer] bestand moet indien nodig verwijzen naar de juiste opzoekings- en afmetingsbestanden.
* Het referenced raadplegingsdossier moet ook binnen de de installatiemap van de server van de Data Workbench worden opgeslagen, en zijn weg moet nauwkeurig in het [!DNL .layer] dossier worden gespecificeerd.

Voor meer informatie over het formaat en de parameters voor elk type van laagdossier en zijn bijbehorende dossiers, zie de sectie in dit hoofdstuk voor het aangewezen laagtype.
