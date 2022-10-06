---
description: U kunt de vormgeving van menu's aanpassen, zoals het menu van het werkruimtevenster (dat u kunt openen door met de rechtermuisknop in een werkruimte te klikken) en menu's met maateenheden, afmetingen en kaartlagen.
title: Een menu aanpassen
uuid: 8c409c50-40b3-4de3-8048-a825ef4d75f5
exl-id: 7a377d9c-d339-43d8-a71a-a322416b2e60
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Een menu aanpassen{#customize-a-menu}

{{eol}}

U kunt de vormgeving van menu&#39;s aanpassen, zoals het menu van het werkruimtevenster (dat u kunt openen door met de rechtermuisknop in een werkruimte te klikken) en menu&#39;s met maateenheden, afmetingen en kaartlagen.

De hiërarchie van elk menu weerspiegelt de structuur van de bijbehorende map in het dialoogvenster [!DNL Profile Manager]. Het menu van het werkruimtevenster spiegelt bijvoorbeeld de structuur van de map Menu en het menu Metriek spiegelt de structuur van de map Metrics. Voor elk menu kan de corresponderende map de volgende items bevatten:

* **Bestanden:** Deze bestanden vertegenwoordigen de visualisaties, legenda&#39;s, annotaties, beheerinterfaces, metriek, dimensies of kaartlagen die u kunt openen door op het bijbehorende menu-item te klikken.
* **An [!DNL order.txt] bestand:** Dit bestand geeft aan in welke volgorde de items in het menu worden weergegeven.
* **Submappen:** Elke submap vertegenwoordigt een submenu. Elke submap kan zijn eigen bestanden, submappen en [!DNL order.txt] bestand.

De [!DNL Add Legend] bevat in die volgorde de menu-items Metrisch, Kleur, Waarde en Vertrouwen. In vergelijking hiermee\n voegt u de map Legenda toe in het dialoogvenster [!DNL Profile Manager] bevat de bestanden [!DNL Color.vw], [!DNL Confidence.vw], [!DNL Metric.vw], en [!DNL Value.vw] bestanden in alfabetische volgorde, alsmede een [!DNL order.txt] om de volgorde van de andere bestanden te bepalen.
