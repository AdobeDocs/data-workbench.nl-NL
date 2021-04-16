---
description: Stappen om de map Transform te upgraden.
title: Transformatie bijwerken
uuid: 26e567bc-7571-4317-b77c-2631a163a4b5
exl-id: b5e21862-caf1-42e4-9247-c870d7b3180e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Transformatie bijwerken{#upgrading-transform}

Stappen om de map Transform te upgraden.

1. Open het [!DNL .zip]-bestand voor het [!DNL Insight Server]-releasepakket en open de map [!DNL Profiles] in dat [!DNL .zip]-bestand.
1. Kopieer de map [!DNL Transform] naar de map [!DNL Profiles] in de installatiemap [!DNL Insight Server]. Hierbij wordt de bestaande map [!DNL Transform] overschreven.
1. Voor elk profiel dat het [!DNL Transform] profiel erft, bevestig dat het [!DNL profile.cfg] dossier een &quot;Transformatie&quot;ingang in de vector van Folders heeft.
Het opnieuw verwerken van gegevens begint na synchronisatie van het profiel.
