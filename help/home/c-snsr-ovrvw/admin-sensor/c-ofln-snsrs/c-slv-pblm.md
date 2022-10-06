---
description: Wanneer een Webserver offline wegens een mislukking gaat, is de oplossing eenvoudig die een gebruiker van de Data Workbench met aangewezen voorrechten vereist om het dossier van de Verwerkingsmodus van het Logboek te openen Mode.cfg en identiteitskaart van de Sensor (in ons voorbeeld, WEB2) aan de "Off-line sectie van Bronnen"toe te voegen.
title: Het probleem oplossen
uuid: 19d47b06-be12-4adf-9eac-b16cf7131834
exl-id: 4a05dc06-360b-4c15-a881-81d350e95372
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Het probleem oplossen{#solving-the-problem}

{{eol}}

Wanneer een Webserver offline wegens een mislukking gaat, is de oplossing eenvoudig die een gebruiker van de Data Workbench met aangewezen voorrechten vereist om het dossier van de Verwerkingsmodus van het Logboek te openen Mode.cfg en identiteitskaart van de Sensor (in ons voorbeeld, WEB2) aan de &quot;Off-line sectie van Bronnen&quot;toe te voegen.

In deze sectie van het bestand wordt de [!DNL data workbench server] dat het geen gegevens meer mag verwachten van deze bron, omdat het in feite offline is.

>[!NOTE]
>
>Deze wijziging hoeft niet te worden uitgevoerd door een Adobe Consultant. Iedereen die de juiste rechten heeft om de [!DNL Log Processing Mode.cfg] kan deze wijziging aanbrengen.

Als WEB2 gegevens opnieuw begint te verzenden, [!DNL data workbench server] Hiermee plaatst u de bron weer online en past u de waarde Na-tijd aan om de laatste keer weer te geven dat de bron gegevens heeft ontvangen van alle bronnen waarvan de bron bekend is. Met andere woorden, nieuwe gegevens die in het systeem komen krijgen voorrang op gegevens die in het [!DNL Log Processing Mode.cfg file].

Als WEB2 opnieuw offline gaat, zal van tijd opnieuw ophouden, en u zult moeten uitgeven [!DNL Log Processing Mode.cfg] bestand opnieuw, ook al wordt WEB2 mogelijk al als een offline bron vermeld. Dit is een artefact van het ontwerp van het product in overeenstemming met de definitie van het &quot;vanaf de tijd&quot;: de laatste keer dat het systeem gegevens voor alle bekende bronnen heeft.

Wanneer u meer webservers toevoegt (WEB4, WEB5, WEB6), en worden gegevens naar de [!DNL data workbench server], hoeft u niets te doen om de [!DNL data workbench server] de nieuwe bronnen erkennen. Het systeem wordt zich er eenvoudigweg van bewust dat het gegevens van deze nieuwe bronnen zou moeten verwachten, zoals hierboven beschreven.
