---
description: De stappen aan het uitgeven van bestaande dataset omvatten dossiers.
solution: Analytics
title: Bestaande gegevensset bewerken Bestaande bestanden opnemen
topic: Data workbench
uuid: fcce2e46-b4a8-4c53-83bb-32ab410eb89e
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Bestaande gegevensset bewerken Bestaande bestanden opnemen{#editing-existing-dataset-include-files}

De stappen aan het uitgeven van bestaande dataset omvatten dossiers.

U opent een bestaande dataset omvat dossier gebruikend [!DNL Profile Manager] in gegevenswerkbank.

Voor informatie over het openen van en het werken met [!DNL Profile Manager], zie de Gids van de Gebruiker van de Werkbank van *Gegevens*.

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om de inhoud van de folder te tonen.

   * Om een [!DNL Log Processing Dataset Include] dossier te openen, klik **[!UICONTROL Log Processing]** om de inhoud van de folder te tonen.

   * Om een [!DNL Transformation Dataset Include] dossier te openen, klik **[!UICONTROL Transformation]** om de inhoud van de folder te tonen.

1. Klik het vinkje naast de gewenste dataset met de rechtermuisknop aan omvatten dossier en klikken **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het configuratievenster verschijnt.

   U kunt een dataset ook openen omvat dossier van a [!DNL Transformation Dependency Maps]. Voor informatie over [!DNL Transformation Dependency Maps], zie [Opwerking en Herschikking](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

1. Geef de parameters in het configuratiedossier uit zoals aangewezen. Zie Dataset voor [logboekverwerking Bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) of gegevensset voor [transformatie bevatten bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) voor beschrijvingen van de parameters.

   Wanneer u een dataset bewerkt met een bestand in een werkbankvenster, kunt u sneltoetsen gebruiken voor de basisbewerkingsfuncties, zoals cut (Ctrl+x), kopiëren (Ctrl+c), plakken (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klik+drag) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst van één configuratiedossier () aan een andere te kopiëren en te kleven. [!DNL .cfg]

1. Om uw veranderingen te bewaren, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort. De opwerking of de retransformatie van de gegevens beginnen na synchronisatie van het datasetprofiel.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

