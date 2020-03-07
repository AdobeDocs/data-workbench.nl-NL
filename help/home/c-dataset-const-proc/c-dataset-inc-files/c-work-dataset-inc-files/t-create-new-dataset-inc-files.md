---
description: De stappen om een nieuwe dataset tot stand te brengen omvatten dossier.
solution: Analytics
title: Het creëren van Nieuwe Dataset omvat Dossiers
topic: Data workbench
uuid: 707bdd84-b12b-4226-b6aa-43c9fc7ec9fe
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Het creëren van Nieuwe Dataset omvat Dossiers{#creating-new-dataset-include-files}

De stappen om een nieuwe dataset tot stand te brengen omvatten dossier.

U zou een nieuwe dataset moeten tot stand brengen omvat dossier om het even welke volgende taken van de datasetconfiguratie uit te voeren:

* Het specificeren van nieuwe gebieden van gegevens die van logboekverwerking tot transformatie moeten worden overgegaan.
* Het bepalen van transformaties die één van beiden van het volgende doen:

   * Bestaande logboekvelden bijwerken.
   * Produceer nieuwe gebieden die van logboekverwerking tot transformatie moeten worden overgegaan of die worden gebruikt om uitgebreide afmetingen te bepalen.

      Voor informatie over de beschikbare transformatietypen, zie de Transformaties van [Gegevens](../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

      >[!NOTE]
      >
      >Als u transformaties in een nieuwe dataset bepaalt omvat dossier, ben zeker om de orde van de input en de output in mening te houden. Voor informatie over het opdracht geven tot van transformaties, zie [Overeenkomsten voor het construeren van Transformaties](../../../../home/c-dataset-const-proc/c-data-trans/c-con-transf.md#concept-01998eebb7e347c58255fb442f2613b6).

* Het creëren van uitgebreide afmetingen. Voor informatie over de beschikbare afmetingstypes, zie [Uitgebreide Afmetingen](../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

1. Terwijl het werken in uw datasetprofiel, open de [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om de bestaande dataset te bekijken omvatten dossiers.

   * Om de [!DNL Log Processing Dataset Include] dossiers te bekijken, klik **[!UICONTROL Log Processing]**.

   * Om de [!DNL Transformation Dataset Include] dossiers te bekijken, klik **[!UICONTROL Transformation]**.

1. Creeer een nieuwe [!DNL Log Processing] of [!DNL Transformation Dataset Include] dossiers door één van de volgende stappen uit te voeren:

   * In de [!DNL User] kolom voor de folder van de Verwerking van het Logboek, klik **[!UICONTROL Create]** > **[!UICONTROL New Log Processing]**. Een genoemd dossier [!DNL New Log Processing.cfg] verschijnt in de folder.

   * In de [!DNL User] kolom voor de folder van de Transformatie, klik **[!UICONTROL Create]** > **[!UICONTROL New Transformation]**. Een genoemd dossier [!DNL New Transformation.cfg] verschijnt in de folder.

1. Noem het nieuwe dossier anders door zijn vinkje in de [!DNL User] kolom met de rechtermuisknop aan te klikken en de nieuwe naam in de parameter van het Dossier te typen.

   ![Stapgegevens](assets/vis_ProfileManager_RenameFile.png)

1. Klik het vinkje voor het anders genoemde dossier met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het configuratievenster verschijnt.
1. Geef de parameters in het configuratiedossier uit zoals aangewezen. Zie Dataset voor [logboekverwerking Bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) of gegevensset voor [transformatie opnemen Bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) opnemen voor beschrijvingen van de beschikbare parameters.
1. Om uw veranderingen te bewaren, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort. De opwerking of de retransformatie van de gegevens beginnen na synchronisatie van het datasetprofiel.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

Om een dataset uit te geven omvat dossier dat u creeerde, zie het [Uitgeven Bestaande Dataset Dossiers](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077)omvatten.
