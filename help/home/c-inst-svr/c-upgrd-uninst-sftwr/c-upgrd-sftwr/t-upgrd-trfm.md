---
description: Stappen om de map Transform te upgraden.
title: Transformatie bijwerken
uuid: 26e567bc-7571-4317-b77c-2631a163a4b5
exl-id: b5e21862-caf1-42e4-9247-c870d7b3180e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Transformatie bijwerken{#upgrading-transform}

{{eol}}

Stappen om de map Transform te upgraden.

1. Open de [!DNL .zip] bestand voor de [!DNL Insight Server] releasepakket en open de [!DNL Profiles] map binnen die [!DNL .zip] bestand.
1. Kopieer de [!DNL Transform] aan de [!DNL Profiles] in uw [!DNL Insight Server] installatiemap. Hiermee overschrijft u het bestaande [!DNL Transform] map.
1. Voor elk profiel dat het [!DNL Transform] -profiel, bevestigen dat de [!DNL profile.cfg] bestand heeft een Transform-item in de Directory-vector.
Het opnieuw verwerken van gegevens begint na synchronisatie van het profiel.
