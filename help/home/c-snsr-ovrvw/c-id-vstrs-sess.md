---
description: Bij het verzamelen van gebeurtenisgegevens van een webserver stelt Sensor automatisch een permanente cookie in voor elke bezoeker die een kleine willekeurige id bevat, zonder persoonlijke identificatiegegevens vast te leggen.
solution: Analytics
title: Hoe identificeert Sensor bezoekers en sessies?
uuid: 3735ed2d-67c4-469b-8b3e-0fac90cc4c09
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---


# Hoe identificeert Sensor bezoekers en sessies?{#how-does-sensor-identify-visitors-and-sessions}

Bij het verzamelen van gebeurtenisgegevens van een webserver stelt Sensor automatisch een permanente cookie in voor elke bezoeker die een kleine willekeurige id bevat, zonder persoonlijke identificatiegegevens vast te leggen.

Dit Adobe-cookie wordt gebruikt om de unieke bezoeker en alle bijbehorende sessies te identificeren.

Door gebrek, [!DNL Sensor] vangt alle gebieden van het Formaat van het Dossier van het Logboek W3C Uitgebreid van elke kopbal van HTTP, maar u kunt vormen [!DNL Sensor] om het even welke kopbal te vangen die tussen de cliënt en de server wordt overgebracht. Voor informatie over de gebieden van gebeurtenisgegevens die door [!DNL Sensor] in [!DNL .vsl] dossiers worden verzameld, zie de Gebieden [van het Verslag van](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44)Gebeurtenisgegevens.

In sommige browsers van bezoekers worden cookies niet permanent opgeslagen en in een zeer klein aantal browsers van bezoekers worden cookies helemaal niet geaccepteerd (zelfs sessiecookies). Hoewel zij slechts een fractie van het totale verkeer van een plaats vertegenwoordigen, kunnen zij in significante misrekening resulteren als elke paginamening door zulk een bezoeker verkeerd als volledige zitting wordt geteld, zoals door sommige software van de logboekdossieranalyse wordt gedaan. Adobe lost dit probleem op door bezoekers met en zonder cookies te kunnen analyseren.

Zie de *Data Workbench Sensor Guide* voor meer informatie over het filter Verbroken sessies.
