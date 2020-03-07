---
description: Het dashboard vereist bepaalde read-only toestemmingen om tot uw gegevens van de gegevenswerkbank toegang te hebben en te kunnen tonen. Schrijfrechten zijn niet vereist.
solution: Analytics
title: Toegangsbeheer configureren
topic: Data workbench
uuid: 600b6799-547d-46da-9027-4f64943e2ccd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Toegangsbeheer configureren{#configuring-access-control}

Het dashboard vereist bepaalde read-only toestemmingen om tot uw gegevens van de gegevenswerkbank toegang te hebben en te kunnen tonen. Schrijfrechten zijn niet vereist.

Het vormen van toegangsbeheer impliceert het uitgeven van uw [!DNL Access Control.cfg] dossier op de FSU(s) en het toevoegen van een nieuwe groep om toestemming aan het dashboard van de gegevenswerkbank te verlenen:

1. Geef het [!DNL AccessControl.cfg] dossier (bij voorkeur gebruikend het werkstation van de gegevenswerkbank) uit.
1. Creeer een nieuwe groep genoemd de Toegang van het *Dashboard van het Inzicht*.
1. Onder de leden van deze groep, voeg juiste GN toe die aan u voor dit doel wordt verstrekt (Voorbeeld: CN:INSIGHT-USER01). De Zorg van de Klant van Adobe van het contact voor deze GN.
1. Onder de read-only toegang van deze groep, wijzig de lijst om op het volgende te wijzen:

* /Profielen/$
* /Profielen/
* /Adressen
* /Status/
* /Users/$

1. Verwijder om het even welke punten uit de read-write toegangssectie, aangezien geen schrijf toestemmingen voor het dashboard worden vereist.
1. Sparen de veranderingen in het [!DNL AccessControl.cfg] dossier aan de server voor toestemmingen om van kracht te worden.
