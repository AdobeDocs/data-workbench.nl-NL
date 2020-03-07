---
description: Wanneer de Sensor gebeurtenisgegevens van een Webserver verzamelt, plaatst automatisch een blijvend koekje voor elke bezoeker die een klein willekeurig herkenningsteken bevat, zonder om het even welke persoonlijk identificerende informatie te vangen.
solution: Insight
title: Hoe identificeert de sensor Bezoekers en Zittingen?
uuid: 3735ed2d-67c4-469b-8b3e-0fac90cc4c09
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Hoe identificeert de sensor Bezoekers en Zittingen?{#how-does-sensor-identify-visitors-and-sessions}

Wanneer de Sensor gebeurtenisgegevens van een Webserver verzamelt, plaatst automatisch een blijvend koekje voor elke bezoeker die een klein willekeurig herkenningsteken bevat, zonder om het even welke persoonlijk identificerende informatie te vangen.

Dit koekje van Adobe wordt gebruikt om de unieke bezoeker en elk van zijn verwante zittingen te identificeren.

Door gebrek, [!DNL Sensor] vangt alle W3C Uitgebreide gebieden van het Formaat van het Dossier van het Logboek van elke HTTP- kopbal, maar u kunt vormen [!DNL Sensor] om het even welke kopbal te vangen die tussen de cliënt en de server wordt overgebracht. Voor informatie over de gebieden van gebeurtenisgegevens die door [!DNL Sensor] in [!DNL .vsl] dossiers worden verzameld, zie de Gebieden van het Verslag van de Gegevens van de [Gebeurtenis](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44).

In de browsers van sommige bezoekers worden cookies niet permanent opgeslagen, en een zeer klein aantal bezoekersbrowsers accepteert geen cookies (zelfs sessiecookies). Alhoewel zij slechts een fractie van het totale verkeer van een plaats rekenschap geven, kunnen zij in significante mistelling resulteren als elke paginamening door zulk een bezoeker verkeerd als volledige zitting wordt geteld, zoals door één of andere software van de logboekdossieranalyse wordt gedaan. Adobe behandelt dit probleem door u toe te laten om bezoekers met en zonder koekjes te analyseren.

Voor meer informatie over de Broken Filter van Zittingen, zie de Gids van de Sensor van de *Werkbank van Gegevens*.
