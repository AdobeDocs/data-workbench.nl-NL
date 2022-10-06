---
description: De stappen aan het uitgeven van bestaande dataset omvatten dossiers.
title: Bestaande gegevensset met include-bestanden bewerken
uuid: fcce2e46-b4a8-4c53-83bb-32ab410eb89e
exl-id: f4095871-d004-4e10-af18-bf6c1e47493d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Bestaande gegevensset met include-bestanden bewerken{#editing-existing-dataset-include-files}

{{eol}}

De stappen aan het uitgeven van bestaande dataset omvatten dossiers.

U opent een bestaande dataset omvat dossier gebruikend [!DNL Profile Manager] in de werkbank voor gegevens.

Voor informatie over het openen en werken met de [!DNL Profile Manager], zie de *Gebruikershandleiding voor Data Workbench*.

1. Tijdens het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik op **[!UICONTROL Dataset]** om de inhoud van de map weer te geven.

   * Als u een [!DNL Log Processing Dataset Include] bestand, klikt u op **[!UICONTROL Log Processing]** om de inhoud van de map weer te geven.

   * Als u een [!DNL Transformation Dataset Include] bestand, klikt u op **[!UICONTROL Transformation]** om de inhoud van de map weer te geven.

1. Klik met de rechtermuisknop op het vinkje naast de gewenste gegevensset met include-bestanden en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het configuratievenster wordt weergegeven.

   U kunt een dataset ook openen omvat dossier van een [!DNL Transformation Dependency Maps]. Voor informatie over [!DNL Transformation Dependency Maps], zie [Opwerking en heromzetting](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

1. Bewerk de parameters in het configuratiebestand naar wens. Zie [Gegevensset logbestandsverwerking inclusief bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) of [Gegevensset transformatie bevat bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) voor beschrijvingen van de parameters.

   Wanneer u een dataset bewerkt die een bestand bevat in een werkbankvenster voor gegevens, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals cut (Ctrl+x), copy (Ctrl+c), paste (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Daarnaast kunt u de sneltoetsen gebruiken om tekst uit één configuratiebestand te kopiëren en te plakken ( [!DNL .cfg]) aan een andere.

1. Als u uw wijzigingen wilt opslaan, klikt u met de rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort. Het opnieuw verwerken of omzetten van de gegevens begint na synchronisatie van het gegevenssetprofiel.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.
