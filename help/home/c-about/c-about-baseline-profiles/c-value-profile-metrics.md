---
description: ongeldig
solution: Analytics
title: Waardeprofielstatistieken
topic: Data workbench
uuid: 68951e33-013a-466b-b0f3-839eaef89cb5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Waardeprofielstatistieken{#value-profile-metrics}

| Metrisch | Formule | Niveau | Beschrijving |
|---|---|---|---|
| Omzetting | [!DNL[Sessionsnot Session_Value=#0]/Sessions] | Sessie | Het percentage van zittingen die bedrijfswaarde (zoals die door het Model van de Bedrijfswaarde wordt bepaald) produceerden. |
| Waardepercentage | [!DNL Value/total(Value)] | Sessie | Het percentage van algemene waarde die uit de geselecteerde reeks zittingen werd geproduceerd. |
| Waarde | [!DNL sum(Session_Value, Session)*0.01] | Sessie | De totale bedrijfswaarde die, in dollars (zoals die door het Model van de Bedrijfswaarde wordt bepaald) wordt geproduceerd. |
| Waardegebeurtenissen | [!DNL[Sessionsnot Session_Value=#0]] | Sessie | De telling van zittingen die bedrijfswaarde (zoals die door het Model Bedrijfs van de Waarde wordt bepaald) produceerde. |
| Waarde Gebeurtenissen per bezoeker | [!DNL (Value_Events/Visitors) by Visitor] | Bezoeker | Het gemiddelde aantal zittingen voor elke bezoeker die bedrijfswaarde (zoals die door het Model van de Bedrijfswaarde wordt bepaald) produceerde. |
| Waarde per bezoeker | [!DNL (Value/Visitors) by Visitor] | Bezoeker | De gemiddelde bedrijfswaarde, in dollars, door elke bezoeker wordt geproduceerd die. |
