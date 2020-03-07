---
description: De testresultaten moeten duidelijk en zinvol zijn, zodat u er zeker van kunt zijn dat u op basis van deze resultaten beslissingen van grote dollars neemt.
solution: Insight,Analytics
title: Wat moet ik testen?
topic: Data workbench
uuid: 9dfe3685-885e-4098-ab1d-ac891ccc5199
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# Wat moet ik testen?{#what-should-i-test}

De testresultaten moeten duidelijk en zinvol zijn, zodat u er zeker van kunt zijn dat u op basis van deze resultaten beslissingen van grote dollars neemt.

Hoewel u diverse paginalay-outs met [!DNL Sensor] en Plaats kunt testen, stelt Adobe voor dat u zich bij het testen van hoge waarde, strategische bedrijfsinitiatieven, of nieuwe of opnieuw ontworpen websitefunctionaliteit concentreert die de doelstellingen richt die u voor uw website evenals voor uw zaken hebt geplaatst. U kunt op dergelijke kwesties zoals beste prijsgaranties, verpersoonlijkingsfunctionaliteit, marktaanbiedingen (bijvoorbeeld, pakketten of bundels), creatief ontwerp, en toepassingsprocessen testen.

De volgende concepten zijn het belangrijkst wanneer het ontwikkelen van uw gecontroleerd experiment:

* **Begrijp de juiste veranderingen aan te brengen.** Dit vereist wat onderzoek naar hoe uw website functioneert en de bedrijfsprocessen die aan de front-end website ten grondslag liggen. U wilt veranderingen aanbrengen die het meeste effect verstrekken en gemakkelijk kunnen worden getest.
* **Kleine veranderingen kunnen een aanzienlijke impact hebben.** Niet alle veranderingen die u test moeten drastisch zijn om een significante invloed op uw zaken te hebben. Altijd open staan voor kleine, maar zeer belangrijke veranderingen.

## Ondersteunde methodologieën {#section-1071adaf54c64ba9bc5ef228c4a23635}

Vele types van experimenten met vele verschillende doelstellingen kunnen worden uitgevoerd gebruikend Plaats. De volgende lijst verstrekt een paar voorbeelden:

* Het veranderen van pagina&#39;s, inhoud, en websiteprocessen om omzettingspercentages te verbeteren.
* Het veranderen van marketing campagnes, bevorderingen, dwars-verkoopt, en omhoog-verkoopt om opbrengst te verhogen.
* De variërende tijden van de paginalading om klantenkwaliteit van de dienst en de daadwerkelijke waarde van infrastructuurprestaties te begrijpen.

Om deze doelstellingen te bereiken, steunt de Plaats de volgende types van methodologieën voor gecontroleerde experimenteren en het testen:

* **Paginavervanging:** Vervang statische URL X met statische URL Y. Deze methodologie is van beperkte toepassing in een dynamische omgeving.
* **Dynamische URI-vervanging:** Dit is een variant van de Vervanging van de Pagina die statische pagina X met dynamische pagina Y vervangt om dynamische inhoud terug te geven.
* **Objectvervanging:** Vervang vast object X door vast object Y.
* **Vervanging van inhoud:** Vervang inhoud reeks X (veelvoudige voorwerpen, pagina&#39;s, lijst, etc.) met inhoud vastgestelde Y.
* **Experimentele variabele vervanging:** Vervang voorwerp JavaScript /writeCookie_X.js met voorwerp JavaScript /writeCookie_Y.js om een koekje te schrijven dat door een achterste deelsysteem kan worden gebruikt om bepaalde inhoud te dienen.

>[!NOTE]
>
>De gecontroleerde experimenten zijn gebaseerd op de vervanging van URI, niet de vervanging van het vraagkoord. URI binnen een bepaalde URL wordt benadrukt in het volgende voorbeeld:
>
>`http://www.omniture.com/index.asp?id=1`
>
>Bijvoorbeeld, in uw gecontroleerd experiment kon u specificeren dat de controlegroep URI met de testgroep URI [!DNL index.asp] wordt vervangen [!DNL index2.asp] om te bepalen welk paginaontwerp in meer waarde zou resulteren.
