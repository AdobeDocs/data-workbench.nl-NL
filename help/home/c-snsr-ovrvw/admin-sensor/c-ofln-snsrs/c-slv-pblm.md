---
description: Wanneer een Webserver wegens een mislukking offline gaat, is de oplossing eenvoudige die een gebruiker van de Werkbank van Gegevens met aangewezen voorrechten vereist om het dossier van de Verwerking van het Logboek te openen Mode.cfg en identiteitskaart van de Sensor (in ons voorbeeld, WEB2) toe te voegen aan de "Off-line Bronnen"sectie.
solution: Insight
title: Het probleem oplossen
uuid: 19d47b06-be12-4adf-9eac-b16cf7131834
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het probleem oplossen{#solving-the-problem}

Wanneer een Webserver wegens een mislukking offline gaat, is de oplossing eenvoudige die een gebruiker van de Werkbank van Gegevens met aangewezen voorrechten vereist om het dossier van de Verwerking van het Logboek te openen Mode.cfg en identiteitskaart van de Sensor (in ons voorbeeld, WEB2) toe te voegen aan de &quot;Off-line Bronnen&quot;sectie.

Deze sectie van het dossier vertelt [!DNL data workbench server] dat het niet meer om het even welke gegevens van deze bron zou moeten verwachten omdat het, in feite, off-line is.

>[!NOTE]
>
>Deze verandering te hoeven niet door een Adviseur van Adobe worden uitgevoerd. Iedereen die de aangewezen voorrechten heeft om het [!DNL Log Processing Mode.cfg] dossier te openen kan deze verandering aanbrengen.

Als WEB2 begint om gegevens opnieuw te verzenden, [!DNL data workbench server] brengt de bron terug online en past op tijd aan om op de laatste tijd te wijzen het gegevens van alle bronnen ontving waarvan het zich bewust is. Met andere woorden, de nieuwe gegevens die in het systeem komen nemen belangrijkheid over wat in geschreven in het [!DNL Log Processing Mode.cfg file].

Als WEB2 opnieuw offline gaat, zal van tijd opnieuw ophouden, en u zult het [!DNL Log Processing Mode.cfg] dossier moeten opnieuw uitgeven alhoewel het WEB2 reeds zou kunnen hebben die als off-line bron wordt vermeld. Dit is een artefact van het ontwerp van het product dat in overeenstemming is met de definitie van het begrip &quot;op tijd&quot;: de laatste keer dat het systeem over gegevens voor alle bekende bronnen beschikt .

Wanneer u meer Webservers (WEB4, WEB5, WEB6) toevoegt, en zij beginnen verzendend gegevens naar de [!DNL data workbench server], te hoeven u om het even wat te doen niet om te hebben de nieuwe bronnen [!DNL data workbench server] erkennen. Het systeem wordt zich er simpelweg van bewust dat het gegevens van deze nieuwe bronnen zou moeten verwachten, zoals hierboven beschreven.
