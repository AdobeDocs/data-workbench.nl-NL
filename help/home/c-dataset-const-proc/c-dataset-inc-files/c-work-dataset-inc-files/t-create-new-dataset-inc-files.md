---
description: De stappen om een nieuwe dataset tot stand te brengen omvatten dossier.
title: Nieuwe gegevensset maken met include-bestanden
uuid: 707bdd84-b12b-4226-b6aa-43c9fc7ec9fe
exl-id: 8a7b343d-b695-41aa-b465-8c5cd68d6ef7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Nieuwe gegevensset maken met include-bestanden{#creating-new-dataset-include-files}

{{eol}}

De stappen om een nieuwe dataset tot stand te brengen omvatten dossier.

U zou een nieuwe dataset moeten creëren omvat dossier om het even welke volgende taken van de datasetconfiguratie uit te voeren:

* Het specificeren van nieuwe gebieden van gegevens die van logboekverwerking tot transformatie moeten worden overgegaan.
* Transformaties definiëren die een van de volgende handelingen uitvoeren:

   * Bestaande logvelden bijwerken.
   * Produceer nieuwe gebieden die van logboekverwerking tot transformatie moeten worden overgegaan of die worden gebruikt om uitgebreide afmetingen te bepalen.

      Voor informatie over de beschikbare transformatietypen raadpleegt u [Gegevenstransformaties](../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

      >[!NOTE]
      >
      >Als u transformaties in een nieuwe dataset omvat dossier bepaalt, ben zeker om de orde van de input en de output in mening te houden. Voor informatie over de volgorde van transformaties raadpleegt u [Conventies voor het samenstellen van transformaties](../../../../home/c-dataset-const-proc/c-data-trans/c-con-transf.md#concept-01998eebb7e347c58255fb442f2613b6).

* Uitgebreide afmetingen maken. Voor informatie over de beschikbare dimensietypen, zie [Uitgebreide Dimension](../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

1. Tijdens het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik op **[!UICONTROL Dataset]** om de bestaande dataset te bekijken omvat dossiers.

   * Als u het dialoogvenster [!DNL Log Processing Dataset Include] bestanden, klikt u op **[!UICONTROL Log Processing]**.

   * Als u het dialoogvenster [!DNL Transformation Dataset Include] bestanden, klikt u op **[!UICONTROL Transformation]**.

1. Een nieuwe [!DNL Log Processing] of [!DNL Transformation Dataset Include] bestanden door een van de volgende stappen uit te voeren:

   * In de [!DNL User] kolom voor de map Log Processing, klikt u op **[!UICONTROL Create]** > **[!UICONTROL New Log Processing]**. Een bestand met de naam [!DNL New Log Processing.cfg] wordt weergegeven in de map.

   * In de [!DNL User] kolom voor de map Transformation, klikt u op **[!UICONTROL Create]** > **[!UICONTROL New Transformation]**. Een bestand met de naam [!DNL New Transformation.cfg] wordt weergegeven in de map.

1. Wijzig de naam van het nieuwe bestand door met de rechtermuisknop op het vinkje ervan te klikken in het dialoogvenster [!DNL User] en typt u de nieuwe naam in de parameter File.

   ![Stapinfo](assets/vis_ProfileManager_RenameFile.png)

1. Klik met de rechtermuisknop op het vinkje voor het bestand met de nieuwe naam en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het configuratievenster wordt weergegeven.
1. Bewerk de parameters in het configuratiebestand naar wens. Zie [Gegevensset logbestandsverwerking inclusief bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) of [Gegevensset transformatie bevat bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) voor beschrijvingen van de beschikbare parameters.
1. Als u uw wijzigingen wilt opslaan, klikt u met de rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort. Het opnieuw verwerken of omzetten van de gegevens begint na synchronisatie van het gegevenssetprofiel.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

Om een dataset uit te geven omvat dossier dat u creeerde, zie [Bestaande gegevensset met include-bestanden bewerken](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077).
