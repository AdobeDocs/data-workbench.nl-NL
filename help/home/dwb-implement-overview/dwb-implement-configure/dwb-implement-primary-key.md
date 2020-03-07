---
description: Deze sectie verklaart hoe te om Primaire sleutels (het Volgen identiteitskaart) voor de datasets van de Werkbank van Gegevens voor schemaontwerp en implementatie tot stand te brengen.
title: Gegevensverwerking - Primaire sleutel voor gebouwen
uuid: 7a12950e-6ac0-47d5-b4a8-0b50c48b04fa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gegevensverwerking - Primaire sleutel voor gebouwen{#data-processing-building-primary-key}

Deze sectie verklaart hoe te om Primaire sleutels (het Volgen identiteitskaart) voor de datasets van de Werkbank van Gegevens voor schemaontwerp en implementatie tot stand te brengen.

## Begrijpend het Volgen identiteitskaart {#section-24683031044a4af49988655ccb9a45fd}

Na het lezen van en het decoderen van de gegevens in DWB (het gebruiken van decoders), is de eerste stap het Volgende Identiteitskaart en Timestamp te bepalen. Het volgen identiteitskaart is een herkenningsteken dat uniek een verslag van de Klant identificeert. Het kan om het even welk gebied in het voer zoals e-mail-identiteitskaart, het Aantal van de Sociale Zekerheid, identiteitskaart van de Koekje, enz. zijn Het gebied dat als het Volgen identiteitskaart moet worden gebruikt wordt beslist door de cliënt tijdens de ontdekkingszitting. VolgID en Timestamp zijn verplichte gebieden en moeten voor elke verslag worden bepaald.

Gewoonlijk wordt Cookie-ID (combinatie van *x-visid_high* en* x-visid_low*) voor online gegevens gebruikt als standaardmechanisme voor unieke klantidentificatie, maar deze kan worden gewijzigd volgens de vereisten van de klant. De datum en het tijdstip waarop het verzoek (of de gebeurtenis) voorkomt is *x-timestamp*. Alle verslagen in DWB zijn groep door identiteitskaart *te* volgen en op timestamp te sorteren. Het vereiste [!DNL Definitions.cfg] dossier van het Gebied is een Dataset van de Verwerking van het Logboek omvat dossier dat de vereiste gebieden bepaalt: *x-trackingid* en *x-timestamp*.

Opmerking: *x-trackingid *in DWB is een ingebouwd gebied en deze naam zou niet voor een ander gebied moeten worden gebruikt.

**Voorbeeld 1**: Het creëren van *x-trackingidentiteitskaart* die identiteitskaart van het Koekje gebruikt (wanneer slechts het online gegeven wordt gebruikt)

Om *x-trackingid *in DWB tot stand te brengen die identiteitskaart van het Koekje gebruikt, gebruik de functie van de knoeiboel om *x-trackingid* in het [!DNL foundation.cfg] dossier tot stand te brengen (het is een beste praktijk om volgende identiteitskaart binnen te bepalen [!DNL foundation.cfg] maar het kan in een ander configuratiedossier onder [!DNL Dataset > log processing] omslag worden bepaald) zoals getoond:

![](assets/dwb_impl_primary_key1.png)

**Voorbeeld 2**: Het creëren van *x-trackingidentiteitskaart* gebruikend E-mail-identiteitskaart (wanneer zowel online als off-line gegevens beschikbaar zijn)

Veronderstellend, zowel zijn de off-line als online gegevens beschikbaar (bijvoorbeeld), en e-mailidentiteitskaart is beschikbaar in beide gegevensbronnen. Aangezien, zal identiteitskaart E-mail uniek een klant identificeert, zal het worden gebruikt om *x-trackingidentiteitskaart* tot stand te brengen.

Gebruik de functie van de Hash om *trackingId* tot stand te brengen zoals getoond:

![](assets/dwb_impl_primary_key2.png)

