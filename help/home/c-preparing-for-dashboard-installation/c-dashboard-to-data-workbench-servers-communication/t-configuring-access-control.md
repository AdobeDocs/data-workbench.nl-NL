---
description: Het dashboard vereist bepaalde read-only toestemmingen om tot uw gegevens van de gegevenswerkbankwerkbank toegang te hebben en te tonen. Schrijfrechten zijn niet vereist.
title: Toegangsbeheer configureren
uuid: 600b6799-547d-46da-9027-4f64943e2ccd
exl-id: a9ff61bb-c519-4205-8fa8-bfd1986fcd60
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Het vormen Toegangsbeheer{#configuring-access-control}

Het dashboard vereist bepaalde read-only toestemmingen om tot uw gegevens van de gegevenswerkbankwerkbank toegang te hebben en te tonen. Schrijfrechten zijn niet vereist.

Het vormen van toegangsbeheer impliceert het uitgeven van uw [!DNL Access Control.cfg] dossier op FSU(s) en het toevoegen van een nieuwe groep om toestemming aan het dashboard van de gegevenswerkbank te verlenen:

1. Bewerk het [!DNL AccessControl.cfg]-bestand (bij voorkeur met het werkstation van de gegevenswerkbank).
1. Maak een nieuwe groep met de naam *Insight Dashboard Access*.
1. Voeg onder de leden van deze groep de juiste GN toe die u hiervoor hebt ontvangen (bijvoorbeeld: CN:INSIGHT-USER01). Neem contact op met de klantenservice van Adobe voor deze CN.
1. Onder de read-only toegang van deze groep, wijzig de lijst om het volgende te weerspiegelen:

* /Profielen/$
* /Profielen/
* /Adressen
* /Status/
* /Users/$

1. Verwijder om het even welke punten uit read-write toegangssectie, aangezien geen schrijftoestemmingen voor het dashboard worden vereist.
1. Sla de wijzigingen in het [!DNL AccessControl.cfg]-bestand op de server op, zodat de machtigingen van kracht worden.
