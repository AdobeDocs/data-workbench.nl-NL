---
description: Bij het verzamelen van gebeurtenisgegevens van een webserver stelt Sensor automatisch een permanente cookie in voor elke bezoeker die een kleine willekeurige id bevat, zonder persoonlijke identificatiegegevens vast te leggen.
title: Hoe identificeert Sensor bezoekers en sessies?
uuid: 3735ed2d-67c4-469b-8b3e-0fac90cc4c09
exl-id: f5781ed6-ac83-4a8e-b412-8966f8c39c41
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Hoe identificeert Sensor bezoekers en sessies?{#how-does-sensor-identify-visitors-and-sessions}

Bij het verzamelen van gebeurtenisgegevens van een webserver stelt Sensor automatisch een permanente cookie in voor elke bezoeker die een kleine willekeurige id bevat, zonder persoonlijke identificatiegegevens vast te leggen.

Dit Adobe-cookie wordt gebruikt om de unieke bezoeker en alle bijbehorende sessies te identificeren.

Standaard legt [!DNL Sensor] alle velden in de W3C Extended-indeling voor logbestanden vast vanaf elke HTTP-header, maar u kunt [!DNL Sensor] zo configureren dat elke header wordt vastgelegd die wordt verzonden tussen de client en de server. Zie [Gebeurtenisgegevensvelden](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44) voor informatie over de gebeurtenisgegevensvelden die door [!DNL Sensor] in [!DNL .vsl]-bestanden worden verzameld.

In sommige browsers van bezoekers worden cookies niet permanent opgeslagen en in een zeer klein aantal browsers van bezoekers worden cookies helemaal niet geaccepteerd (zelfs sessiecookies). Hoewel zij slechts een fractie van het totale verkeer van een plaats vertegenwoordigen, kunnen zij in significante misrekening resulteren als elke paginamening door zulk een bezoeker verkeerd als volledige zitting wordt geteld, zoals door sommige software van de logboekdossieranalyse wordt gedaan. Adobe lost dit probleem op door bezoekers met en zonder cookies te kunnen analyseren.

Zie de *Data Workbench Sensor Guide* voor meer informatie over het filter Verbroken sessies.
