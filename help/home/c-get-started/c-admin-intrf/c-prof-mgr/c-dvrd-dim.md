---
description: De nieuwe dimensies die u met Data Workbench maakt (afgeleide dimensies genoemd) zijn clientafmetingen.
title: Werken met afgeleide afmetingen
uuid: 3a955fdc-6666-40ab-aee0-bd23c260c009
exl-id: 5b7e3a2a-ac61-4186-ad6c-234edf68af3e
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# Werken met afgeleide afmetingen{#work-with-derived-dimensions}

De nieuwe dimensies die u met Data Workbench maakt (afgeleide dimensies genoemd) zijn clientafmetingen.

In plaats van deze dimensies tijdens de aanleg en het updateproces van de dataset (in het [!DNL Transformation.cfg] dossier) op uw de servercomputers van de Data Workbench te bepalen, worden de afgeleide dimensies gecreeerd en individueel opgeslagen als [!DNL .dim] dossiers in een profiel. Dientengevolge, kunt u bestaand veranderen en nieuwe afgeleide dimensies creëren zonder uw dataset te herverwerken.

>[!NOTE]
>
>Raadpleeg de toepasselijke handleiding voor de toepassing van Data Workbench voor meer informatie over de afmetingen dan in deze sectie wordt gegeven.

Voor meer informatie over de configuratie en het updateproces van de dataset, zie *de Gids van de Configuratie van de Dataset*.

## Een afgeleide dimensie maken {#section-fd9b6ca13a8f4aa9bbc2fff3ef15cb76}

Als u een afgeleide dimensie wilt maken, kunt u een bestaande dimensie kopiëren en wijzigen of een dimensie opslaan vanuit een visualisatie.

## Een afgeleide dimensie maken van een bestaande dimensie {#section-f46c2d3ab0a5416c98d6e79d18d99fa1}

De gebruikers willen het vaakst nieuwe tijddimensies van bestaande tot stand brengen. U kunt bijvoorbeeld een nieuwe dimensie &quot;Laatste 5 dagen&quot; maken van de bestaande dimensie &quot;Laatste 7 dagen&quot;.

1. Klik in [!DNL Profile Manager] in de kolom *profielnaam* met de rechtermuisknop op het vinkje voor een dimensie die lijkt op de dimensie die u wilt maken en klik op **[!UICONTROL Copy]**.

   Als u bijvoorbeeld [!DNL Last 7 Days.dim] wilt kopiëren vanuit de map Rapportage van het profiel [!DNL Traffic], klikt u met de rechtermuisknop op het vinkje voor de bestandsnaam in de kolom [!DNL Traffic] en klikt u op **[!UICONTROL Copy]**.

   ![](assets/vis_ProfMgr_CopyDimension.png)

1. Klik met de rechtermuisknop in de kolom [!DNL User] voor de map waarin u de gekopieerde dimensie wilt opslaan en klik op **[!UICONTROL Paste]**.

   De dimensie wordt weergegeven in de map met geselecteerde Dimension met een vinkje in de kolom [!DNL User].

1. Als u de naam van de nieuwe dimensie wilt wijzigen, klikt u met de rechtermuisknop op het vinkje in de kolom [!DNL User] en typt u de nieuwe naam in het veld [!DNL File].
1. Klik in het snelmenu met de rechtermuisknop op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De definiërende parameters voor de dimensie worden weergegeven.
1. Wijzig zo nodig de parameters om de nieuwe dimensie te definiëren.

   Voor tijddimensies, moet u hoogstwaarschijnlijk slechts de parameters van de Telling en van de Waaier wijzigen.

1. Als u het bestand wilt opslaan, klikt u met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klikt u op **[!UICONTROL Save]**.

   Als u wilt dat alle gebruikers van een profiel de dimensie gebruiken die u hebt gemaakt, moet u het naar het profiel uploaden met de [!DNL Profile Manager]. Zie [Bestanden publiceren naar uw werkprofiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9) voor meer informatie.

U kunt nu de nieuwe dimensie in het hele huidige profiel gebruiken door deze te selecteren zoals u elke ingebouwde dimensie zou gebruiken.

## Dimensies opslaan vanuit een visualisatie {#section-84cfe5e9ccb640afa2ee4e2da2682757}

U kunt uitgebreide afmetingen opslaan op basis van procestoewijzingen en segmenten. Voor stappen om een afmeting van een proceskaart te bewaren, zie [Dimension van Proceskaarten](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/t-dim-proc-maps.md#task-44d9e555d4a944e6aa81993eef703051) bewaren. Zie [Segment-Dimension maken](../../../../home/c-get-started/c-analysis-vis/c-seg/c-create-seg-dim.md#concept-70b363edcad14185ba8051646ad3d44e) op pagina 82 voor stappen om een segmentdimensie op te slaan.

## Een segment opslaan als een dimensie {#section-7c443cf1ac5a44659623cabb9e0c1ab8}

U kunt gedefinieerde segmenten ook opslaan als een dimensie. Zie [Een segmentvisualisatie opnieuw gebruiken](../../../../home/c-get-started/c-analysis-vis/c-seg/c-reuse-seg-vis.md#concept-a8a607bd415d404a83c32a26b804cbdc) voor stappen.

## Een bestaande afgeleide dimensie bewerken {#section-3a82c604bf1c4d369770556d268808b2}

1. I

   Klik in [!DNL Profile Manager] in de kolom *profielnaam* met de rechtermuisknop op het vinkje voor het dimensiebestand dat u wilt bewerken en klik op **[!UICONTROL Make Local]**.
1. Klik met de rechtermuisknop op het vinkje voor het dimensiebestand in de kolom [!DNL User] en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.
1. Voltooi indien nodig de parameters. Neem voor meer informatie contact op met de Adobe Consulting Services.
1. Als u het bestand wilt opslaan, klikt u met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klikt u op **[!UICONTROL Save]**.

   Als u wilt dat alle gebruikers van een profiel de gewijzigde dimensie gebruiken, moet u het naar het profiel uploaden met de [!DNL Profile Manager]. Zie [Bestanden publiceren naar uw werkprofiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9) voor meer informatie.
