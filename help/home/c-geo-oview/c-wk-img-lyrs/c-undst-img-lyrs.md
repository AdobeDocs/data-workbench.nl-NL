---
description: Conceptuele informatie over de het profiellagen van de Geografie, types van beeldlagen, en het creëren van nieuwe lagen.
title: Werken met afbeeldingslagen
uuid: 8f4618bf-d8bd-4d21-a29e-ab2871d781ca
exl-id: ffe084ec-db8b-46f4-8266-0f1b771b3349
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%

---

# Beeldlagen begrijpen{#understanding-imagery-layers}

Conceptuele informatie over de het profiellagen van de Geografie, types van beeldlagen, en het creëren van nieuwe lagen.

## Typen afbeeldingslagen {#section-ce25364651a04cd1b83f9ac7c231fa41}

Met de gegevenswerkbank [!DNL Geography] kunt u de volgende typen afbeeldingslagen weergeven in de gegevenswerkbank:

* **Terrain image layer:** This type of layer displays terrain imagery of the Earth, over welke geografische gegevens kunnen worden weergegeven. De wereldwijde visualisatie in de werkbank voor gegevens is een voorbeeld van een achtergrondafbeeldingslaag. Zie [Werken met Terrain Image Layers](../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf).

* **Elementpuntlaag:** Dit type laag geeft één punt op de bol weer voor elk element van een dimensie. Zie [Werken met elementpuntlagen](../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs.md#concept-52b3262ab4e042a18956be8809638af9).

* **Vectorlaag:** Bij dit type laag worden vectorgegevens (lijntekeningen) over de hele wereld weergegeven. Zie [Werken met vectorlagen](../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-wk-vctr-lyrs.md#concept-a2c9e8155f554cbe96ee3aaf44f2d620).

In de werkbank Gegevens kunt u selecteren welke van deze lagen u voor een bepaalde analystaak wilt tonen.

## Geografische profiellagen {#section-4d9fb9b357764493a4d97d2b4068bb67}

Het [!DNL Geography] profiel voorziet u van een reeks standaardbeeldlagen, die in Profiles\Geography\Maps folder within the data workbench server installation directory worden opgeslagen:

* **Blauw marmer 2 km:** Deze achtergrondafbeeldingslaag maakt een 3D-kaart van de wereld. Dit is wat wordt weergegeven wanneer u de wereldvisualisatie toevoegt aan een werkruimte. Als deze laag niet is geselecteerd, is de bol niet zichtbaar, maar worden de andere lagen wel weergegeven. Het [!DNL Blue Marble 2km.layer] dossier verwijst naar het [!DNL Blue Marble 2km.tsi] dossier.

   Voor informatie over het werken met de wereldvisualisatie, zie *Gids van de Gebruiker van de Data Workbench*.

* **Zip de Punten:** Deze laag van het elementenpunt laat u toe om plaatsen in uw dataset in kaart te brengen gebruikend een Code van het PIT van Verenigde Staten. Het opzoekbestand [!DNL Zip Points.txt] (opgegeven door Adobe) bevat een lijst met alle ZIP-codes van de Verenigde Staten en de breedte en lengte van elke ZIP-code. Het [!DNL Zip Points.layer] dossier verwijst naar [!DNL Zip Points.txt] dossier en [!DNL Zipcode.dim] dossier en bevat de configuratieparameters nodig om de plaatsen op de wereldbol te tonen. Elk element van de dimensie van de Code van het PIT ( [!DNL Zipcode.dim]) dat u binnen uw dataset bepaalt wordt in kaart gebracht op de wereldbol gebruikend de breedte en lengtegraad die voor die Code van het PIT in [!DNL Zip Points.txt] raadplegingsdossier worden vermeld.

   Voor informatie over het bepalen van afmetingen, zie *de Gids van de Configuratie van de Dataset.*

* **Grens:** Deze vectorlaag biedt de belangrijkste politieke wereldgrenzen, zoals landen, en de grenzen van natuurlijke fysieke eigenschappen van de aarde, zoals meren en eilanden. Het [!DNL Boundaries.layer]-bestand verwijst naar een of meer van de bestanden [!DNL mwcoast.vec], [!DNL mwisland.vec], [!DNL mwlake.vec], [!DNL mwnation.vec], [!DNL mwriver.vec], [!DNL mwstate.vec], [!DNL US states.vec] en [!DNL world boundaries.vec].

* **IP Coördinaten:** Deze laag van het elementenpunt gebruikt dynamische punten om u toe te laten om plaatsen in uw dataset in kaart te brengen gebruikend IP adressen. Het [!DNL IP Coordinates.layer] dossier verwijst naar de afmetingen van Coördinaten ( [!DNL Coordinates.dim]) en specificeert metrisch bezoekers als metrisch om de grootte van de punten op de bol voor elke coördinaat te bepalen.

Uw [!DNL Geography]-profiel of andere profielen in uw installatie kunnen aanvullende afbeeldingslagen bevatten die door Adobe zijn verschaft of die uw bedrijf heeft gemaakt.

## Nieuwe lagen maken {#section-dc5a2f31d5fc46f58b865b9bb89fcfd4}

U kunt nieuwe afbeeldingslagen maken door het juiste type laagbestand in het profiel [!DNL Geography] te kopiëren naar een willekeurige map Profielen\*profielnaam*\Maps, en vervolgens de naam van het bestand te wijzigen en het bestand te bewerken. Alle nieuwe lagen moeten aan de volgende vereisten voldoen:

* Het [!DNL .layer] dossier moet aan het formaat van één van de gesteunde laagtypes houden.
* Het [!DNL .layer] dossier moet de aangewezen raadpleging en de afmetingsdossiers van verwijzingen voorzien, indien nodig.
* Het opzoekbestand waarnaar wordt verwezen, moet ook worden opgeslagen in de installatiemap van de gegevenswerkbank en het pad ervan moet nauwkeurig worden opgegeven in het bestand [!DNL .layer].

Voor meer informatie over het formaat en de parameters voor elk type van laagdossier en zijn bijbehorende dossiers, zie de sectie in dit hoofdstuk voor het aangewezen laagtype.
