---
description: Het de configuratiedossier van het Toegangsbeheer, Access Control.cfg, bepaalt de groepen van het toegangsbeheer waardoor de Server van het Inzicht toestemmingen aan dossiers verleent die op de attributen (OU, CN, etc.) van het certificaat van de inkomende verbinding worden gebaseerd.
title: Toegangsbeheer configureren
uuid: e0206b43-3c8c-48ec-b663-814f5b663b96
exl-id: 2836c907-fc74-4d35-badc-b8f06cd6989f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Toegangsbeheer configureren{#configuring-access-control}

{{eol}}

Het de configuratiedossier van het Toegangsbeheer, Access Control.cfg, bepaalt de groepen van het toegangsbeheer waardoor de Server van het Inzicht toestemmingen aan dossiers verleent die op de attributen (OU, CN, etc.) van het certificaat van de inkomende verbinding worden gebaseerd.

**Aanbevolen frequentie:** Indien nodig

[!DNL Insight Server] verstrekt configureerbare toegangsbeheergroepen om de veiligheid van verbindingen te beheren aan [!DNL Insight Server]. Toegangsbeheergroepen identificeren gebruikers die beheerfuncties mogen uitvoeren via [!DNL Insight].

Als u toegang moet bieden aan nieuwe gebruikers of nieuwe machines, bijvoorbeeld wanneer u een computer aan een [!DNL Insight Server] cluster, bewerkt u eenvoudig het configuratiebestand van Toegangsbeheer.
