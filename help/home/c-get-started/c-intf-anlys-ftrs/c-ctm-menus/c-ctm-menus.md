---
description: U kunt de verschijning van menu's met inbegrip van het menu van het werkruimtevenster (dat door in om het even welke werkruimte met de rechtermuisknop aan te klikken wordt betreden) aanpassen en menu's die van metriek, afmetingen, en kaartlagen een lijst maken.
solution: Analytics
title: Een menu aanpassen
topic: Data workbench
uuid: 8c409c50-40b3-4de3-8048-a825ef4d75f5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Een menu aanpassen{#customize-a-menu}

U kunt de verschijning van menu&#39;s met inbegrip van het menu van het werkruimtevenster (dat door in om het even welke werkruimte met de rechtermuisknop aan te klikken wordt betreden) aanpassen en menu&#39;s die van metriek, afmetingen, en kaartlagen een lijst maken.

De hiërarchie van om het even welk menu spiegelt de structuur van zijn folder in [!DNL Profile Manager]. Bijvoorbeeld, weerspiegelt het menu van het werkruimtevenster de structuur van de folder van het Menu en het metriekmenu spiegelt de structuur van de folder van Metriek. Voor om het even welk menu, kan de overeenkomstige folder de volgende punten bevatten:

* **Bestanden:** Deze dossiers vertegenwoordigen de visualisaties, legends, annotaties, administratieve interfaces, metriek, afmetingen, of kaartlagen die u kunt openen door het overeenkomstige menupunt te klikken.
* **Een[!DNL order.txt]bestand:** Dit dossier specificeert in welke orde het menu zijn punten toont.
* **Subdirectories:** Elke subdirectory vertegenwoordigt een submenu. Elke subdirectory kan zijn eigen dossiers, subdirectories, en [!DNL order.txt] dossier bevatten.

Bijvoorbeeld, bevat het [!DNL Add Legend] menu de menupunten Metrisch, Kleur, Waarde, en Vertrouwen, in die orde. In vergelijking, voegt het Menu \ de folder van de Legende in toe [!DNL Profile Manager] bevat de dossiers [!DNL Color.vw], [!DNL Confidence.vw], [!DNL Metric.vw], en de [!DNL Value.vw] dossiers in alfabetische orde, evenals een [!DNL order.txt] dossier om de orde van de andere dossiers te controleren.
