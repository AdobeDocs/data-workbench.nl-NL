---
description: De toepassing van de gegevenswerkbankcliënt steunt nu Vereenvoudigd Chinees.
solution: Analytics
title: Vereenvoudigde Chinese lokalisatie
topic: Data workbench
uuid: ddf4eade-7c5f-4ccf-aa9f-dd8d109a059f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vereenvoudigde Chinese lokalisatie{#simplified-chinese-localization}

De toepassing van de gegevenswerkbankcliënt steunt nu Vereenvoudigd Chinees.

**Om Vereenvoudigd Chinees** te installeren:

Alvorens dossiers te vormen [!DNL Insight.exe] en te steunen, moet u de cliënttoepassing weggaan.

1. Creeer een kortere weg die in de bevel-lijn overgaat die aan het [!DNL insight.exe] dossier plaatst.

   ```
   Insight.exe -zh-cn
   ```

1. Vorm [!DNL Insight.cfg] om enige en dubbel-byte doopvontkarakters te steunen.

   De werkbank van gegevens steunt momenteel zowel Engels als Vereenvoudigd Chinees. U kunt doopvonten selecteren om beide talen te steunen:

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial 
   ```

1. Start opnieuw [!DNL Insight.exe].

