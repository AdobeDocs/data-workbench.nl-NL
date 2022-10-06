---
description: Met een modelviewer kunt u een logistiek regressiemodel genereren met de functie voor het noteren van volheid.
title: Modelviewer
uuid: 7ee8ff29-21c2-4721-804a-c7a5d101b50b
exl-id: e0e4acd4-76a2-436a-993b-2bb7ca91ae1a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Modelviewer{#model-viewer}

{{eol}}

Met een modelviewer kunt u een logistiek regressiemodel genereren met de functie voor het noteren van volheid.

In de modelviewer worden de coëfficiëntgewichten van elke invoervariabele (inclusief de constante term) en het statistische foutbereik weergegeven. Invoervariabelen met een hoge absolute coëfficiënt en een kleine foutmarge zijn de belangrijkste voorspellers in het model.

**Een modelviewerdiagram openen**

1. Selecteren [!DNL Add Visualization > Predictive Analytics > Scoring] .
1. Houd de muisaanwijzer boven het model Voltooien van een opgeslagen score.

![](assets/propensity_model_viewer.png)

De inputvariabelen met een coëfficiënt >= 1 zijn positieve invloeden op het voortstuwingsmodel. De coëfficiënten die &lt; 1 zijn, zijn negatieve invloeden op het nevenmodel. Het bereik dat tussen de haakjes staat, is de fout en geeft de consistentie aan van de invoervariabele in de geslaagde populatie.
