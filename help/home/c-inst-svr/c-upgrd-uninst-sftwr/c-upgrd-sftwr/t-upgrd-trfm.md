---
description: Stappen om de map Transform te upgraden.
solution: Analytics
title: Transformatie bijwerken
uuid: 26e567bc-7571-4317-b77c-2631a163a4b5
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---


# Transformatie bijwerken{#upgrading-transform}

Stappen om de map Transform te upgraden.

1. Open het [!DNL .zip] bestand voor het [!DNL Insight Server] releasepakket en open de [!DNL Profiles] map in dat [!DNL .zip] bestand.
1. Kopieer de [!DNL Transform] map naar de [!DNL Profiles] map in de [!DNL Insight Server] installatiemap. Hiermee overschrijft u de bestaande [!DNL Transform] map.
1. Bevestig voor elk profiel dat het [!DNL Transform] profiel overerft dat het [!DNL profile.cfg] bestand een Transform-item heeft in de Directory-vector.
Het opnieuw verwerken van gegevens begint na synchronisatie van het profiel.
