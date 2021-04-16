---
description: De stappen aan het uitgeven van bestaande dataset omvatten dossiers.
title: Bestaande gegevensset met include-bestanden bewerken
uuid: fcce2e46-b4a8-4c53-83bb-32ab410eb89e
exl-id: f4095871-d004-4e10-af18-bf6c1e47493d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Bestaande gegevensset bewerken bevat bestanden{#editing-existing-dataset-include-files}

De stappen aan het uitgeven van bestaande dataset omvatten dossiers.

U opent een bestaande dataset omvat dossier gebruikend [!DNL Profile Manager] in gegevenswerkbank.

Voor informatie over het openen en het werken met [!DNL Profile Manager], zie *de Gids van de Gebruiker van de Data Workbench*.

1. Tijdens het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om de inhoud van de folder te tonen.

   * Als u een [!DNL Log Processing Dataset Include]-bestand wilt openen, klikt u op **[!UICONTROL Log Processing]** om de inhoud van de map weer te geven.

   * Als u een [!DNL Transformation Dataset Include]-bestand wilt openen, klikt u op **[!UICONTROL Transformation]** om de inhoud van de map weer te geven.

1. Klik het vinkje naast de gewenste dataset omvatten dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het configuratievenster wordt weergegeven.

   U kunt een dataset ook openen omvat dossier van [!DNL Transformation Dependency Maps]. Voor informatie over [!DNL Transformation Dependency Maps], zie [Reprocessing and Retransformation](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

1. Bewerk de parameters in het configuratiebestand naar wens. Zie [Gegevensset voor logverwerking Inclusief bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) of [Gegevensset voor transformatie Inclusief bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) voor beschrijvingen van de parameters.

   Wanneer u een dataset bewerkt die een bestand bevat in een werkbankvenster voor gegevens, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals cut (Ctrl+x), copy (Ctrl+c), paste (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst van één configuratiedossier ( [!DNL .cfg]) aan een ander te kopiëren en te kleven.

1. Als u uw wijzigingen wilt opslaan, klikt u met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klikt u op **[!UICONTROL Save]**.
1. Als u wilt dat de lokaal aangebrachte wijzigingen van kracht worden, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort. Het opnieuw verwerken of omzetten van de gegevens begint na synchronisatie van het gegevenssetprofiel.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.
