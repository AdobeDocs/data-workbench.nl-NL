---
description: Deze sectie verklaart hoe te om Primaire sleutels (het Volgen identiteitskaart) voor Data Workbench datasets voor schemaontwerp en implementatie tot stand te brengen.
title: Gegevensverwerking - Primaire sleutel voor het bouwen van gegevens
uuid: 7a12950e-6ac0-47d5-b4a8-0b50c48b04fa
exl-id: 9937038f-d011-4946-8a5b-cc724b611ae5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Gegevensverwerking - Primaire sleutel voor het bouwen van gegevens{#data-processing-building-primary-key}

{{eol}}

Deze sectie verklaart hoe te om Primaire sleutels (het Volgen identiteitskaart) voor Data Workbench datasets voor schemaontwerp en implementatie tot stand te brengen.

## Id voor bijhouden {#section-24683031044a4af49988655ccb9a45fd}

Na het lezen en decoderen van de gegevens in DWB (het gebruiken van decoders), is de eerste stap het bepalen van Tracking identiteitskaart en Tijdstempel. De volgende-id is een unieke identificatie voor een record van de klant. Dit kan elk veld in de feed zijn, zoals e-mailadres, burgerservicenummer, cookie-id, enzovoort. Het veld dat als volgnummer-id moet worden gebruikt, wordt door de client tijdens de detectiesessie bepaald. Tracking-id en tijdstempel zijn verplichte velden en moeten voor elke record worden gedefinieerd.

Doorgaans, voor online gegevens, Cookie-id (combinatie van *x-visid_high* en* x-visid_low*) wordt gebruikt als het standaardmechanisme voor unieke klantidentificatie, maar dit kan volgens de vereisten van de klant worden gewijzigd. De datum en het tijdstip waarop de aanvraag (of gebeurtenis) plaatsvindt, zijn: *x-timestamp*. Alle records in DWB worden gegroepeerd op *trackingid* en gesorteerd op tijdstempel. Het vereiste veld [!DNL Definitions.cfg] Het bestand is een Include-bestand van de gegevensset van de logbestandverwerking waarin de vereiste velden worden gedefinieerd: *x-trackingid* en *x-timestamp*.

Opmerking: *x-trackingid *in DWB is een ingebouwd veld en deze naam mag niet worden gebruikt voor andere velden.

**Voorbeeld 1**: Maken *x-trackingid* Cookie-id gebruiken (wanneer alleen onlinegegevens worden gebruikt)

Als u de *x-trackingid *in DWB wilt maken met Cookie-id, gebruikt u de functie Hash om de *x-trackingid* in de [!DNL foundation.cfg] bestand (het wordt aanbevolen de id voor bijhouden te definiëren in [!DNL foundation.cfg] maar het kan in om het even welk ander configuratiedossier onder worden bepaald [!DNL Dataset > log processing] map) zoals weergegeven:

![](assets/dwb_impl_primary_key1.png)

**Voorbeeld 2**: Maken *x-trackingid* e-mailadres gebruiken (wanneer zowel online als offline gegevens beschikbaar zijn)

Aangenomen dat zowel offline als online gegevens beschikbaar zijn (in dit voorbeeld) en de e-mailid beschikbaar is in beide gegevensbronnen. Aangezien de e-mailid een klant op unieke wijze identificeert, wordt deze gebruikt om de *x-trackingid*.

Gebruik de functie Hash om de *trackingId* zoals weergegeven:

![](assets/dwb_impl_primary_key2.png)
