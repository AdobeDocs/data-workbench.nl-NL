---
description: Wanneer een Webserver offline wegens een mislukking gaat, is de oplossing eenvoudig die een gebruiker van de Data Workbench met aangewezen voorrechten vereist om het dossier van de Verwerkingsmodus van het Logboek te openen Mode.cfg en identiteitskaart van de Sensor (in ons voorbeeld, WEB2) aan de "Off-line sectie van Bronnen"toe te voegen.
solution: Analytics
title: Het probleem oplossen
uuid: 19d47b06-be12-4adf-9eac-b16cf7131834
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Het probleem oplossen{#solving-the-problem}

Wanneer een Webserver offline wegens een mislukking gaat, is de oplossing eenvoudig die een gebruiker van de Data Workbench met aangewezen voorrechten vereist om het dossier van de Verwerkingsmodus van het Logboek te openen Mode.cfg en identiteitskaart van de Sensor (in ons voorbeeld, WEB2) aan de &quot;Off-line sectie van Bronnen&quot;toe te voegen.

Deze sectie van het dossier vertelt het [!DNL data workbench server] dat het geen gegevens van deze bron meer zou moeten verwachten omdat het, in feite, off-line is.

>[!NOTE]
>
>Deze wijziging hoeft niet te worden uitgevoerd door een Adobe Consultant. Iedereen die de juiste rechten heeft om het [!DNL Log Processing Mode.cfg] bestand te openen, kan deze wijziging doorvoeren.

Als WEB2 begint gegevens opnieuw te verzenden, [!DNL data workbench server] brengt de bron terug online en past vanaf tijd aan om op de laatste tijd te wijzen het gegevens van alle bronnen te wijzen waarvan het zich bewust is. Met andere woorden, nieuwe gegevens die in het systeem komen krijgen voorrang boven wat in het [!DNL Log Processing Mode.cfg file]systeem wordt geschreven.

Als WEB2 opnieuw offline gaat, zal van tijd opnieuw ophouden, en u zult het [!DNL Log Processing Mode.cfg] dossier opnieuw moeten uitgeven alhoewel het WEB2 reeds als off-line bron zou kunnen hebben vermeld. Dit is een artefact van het ontwerp van het product in overeenstemming met de definitie van het &quot;vanaf de tijd&quot;: de laatste keer dat het systeem gegevens voor alle bekende bronnen heeft.

Wanneer u meer Webservers (WEB4, WEB5, WEB6) toevoegt, en zij beginnen gegevens naar de [!DNL data workbench server]te verzenden, te hoeven u om niets te doen om de nieuwe bronnen te hebben [!DNL data workbench server] herkennen. Het systeem wordt zich er eenvoudigweg van bewust dat het gegevens van deze nieuwe bronnen zou moeten verwachten, zoals hierboven beschreven.
