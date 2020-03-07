---
description: Als u geen configuratiedossier van een intern of ander geërft profiel (namelijk wilt u de instructies in het dossier worden genegeerd tijdens datasetbouw) wilt erven, maar u wilt niet het dossier wijzigen, kunt u een leeg (nul-byte) dossier met de zelfde naam tot stand brengen en het dossier in een ander profiel opslaan.
solution: Analytics
title: Gegevensset-configuratiebestanden verbergen
topic: Data workbench
uuid: eb33cf54-e067-4af2-a10e-7ffe43910e4f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gegevensset-configuratiebestanden verbergen{#hiding-dataset-configuration-files}

Als u geen configuratiedossier van een intern of ander geërft profiel (namelijk wilt u de instructies in het dossier worden genegeerd tijdens datasetbouw) wilt erven, maar u wilt niet het dossier wijzigen, kunt u een leeg (nul-byte) dossier met de zelfde naam tot stand brengen en het dossier in een ander profiel opslaan.

**Aan nul-byte een dossier van de datasetconfiguratie**

1. In [!DNL Profile Manager], open de noodzakelijke omslagen en subfolders om van het dossier de plaats te bepalen dat u aan nul-byte wilt.
1. Klik het vinkje naast de naam van het dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.
1. Open het lokale dossier in een tekstredacteur zoals Blocnote en schrap zijn inhoud.
1. Sparen en sluit het dossier.
1. In [!DNL Profile Manager], sparen het nul-bytedossier aan een profiel rechts van het profiel waarin het oorspronkelijke dossier verblijft. (U wilt het nul-bytedossier belangrijkheid over het oorspronkelijke dossier nemen.)

   In [!DNL Profile Manager], identificeert een koppelteken (-), in plaats van een vinkje, in een kolom het nul-bytedossier zoals aangetoond in het hieronder voorbeeld.

   ![](assets/vis_ProfileManager_ZeroByteFile.png)

Wanneer u uw dataset opnieuw verwerkt, bevat de dataset niet de datasetcomponenten die het originele dossier bepaalt.

>[!NOTE]
>
>Als u nul-byte een configuratiedossier dat een uitgebreide afmeting bepaalt die in een visualisatie of een metrische definitie wordt gebruikt, veroorzaakt de gegevenswerkbank een fout voor die visualisatie of metrisch, respectievelijk.

U kunt nul-bytedossiers ook gebruiken om metrisch, afmeting, of filter naar een andere plaats in het profiel te verplaatsen of menupunten te verbergen. Voor informatie, zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.
