---
description: Als u geen toestemming hebt om dossiers van een profiel te schrappen of u wilt geen dossier permanent schrappen, kunt u lege (nul-byte) dossiers gebruiken om dossiers te verbergen.
solution: Analytics
title: Een bestand verbergen door het te leegmaken (nul-byte)
topic: Data workbench
uuid: 82c1a5c9-1bbb-41c7-bee7-704f0a9ef87d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Een bestand verbergen door het te leegmaken (nul-byte){#hide-a-file-by-emptying-it-zero-byte}

Als u geen toestemming hebt om dossiers van een profiel te schrappen of u wilt geen dossier permanent schrappen, kunt u lege (nul-byte) dossiers gebruiken om dossiers te verbergen.

In [!DNL Profile Manager], identificeert een koppelteken (-), in plaats van een vinkje, in een kolom een nul-bytedossier.

![](assets/vis_ProfMgr_Zero-byte.png)

In tegenstelling tot de andere methodes om dossiers (zoals [!DNL order.txt], de parameter van de Show, en de Verborgen parameter) te verbergen, behandelt de Werkbank van Gegevens nul-byted dossiers als niet-bestaand. Bijvoorbeeld, als u nul-byte een afmeting die in een visualisatie of een metrische definitie is gebruikt, veroorzaakt de Werkbank van Gegevens een fout voor die visualisatie of metrisch, respectievelijk.

Deze functionaliteit is nuttig om een aantal redenen, met inbegrip van wanneer u het volgende wilt doen:

* **Maak een dossier onbruikbaar** in de Werkbank van Gegevens zonder de profieltoestemmingen te vereisen die worden vereist om het dossier te schrappen.
* **Verplaats metrisch, afmeting, of filter** naar een andere plaats zonder de profieltoestemmingen te vereisen om het dossier van de originele plaats te schrappen.
* **Menu-items verbergen.** Bijvoorbeeld, heeft het [!DNL Base] profiel een [!DNL Metric Legend] bepaald in het [!DNL Metric.vw] dossier. Zeg uw bedrijf drie metrische legenden heeft gecreeerd die u op een Add Legend > Metrische submenu wilt verschijnen. U kunt nul-byte het [!DNL Base] profieldossier [!DNL Metric.vw] zodat slechts uw nieuwe submenu en drie nieuwe metrische legenden verschijnen.

**Om een dossier te verbergen**

1. In [!DNL Profile Manager], open de noodzakelijke omslagen en subfolders om van het dossier de plaats te bepalen dat u aan nul-byte wilt.
1. Klik het vinkje naast de naam van het dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.
1. Open het lokale dossier en schrap zijn inhoud.
1. Sparen en sluit het dossier.

