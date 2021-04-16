---
description: De gegevenswerkbank clienttoepassing ondersteunt nu Vereenvoudigd Chinees.
title: Vereenvoudigde Chinese lokalisatie
uuid: ddf4eade-7c5f-4ccf-aa9f-dd8d109a059f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---


# Vereenvoudigde Chinese lokalisatie{#simplified-chinese-localization}

De gegevenswerkbank clienttoepassing ondersteunt nu Vereenvoudigd Chinees.

**Vereenvoudigd Chinees** installeren:

Voordat u [!DNL Insight.exe] kunt configureren en bestanden kunt ondersteunen, moet u de clienttoepassing afsluiten.

1. Maak een sneltoets die de opdrachtregelinstelling doorgeeft aan het bestand [!DNL insight.exe].

   ```
   Insight.exe -zh-cn
   ```

1. Configureer [!DNL Insight.cfg] om single- en double-byte lettertypetekens te ondersteunen.

   De werkbank voor gegevens ondersteunt momenteel zowel Engels als Vereenvoudigd Chinees. U kunt lettertypen selecteren die beide talen ondersteunen:

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial 
   ```

1. Start [!DNL Insight.exe] opnieuw.

