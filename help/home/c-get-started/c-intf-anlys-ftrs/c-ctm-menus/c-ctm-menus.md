---
description: U kunt de vormgeving van menu's aanpassen, zoals het menu van het werkruimtevenster (dat u kunt openen door met de rechtermuisknop in een werkruimte te klikken) en menu's met maateenheden, afmetingen en kaartlagen.
title: Een menu aanpassen
uuid: 8c409c50-40b3-4de3-8048-a825ef4d75f5
exl-id: 7a377d9c-d339-43d8-a71a-a322416b2e60
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Een menu aanpassen{#customize-a-menu}

U kunt de vormgeving van menu&#39;s aanpassen, zoals het menu van het werkruimtevenster (dat u kunt openen door met de rechtermuisknop in een werkruimte te klikken) en menu&#39;s met maateenheden, afmetingen en kaartlagen.

De hiërarchie van om het even welk menu weerspiegelt de structuur van zijn folder in [!DNL Profile Manager]. Het menu van het werkruimtevenster spiegelt bijvoorbeeld de structuur van de map Menu en het menu Metriek spiegelt de structuur van de map Metrics. Voor elk menu kan de corresponderende map de volgende items bevatten:

* **Bestanden:** deze bestanden vertegenwoordigen de visualisaties, legenda&#39;s, annotaties, beheerinterfaces, metriek, dimensies of kaartlagen die u kunt openen door op het bijbehorende menu-item te klikken.
* **An  [!DNL order.txt] file:** This file specifies in which order the menu displays its items.
* **submappen:** elke submap vertegenwoordigt een submenu. Elke subdirectory kan zijn eigen bestanden, submappen en [!DNL order.txt]-bestand bevatten.

Het menu [!DNL Add Legend] bevat bijvoorbeeld de menu-items Metrisch, Kleur, Waarde en Vertrouwen in die volgorde. Ter vergelijking: de map Menu\Add Legend in [!DNL Profile Manager] bevat de bestanden [!DNL Color.vw], [!DNL Confidence.vw], [!DNL Metric.vw] en [!DNL Value.vw] in alfabetische volgorde, evenals een [!DNL order.txt]-bestand om de volgorde van de andere bestanden te bepalen.
