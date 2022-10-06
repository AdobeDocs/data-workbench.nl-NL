---
description: Het dashboard vereist bepaalde read-only toestemmingen om tot uw gegevens van de gegevenswerkbankwerkbank toegang te hebben en te tonen. Schrijfrechten zijn niet vereist.
title: Toegangsbeheer dashboard configureren
uuid: 600b6799-547d-46da-9027-4f64943e2ccd
exl-id: a9ff61bb-c519-4205-8fa8-bfd1986fcd60
source-git-commit: 90b9fff995cb37a62024f454f009e9e0d7b927cd
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# Toegangsbeheer dashboard configureren{#configuring-dashboard-access-control}

{{eol}}

Het dashboard vereist bepaalde read-only toestemmingen om tot uw gegevens van de gegevenswerkbankwerkbank toegang te hebben en te tonen. Schrijfrechten zijn niet vereist.

Het vormen van toegangsbeheer impliceert het uitgeven van uw [!DNL Access Control.cfg] bestand op de FSU(&#39;s) en een nieuwe groep toevoegen om toestemming te verlenen aan het dashboard voor de gegevenswerkbank:

1. Bewerk de [!DNL AccessControl.cfg] bestand (bij voorkeur met het werkstation van de gegevenswerkbank).
1. Een nieuwe groep maken met de naam *Toegang dashboard tonen*.
1. Voeg onder de leden van deze groep de juiste GN toe die u hiervoor hebt ontvangen (Voorbeeld: CN:INSIGHT-USER01). Neem contact op met de klantenservice van Adobe voor deze CN.
1. Onder de read-only toegang van deze groep, wijzig de lijst om het volgende te weerspiegelen:

* /Profielen/$
* /Profielen/
* /Adressen
* /Status/
* /Users/$

1. Verwijder om het even welke punten uit read-write toegangssectie, aangezien geen schrijftoestemmingen voor het dashboard worden vereist.
1. Sla de wijzigingen op in het dialoogvenster [!DNL AccessControl.cfg] aan de server voor toestemmingen om van kracht te worden.
