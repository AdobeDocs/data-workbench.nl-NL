---
description: De nieuwe afmetingen die u het gebruiken van de Werkbank van Gegevens creeert (die als afgeleide afmetingen wordt bedoeld) zijn cliënt-zijafmetingen.
solution: Analytics
title: Werken met afgeleide afmetingen
topic: Data workbench
uuid: 3a955fdc-6666-40ab-aee0-bd23c260c009
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Werken met afgeleide afmetingen{#work-with-derived-dimensions}

De nieuwe afmetingen die u het gebruiken van de Werkbank van Gegevens creeert (die als afgeleide afmetingen wordt bedoeld) zijn cliënt-zijafmetingen.

In plaats van het bepalen van deze afmetingen tijdens de datasetconstructie en updateproces (in het [!DNL Transformation.cfg] dossier) op uw de servercomputers van de Werkbank van Gegevens, worden de afgeleide afmetingen gecreeerd en individueel opgeslagen als [!DNL .dim] dossiers in een profiel. Dientengevolge, kunt u het bestaan veranderen en nieuwe afgeleide afmetingen tot stand brengen zonder uw dataset opnieuw te verwerken.

>[!NOTE]
>
>Voor meer informatie over afmetingen dan in deze sectie wordt verstrekt, zie de aangewezen de toepassingsgids van de Werkbank van Gegevens.

Voor meer informatie over de datasetconfiguratie en het updateproces, zie de Gids *van de Configuratie van de* Dataset.

## Creeer een afgeleide afmetingen {#section-fd9b6ca13a8f4aa9bbc2fff3ef15cb76}

Om een afgeleide afmeting tot stand te brengen, kunt u of een bestaande afmeting kopiëren en wijzigen of een afmeting bewaren van een visualisatie.

## Creeer een afgeleide afmetingen van een bestaande afmeting {#section-f46c2d3ab0a5416c98d6e79d18d99fa1}

De gebruikers willen het vaakst nieuwe tijddimensies van bestaande degenen tot stand brengen. Bijvoorbeeld, kunt u een nieuwe &quot;Laatste 5 Dagen&quot;dimensie van de bestaande &quot;Afgelopen 7 Dagen&quot;dimensie tot stand brengen.

1. In [!DNL Profile Manager], in de kolom van de *profielnaam* , klik het vinkje voor een afmeting met de rechtermuisknop aan die aan de afmeting gelijkaardig is die u wilt tot stand brengen en klikken **[!UICONTROL Copy]**.

   Bijvoorbeeld, om [!DNL Last 7 Days.dim] van de omslag van de Rapportering van het [!DNL Traffic] profiel te kopiëren, klikt u het vinkje voor het dossier met de rechtermuisknop aan - noem in de [!DNL Traffic] kolom en klikt **[!UICONTROL Copy]**.

   ![](assets/vis_ProfMgr_CopyDimension.png)

1. Klik in de [!DNL User] kolom voor de omslag met de rechtermuisknop aan waarin u de gekopieerde dimensie wilt opslaan en klikken **[!UICONTROL Paste]**.

   De afmeting verschijnt in de geselecteerde omslag van Afmetingen met een vinkje in de [!DNL User] kolom.

1. Om de nieuwe dimensie anders te noemen, klik zijn vinkje in de [!DNL User] kolom met de rechtermuisknop aan en typ de nieuwe naam op het [!DNL File] gebied.
1. Klik in het menu met de rechtermuisknop op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De bepalende parameters voor de afmeting verschijnen.
1. Wijzig de parameters zoals nodig om de nieuwe dimensie te bepalen.

   Voor tijddimensies, zult u waarschijnlijk slechts de de parameters van de Telling en van de Waaier moeten wijzigen.

1. Om het dossier te bewaren, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   Als u alle gebruikers van een profiel zou willen om de dimensie te gebruiken die u creeerde, moet u het aan het profiel uploaden gebruikend [!DNL Profile Manager]. Voor meer informatie, zie het [Publiceren van Dossiers aan Uw het Werk Profiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).

U kunt nu de nieuwe dimensie door het huidige profiel gebruiken door het te selecteren aangezien u om het even welke ingebouwde dimensie.

## Sparen een afmeting van een visualisatie {#section-84cfe5e9ccb640afa2ee4e2da2682757}

U kunt uitgebreide afmetingen van proceskaarten en segmenten bewaren. Voor stappen om een afmeting van een proceskaart te bewaren, zie het [Opslaan van Afmetingen van de Kaarten](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/t-dim-proc-maps.md#task-44d9e555d4a944e6aa81993eef703051)van het Proces. Voor stappen om een segmentafmeting te bewaren, zie het [Creëren van de Afmetingen](../../../../home/c-get-started/c-analysis-vis/c-seg/c-create-seg-dim.md#concept-70b363edcad14185ba8051646ad3d44e) van het Segment op pagina 82.

## Een segment opslaan als een dimensie {#section-7c443cf1ac5a44659623cabb9e0c1ab8}

U kunt ook gedefinieerde segmenten opslaan als een dimensie. Voor stappen, zie het [Hergebruiken van een Visualisatie](../../../../home/c-get-started/c-analysis-vis/c-seg/c-reuse-seg-vis.md#concept-a8a607bd415d404a83c32a26b804cbdc)van het Segment.

## Een bestaande afgeleide dimensie bewerken {#section-3a82c604bf1c4d369770556d268808b2}

1. I

   In [!DNL Profile Manager], in de kolom van de *profielnaam* , klik het vinkje voor het afmetingsdossier met de rechtermuisknop aan dat u wilt uitgeven en klikken **[!UICONTROL Make Local]**.
1. Klik het vinkje voor het afmetingsdossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.
1. Voltooi de parameters zoals nodig. Voor meer informatie, contacteer de Raadplegende Diensten van Adobe.
1. Om het dossier te bewaren, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   Als u alle gebruikers van een profiel zou willen om de gewijzigde dimensie te gebruiken, moet u het aan het profiel uploaden gebruikend [!DNL Profile Manager]. Voor meer informatie, zie het [Publiceren van Dossiers aan Uw het Werk Profiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).

