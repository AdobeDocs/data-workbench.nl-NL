---
description: Informatie over het oplossen van de problemen van de Webserver, zoals, als de Webserver uit omwenteling wordt verwijderd, of als de Webserver ontbreekt.
solution: Insight
title: Begrijpen van de Oorzaken
uuid: a2801040-c859-4bf8-90d7-daf3d4f633f3
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Begrijpen van de Oorzaken{#understanding-the-causes}

Informatie over het oplossen van de problemen van de Webserver, zoals, als de Webserver uit omwenteling wordt verwijderd, of als de Webserver ontbreekt.

## Wanneer een Server van het Web uit Omwenteling wordt genomen {#section-b9f709099cb44b4f9d1acb38ca5330e3}

Wanneer een Webserver uit omwenteling van een pool van servers wordt genomen, maar anders verbonden met de zender die periodieke hartslagen verzendt, wordt de Eind van tijd gehouden huidig en geen interventie op het deel van iedereen wordt vereist.

## Wanneer een Server van het Web ontbreekt {#section-19280cf83ca44bd7b1ee11bfc74494d2}

Wanneer een Webserver volledig off-line wegens één of andere catastrofale mislukking is, of verzendt geen gegevens of hartslagen, [!DNL data workbench server] einden zoals van tijd op de einden om te waarborgen dat het de laatste tijd vertegenwoordigt de [!DNL data workbench server] ontvangen gegevens van ALLE gegevensbronnen waarvan het zich bewust is. Het systeem zelf blijft gegevens verwerken, die nog voor analyse in de Werkbank van Gegevens beschikbaar zijn, maar om het even wat in het [!DNL data workbench server] die op het van tijd gebaseerd is functioneert niet. Bijvoorbeeld, brengt het EIND van tijd het melden in werking en gebruikt om vele afgeleide afmetingen in het systeem tot stand te brengen. Wanneer de EIND van tijd is tegengehouden, wordt de rapportering niet teweeggebracht en deze bepaalde afgeleide dimensies zijn niet beschikbaar.

Bijvoorbeeld, als WEB2 op 15 Juni offline ging en geen gegevens voor vijf dagen zond, zou As van tijd ergens op 15 Juni zijn. De dimensie van gisteren zou bijvoorbeeld 14 juni zijn, hoewel de datum van vandaag 20 juni is.
