---
description: Een legenda van de waarde toont bepaalde waardegebeurtenissen.
title: Waardelegenda
uuid: 7779f442-2f45-4bf8-a62a-585aaceaeb3a
exl-id: b28ba604-93ef-4081-ae55-937fb537c068
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Waardelegenda{#value-legends}

Een legenda van de waarde toont bepaalde waardegebeurtenissen.

De waarde legenda wordt gevormd slechts in de HBX en [!DNL Site] toepassingen, maar zij kunnen voor andere toepassingen worden gevormd. Neem voor meer informatie contact op met de Adobe Consulting Services.

In HBX en [!DNL Site] wordt een value-gebeurtenis gedefinieerd als een sessie die bedrijfswaarde heeft gegenereerd. Zo kunnen de records met gebeurtenisgegevens die aan bepaalde paginaweergaven zijn gekoppeld (bijvoorbeeld een pagina om u te bedanken voor uw bestelling of een pagina om de toepassing te voltooien) waardegebeurtenissen vertegenwoordigen voor een bedrijfsorganisatie.

Met waardegebeurtenissen kunt u de hoeveelheid waarde meten en bijhouden die door de website wordt gegenereerd. U kunt de bedrijfswaarde in dollars voor elke gebeurtenis beoordelen en vragen beantwoorden zoals:

* Wat is het meest winstgevende pad via de website?
* Welke referentie of campagne heeft de meeste waarde opgeleverd?

Voor elke gebeurtenis geeft de legenda de waarde per eenheid van de gebeurtenis (waarde per gebeurtenis) weer en de totale waarde die door de gebeurtenis wordt gegenereerd. Met de legenda kunt u gebeurtenissen voor waarden definiëren en wijzigen en er eenheidswaarden aan toewijzen.

In de volgende tabel worden de metriek weergegeven die betrekking heeft op waardegebeurtenissen.

| Metrisch | Beschrijving |
|---|---|
| Conversie | Het percentage sessies dat de bedrijfswaarde heeft gegenereerd |
| Waarde | De totale gegenereerde bedrijfswaarde in dollars |
| Gem. Waarde | De gemiddelde bedrijfswaarde die, in dollars per zitting wordt geproduceerd |

U kunt eenvoudig alles wat bezoekers op de website doen, definiëren als een waardegebeurtenis: het posten van een verzoek van de klantendienst, het voltooien van een toepassing, het bekijken van een stuk van inhoud, of het voltooien van een aankoop. Elke gebeurtenis value komt overeen met een gebruiker die een bepaalde pagina of set pagina&#39;s op de website opent en is gekoppeld aan een bedrijfswaarde in dollars. Stel bijvoorbeeld dat elke gebruiker die op de pagina &quot;Bedankt voor uw aankoop&quot; komt, een dekkingsbijdrage van gemiddeld $20 genereert. U zou een waardegebeurtenis voor die pagina bepalen die een waarde van $20 heeft.

## Nieuwe waardegebeurtenissen {#section-2ea4d168336e4d2e98b22b636ed43853} definiëren

**Een nieuwe waardegebeurtenis definiëren in HBX of[!DNL Site]**

Wanneer u een waardegebeurtenis maakt, sleept u websitepagina&#39;s die waarde vertegenwoordigen van een visualisatie naar een waardelegenda.

1. Open een waardelegenda.

   ![](assets/lgd_ValueLegend.png)

1. U kunt waardegebeurtenissen vanuit procesafbeeldingen, URI-paginatabellen of paginahiërarchieweergaven aan de legenda toevoegen:

   * Van een proceskaart, sleep knopen van de proceskaart aan de legenda.
   * Druk vanuit een URI-paginatabel op Ctrl+Alt en sleep een pagina van de tabel naar de legenda.
   * Klik in een paginahiërarchieweergave links van een knooppunt (map, pagina of groep) en sleep het knooppunt naar de legenda.

   ![](assets/client-leg.png)

   Met de muisaanwijzer wordt het woord &#39;&#39;Nee&#39;&#39; weergegeven totdat de muis de legenda bereikt.

1. Wijs in de legenda-waarde een bedrijfswaarde toe aan elke sessie waarvoor de gebeurtenis plaatsvindt:

   1. Klik in de kolom [!DNL Value per Event] op de cel die overeenkomt met de pagina die u als waardegebeurtenis hebt toegevoegd.
   1. Typ het dollarbedrag om voor de waarde van die gebeurtenis toe te wijzen en te drukken binnengaan.

   ![](assets/lgd_ValueLegend_Value.png)

   Standaard wordt de URL van de pagina die u als een gebeurtenis value hebt gedefinieerd, weergegeven in de legenda. U kunt desgewenst dubbelklikken op deze URL in de legenda om de bewerkingsmodus te activeren en de naam van de gebeurtenis te wijzigen. U kunt de waarde van een bepaalde gebeurtenis ook op elk gewenst moment bewerken. De server van de Data Workbench berekent automatisch op gebeurtenis-gebaseerde waarden zoals gemiddelde waarde en omzetting opnieuw.

Nadat u minstens één waardegebeurtenis hebt bepaald, wordt de dimensie van het Segment van de Waarde beschikbaar voor gebruik. Deze dimensie vertegenwoordigt de totale waarde die een bezoeker in alle sessies heeft gegenereerd.

## Waardegebeurtenissen {#section-25cd90a859384ca183c0fc0998f888cf} verwijderen

* Klik met de rechtermuisknop op de gewenste gebeurtenis en klik op **[!UICONTROL Delete Event]**.

   ![](assets/lgd_ValueLegend_deleteEvent.png)

>[!NOTE]
>
>De server van de Data Workbench berekent metriek over de volledige reeks gegevens die voor het profiel toegankelijk zijn u gebruikt. Door gebrek, [!DNL Data Workbench Server] berekent dergelijke metriek zoals Waarde, de Gebeurtenissen van de Waarde, Gemiddelde Waarde, en Omzetting over alle gegevens in de dataset van de analyse, zelfs als de gegevens niet uit de zelfde logische bron zijn.

## Exporteren naar Microsoft Excel {#section-feaa7a8eb8124fafbc74169bebaed6d8}

Zie [Venstergegevens exporteren](../../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349) voor informatie over het exporteren van vensters.
