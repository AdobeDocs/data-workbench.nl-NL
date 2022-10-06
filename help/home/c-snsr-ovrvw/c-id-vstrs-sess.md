---
description: Bij het verzamelen van gebeurtenisgegevens van een webserver stelt Sensor automatisch een permanente cookie in voor elke bezoeker die een kleine willekeurige id bevat, zonder persoonlijke identificatiegegevens vast te leggen.
title: Hoe identificeert Sensor bezoekers en sessies?
uuid: 3735ed2d-67c4-469b-8b3e-0fac90cc4c09
exl-id: f5781ed6-ac83-4a8e-b412-8966f8c39c41
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Hoe identificeert Sensor bezoekers en sessies?{#how-does-sensor-identify-visitors-and-sessions}

{{eol}}

Bij het verzamelen van gebeurtenisgegevens van een webserver stelt Sensor automatisch een permanente cookie in voor elke bezoeker die een kleine willekeurige id bevat, zonder persoonlijke identificatiegegevens vast te leggen.

Dit Adobe-cookie wordt gebruikt om de unieke bezoeker en alle bijbehorende sessies te identificeren.

Standaard, [!DNL Sensor] vangt alle gebieden van het Formaat van het Dossier van het Logboek W3C Uitgebreid van elke kopbal van HTTP, maar u kunt vormen [!DNL Sensor] om een header vast te leggen die tussen de client en de server wordt verzonden. Voor informatie over de velden met gebeurtenisgegevens die worden verzameld door [!DNL Sensor] in [!DNL .vsl] bestanden, zie [Gebeurtenisgegevensrecordvelden](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44).

In sommige browsers van bezoekers worden cookies niet permanent opgeslagen en in een zeer klein aantal browsers van bezoekers worden cookies helemaal niet geaccepteerd (zelfs sessiecookies). Hoewel zij slechts een fractie van het totale verkeer van een plaats vertegenwoordigen, kunnen zij in significante misrekening resulteren als elke paginamening door zulk een bezoeker verkeerd als volledige zitting wordt geteld, zoals door sommige software van de logboekdossieranalyse wordt gedaan. Adobe lost dit probleem op door bezoekers met en zonder cookies te kunnen analyseren.

Zie voor meer informatie over het filter Verbroken sessies de optie *Data Workbench Sensor Guide*.
