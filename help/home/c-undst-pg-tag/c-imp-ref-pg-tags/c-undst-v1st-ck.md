---
description: De site gebruikt cookies om bezoekers van uw website op unieke wijze te identificeren en hun gedrag in de loop der tijd te volgen.
title: De v1st-cookie begrijpen
uuid: 6112cafe-51e3-42f0-8554-4a653dea782a
exl-id: c5e8e1cb-686b-4d31-821e-60beb2808f80
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# De v1st-cookie begrijpen{#understanding-the-v-st-cookie}

{{eol}}

De site gebruikt cookies om bezoekers van uw website op unieke wijze te identificeren en hun gedrag in de loop der tijd te volgen.

De eerste keer dat een bepaalde browser (als bezoeker beschouwd) een aanvraag voor uw website indient, [!DNL Sensor] werkt samen met uw webserver om een permanente cookie, cs(cookie)(v1st), in te stellen die intern in het systeem wordt geïnterpreteerd als x-trackingid. Deze permanente cookie wordt ingesteld naast eventuele andere cookies die uw site anders instelt. Met dit cookie kunt u uw bezoekers tijdens meerdere sessies bijhouden. Hierdoor zijn veel soorten analyses mogelijk die anders niet mogelijk zijn.

[!DNL Sensor] Wijst een 64-bits numerieke sleutel toe in het cookie om nieuwe bezoekers te identificeren die een aanvraag van de site indienen als een unieke id. Wanneer de [!DNL Sensor] ziet een verzoek van een browser, controleert het of &quot;cs(cookie)(v1st)&quot;, een &#39;first-party persistente cookie&#39; ingesteld door [!DNL Sensor], bestaat in de aanvraaggegevens. Als cs(cookie)(v1st) niet aanwezig is, [!DNL Sensor], geeft u de browser de opdracht deze in te stellen via uw webserver. In tegenstelling tot andere oplossingen [!DNL Sensor] kan deze cookie instellen op het eerste verzoek van de bezoeker.

Hieronder ziet u de standaard permanente cookieheader die op eerste verzoek van uw site door uw webserver naar de browser wordt gestuurd, op de richting van [!DNL Sensor]. De indeling kan op het moment van configuratie worden gedefinieerd als een andere naam of vervaldatum gewenst is. Bijvoorbeeld:

```
Set-Cookie:v1st=3D80DCA944D60E16; path=/; expires=Wed, 19 Feb 2020 14:28:00 GMT
```

Deze cookie wordt slechts eenmaal ingesteld op het allereerste verzoek dat die bezoeker aan uw site heeft gedaan. Deze wordt vervolgens bij die bezoeker verzameld telkens wanneer die browser in de toekomst een aanvraag voor uw site indient (pagina of verzoek om een ingesloten object). Het cookie is erg klein van formaat om de hoeveelheid bandbreedte te minimaliseren die wordt gebruikt om het naar uw servers over te brengen met elke aanvraag van die browser naar uw site.

Het accepteren van een permanente cookie is een beslissing van de browser. De meeste webgebruikers begrijpen wat cookies doen en herkennen ook dat cookies van de eerste partij een waardevol voordeel voor hen opleveren doordat ze site-inhoud aan hun voorkeuren kunnen aanpassen. Deze cookies van de eerste partij worden niet geblokkeerd door de standaardbeveiligingsinstellingen van populaire browsers. Als een gebruiker cookies van de eerste partij blokkeert, worden de aanvragen voor de paginaweergave nog steeds geregistreerd, maar kunnen de meetgegevens van die aanvragen niet betrouwbaar worden gecorreleerd met een bepaalde bezoeker of zijn sessies op de site. Veel sites, vooral geavanceerde dynamische sites, maken al gebruik van cookies van andere bedrijven, die in veel gevallen nodig zijn om webtoepassingen voor de bezoeker te laten werken. Een stap terug van een blijvend cookie is een sessiecookie, waardoor een reeks verzoeken kan worden samengevoegd tot een sessie, maar bezoekers niet kunnen worden bijgehouden tijdens een sessie. [!DNL Site] kan bezoekersgegevens sessioniseren op basis van sessiecookies of op basis van IP-nummer, maar beide methoden leiden aanzienlijk af van de typen en de waarde van de analyse die kunnen worden uitgevoerd met [!DNL Site] of een ander systeem voor de analyse en rapportage van webactiviteiten.
