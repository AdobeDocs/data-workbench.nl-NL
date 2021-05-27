---
description: Het de configuratiedossier van het Toegangsbeheer, Access Control.cfg, bepaalt de groepen van het toegangsbeheer waardoor de Server van het Inzicht toestemmingen aan dossiers verleent die op de attributen (OU, CN, etc.) van het certificaat van de inkomende verbinding worden gebaseerd.
title: Toegangsbeheer configureren
uuid: e0206b43-3c8c-48ec-b663-814f5b663b96
exl-id: 2836c907-fc74-4d35-badc-b8f06cd6989f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Het vormen Toegangsbeheer{#configuring-access-control}

Het de configuratiedossier van het Toegangsbeheer, Access Control.cfg, bepaalt de groepen van het toegangsbeheer waardoor de Server van het Inzicht toestemmingen aan dossiers verleent die op de attributen (OU, CN, etc.) van het certificaat van de inkomende verbinding worden gebaseerd.

**Aanbevolen frequentie:** indien nodig

[!DNL Insight Server] verstrekt configureerbare toegangsbeheergroepen om de veiligheid van verbindingen aan te beheren  [!DNL Insight Server]. Toegangsbeheergroepen identificeren gebruikers die beheerfuncties mogen uitvoeren via [!DNL Insight].

Als u toegang tot nieuwe gebruikers of nieuwe machines moet verlenen, zoals wanneer het toevoegen van een machine aan een [!DNL Insight Server] cluster, bewerkt u eenvoudig het de configuratiedossier van de Controle van de Toegang.
