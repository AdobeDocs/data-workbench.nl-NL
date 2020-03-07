---
description: Een modelkijker laat u een logistiek regressiemodel produceren gebruikend de Propensity Scoring eigenschap.
solution: Analytics
title: Modelviewer
topic: Data workbench
uuid: 7ee8ff29-21c2-4721-804a-c7a5d101b50b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Modelviewer{#model-viewer}

Een modelkijker laat u een logistiek regressiemodel produceren gebruikend de Propensity Scoring eigenschap.

De modelKijker toont de coëfficiëntgewichten van elke inputvariabele (met inbegrip van de constante termijn) en hun statistische foutenwaaier. De variabelen van de input die een hoge absolute coëfficiënt en een kleine foutenmarge tonen zijn de belangrijkste voorspellers in het model.

**Om een Modelgrafiek van de Kijker te openen**

1. Selecteer [!DNL Add Visualization > Predictive Analytics > Scoring] .
1. Afdekking over model voltooid van een opgeslagen score.

![](assets/propensity_model_viewer.png)

De inputvariabelen met een coëfficiënt >= 1 zijn positieve invloeden op het voortstuwingsmodel. De coëfficiënten die &lt; 1 zijn, zijn negatieve invloeden op het nevenmodel. De waaier die binnen de haakjes wordt bepaald is de fout, en wijst op de consistentie van de inputvariabele over de succesvolle populatie.
