---
description: Waardeprofielcijfers
title: Waardeprofielcijfers
uuid: 68951e33-013a-466b-b0f3-839eaef89cb5
exl-id: 9e95008c-1162-4f50-89d2-dcf5fcf8746a
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---

# Waardeprofielcijfers{#value-profile-metrics}

| Metrisch | Formule | Niveau | Beschrijving |
|---|---|---|---|
| Conversie | `Sessions[not Session_Value=#0]/Sessions` | Sessie | Het percentage sessies dat bedrijfswaarde heeft gegenereerd (zoals gedefinieerd in het Business Value Model). |
| Pct of Value | `Value/total(Value)` | Sessie | Het percentage van de totale waarde dat is gegenereerd op basis van de geselecteerde set sessies. |
| Waarde | `sum(Session_Value, Session)*0.01` | Sessie | De totale gegenereerde bedrijfswaarde in dollars (zoals gedefinieerd door het Business Value Model). |
| Waardegebeurtenissen | `Sessions[not Session_Value=#0]` | Sessie | Het aantal sessies dat bedrijfswaarde heeft gegenereerd (zoals gedefinieerd in het Business Value Model). |
| Waardegebeurtenissen per bezoeker | `(Value_Events/Visitors) by Visitor` | Bezoeker | Het gemiddelde aantal sessies voor elke bezoeker die bedrijfswaarde heeft gegenereerd (zoals gedefinieerd in het Business Value Model). |
| Waarde per bezoeker | `(Value/Visitors) by Visitor` | Bezoeker | De gemiddelde bedrijfswaarde, in dollars, die door elke bezoeker wordt gegenereerd. |
