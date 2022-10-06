---
description: Creeer de de uitvoerkopballen van de douanekolom voor uw segment de dossiers van de segmentuitvoer om gemakkelijk begrepen beschrijvingen voor uitgevoerde segmenten toe te voegen. Met deze exportfunctie kunt u ook uitvoeren als CSV- en TSV-bestanden.
title: Segment exporteren met aangepaste koppen
uuid: 186e7868-13b2-42e1-b83f-5a752ee9b407
exl-id: 1d27f926-35e1-4886-b7a6-702d9947dabb
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Segment exporteren met aangepaste koppen{#segment-export-with-custom-headers}

{{eol}}

Creeer de de uitvoerkopballen van de douanekolom voor uw segment de dossiers van de segmentuitvoer om gemakkelijk begrepen beschrijvingen voor uitgevoerde segmenten toe te voegen. Met deze exportfunctie kunt u ook uitvoeren als CSV- en TSV-bestanden.

De nieuwe functionaliteit is toegevoegd aan de Uitvoer van het Segment, met inbegrip van de capaciteit om met een kopbal uit te voeren, of in Csv en formaat TSV.

U kunt kolomkoppen maken voor uw exportbestanden.

## Exporteren van nieuw segment maken {#section-cffff55855f8467ea468b71393ab7676}

1. Een werkruimte openen en met de rechtermuisknop klikken **[!UICONTROL Tools]** > **[!UICONTROL Detail Table]**.

1. Klik met de rechtermuisknop en selecteer **[!UICONTROL Add Level > Extended]** > Kies een item.
1. Klik met de rechtermuisknop op de titel en selecteer **[!UICONTROL Add Attribute.]** Selecteer een dimensie in het menu.

1. Klik met de rechtermuisknop op de titel en selecteer **[!UICONTROL Add Metric.]** Selecteer een metrische waarde in het menu.

1. Klik met de rechtermuisknop op de titel en selecteer **[!UICONTROL New Segment Export]**.

   ![](assets/segment_export_headers.png)

   **[!UICONTROL New Segment Export with Header]** De naam van de kolom wordt automatisch ingevuld met de naam van de metrische waarde. **[!UICONTROL New Segment Export]** moet u een aangepaste naam instellen. ![](assets/segment_export_with_headers.png)

   >[!NOTE]
   >
   >Het veld Kolomnaam mag niet leeg zijn of de koptekst is niet aanwezig.

1. Klik met de rechtermuisknop en geef het segment een naam en klik vervolgens op **[!UICONTROL Save Export File]**.

   Er wordt een exportvenster geopend.

1. Klik met de rechtermuisknop op de exportnaam en klik op **Opslaan als`<export filename>`**.

   ![](assets/segment_export_headers_7.png)

1. Klik met de rechtermuisknop [!DNL Admin] > [!DNL Profile Manager] > [!DNL Expand Export]. Zoek het exportbestand dat u net hebt gemaakt en sla het op in een bestaand profiel.

   ![](assets/segment_export_headers_8.png)
