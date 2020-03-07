---
description: Conceptuele informatie over beeldlagen.
solution: Analytics
title: Informatie over afbeeldingslagen
topic: Data workbench
uuid: a8b00bda-c5b2-4f27-8c15-2d319b3bfa70
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Informatie over afbeeldingslagen{#about-imagery-layers}

Conceptuele informatie over beeldlagen.

## Typen beeldlagen {#section-891cbf61e8334690bd203a2bb9761b25}

U kunt de volgende types van beeldlagen in de Werkbank van Gegevens bekijken:

* **[!UICONTROL Terrain image layer]:**Dit type van laag toont terreinbeelden van de Aarde, waarover geografische gegevens kunnen worden getoond. De globe visualisatie in is een voorbeeld van een laag van het terreinbeeld. Zie[Werken met Afbeeldingslagen](../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f)voor Terrain.

* **[!UICONTROL Element point layer]:**Dit type van laag toont één punt op de bol voor elk element van een afmeting. Zie het[Werken met de Lagen](../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-layers.md#concept-7c93c54552844a20bd6014ae8446b3fd)van het Punt van het Element.

* **[!UICONTROL Vector layer]:**Dit type van laagvertoningen vectorgegevens (lijnkunst) op de bol. Zie[Werken met vectorlagen](../../../home/c-get-started/c-im-layers/c-vctr-layers/c-vctr-layers.md#concept-a9b9cb7fc33b4aa5ae1646fab202dcc9).

* **[!UICONTROL Presentation layer]** Annoteer en verduidelijk visualisaties gebruikend een presentatiebekleding. Voeg tekstvraag-outs, pijlen, beelden, en kleurencodage toe om uw gegevens te benadrukken en te verduidelijken, en dan met anderen te delen.

In de Werkbank van Gegevens, kunt u selecteren welke van deze lagen u voor een bepaalde analysetaak wilt tonen.

## Geografische profiellagen {#section-d04ab9f1a8cd4c6580e48ce44ac51898}

Het [!DNL Geography] profiel voorziet u van een reeks standaardbeeldlagen, die in Profiles\Geography\Maps folder within the Data Workbench server installation directory worden opgeslagen:

* **[!UICONTROL Blue Marble 2km]:**Deze laag van het terreinbeeld leidt tot een kaart 3-D van de wereld, die is wat toont wanneer u de globe visualisatie aan een werkruimte toevoegt. Wanneer deze laag niet wordt geselecteerd, is de bol niet zichtbaar maar de andere lagen tonen nog. De[!DNL Blue Marble 2km.layer]dossierverwijzingen het[!DNL Blue Marble 2km.tsi]dossier.

* **[!UICONTROL Zip Points]:**Deze laag van het elementenpunt laat u toe om plaatsen in uw dataset in kaart te brengen gebruikend een Code van het PIT van Verenigde Staten. Het[!DNL Zip Points.txt]raadplegingsdossier (dat door Adobe wordt verstrekt) bevat een lijst van alle Codes van het ZIP van de Verenigde Staten en de breedte en de lengtegraad van elke Code van het PIT. De[!DNL Zip Points.layer]dossierverwijzingen het[!DNL Zip Points.txt]dossier en het[!DNL Zipcode.dim]dossier en bevatten de configuratieparameters nodig om de plaatsen op de bol te tonen. Elk element van de dimensie van de Code van het PIT ([!DNL Zipcode.dim]) dat u binnen uw dataset bepaalt wordt in kaart gebracht op de bol gebruikend de breedte en de lengtegraad die voor die Code van het PIT in het[!DNL Zip Points.txt]raadplegingsdossier worden vermeld.

   Voor informatie over het bepalen van afmetingen, zie de Gids *van de Configuratie van de* Dataset.

* **[!UICONTROL Boundaries]:**Deze vectorlaag biedt de belangrijkste politieke wereldgrenzen, zoals landen, en de grenzen van natuurlijke fysieke kenmerken van de aarde, zoals meren en eilanden. De[!DNL Boundaries.layer]dossierverwijzingen één of meer van[!DNL mwcoast.vec],[!DNL mwisland.vec],[!DNL mwlake.vec],[!DNL mwnation.vec],[!DNL mwriver.vec],[!DNL mwstate.vec],[!DNL US states.vec], en[!DNL world boundaries.vec]dossiers.

* **[!UICONTROL IP Coordinates]:**Deze laag van het elementenpunt gebruikt dynamische punten om u toe te laten om plaatsen in uw dataset in kaart te brengen gebruikend IP adressen. De[!DNL IP Coordinates.layer]dossierverwijzingen de afmeting van Coördinaten ([!DNL Coordinates.dim]) en specificeert metrisch de Bezoekers als metrisch om de grootte van de punten op de bol voor elke coördinaat te bepalen te gebruiken.

Uw profiel van de [!UICONTROLNL Geografie] of andere profielen in uw installatie kunnen extra beeldlagen bevatten die Adobe verstrekte of uw bedrijf creeerde.

## Een nieuwe laag maken {#section-b5313773316c4e0fa748f7376a8e7f0b}

U kunt nieuwe beeldlagen tot stand brengen door het aangewezen type van laagdossier te kopiëren inbegrepen in het [!DNL Geography] profiel in om het even welke omslag van Profielen \*profielnaam* \ van Kaarten, dan het anders noemen en het uitgeven van het dossier zoals aangewezen. Alle nieuwe lagen moeten aan de volgende eisen voldoen:

* Het [!DNL .layer] dossier moet aan het formaat van één van de gesteunde laagtypes houden.
* Het [!DNL .layer] dossier moet de aangewezen raadpleging en de afmetingsdossiers van verwijzingen voorzien, indien nodig.
* Het referenced raadplegingsdossier moet ook binnen de de serverinstallatiefolder van de Werkbank van Gegevens worden opgeslagen, en zijn weg moet nauwkeurig in het [!DNL .layer] dossier worden gespecificeerd.

Voor meer informatie over het formaat en de parameters voor elk type van laagdossier en zijn bijbehorende dossiers, zie de sectie in dit hoofdstuk voor het aangewezen laagtype.
