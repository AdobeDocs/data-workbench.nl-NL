---
description: In de map Workspaces van de installatiemap van uw Data Workbench geeft een bestand folder.lock aan of de werkruimten in die map zijn vergrendeld, terwijl een bestand workspace name.lock opgeeft of een bepaalde werkruimte is vergrendeld.
title: Map.lock en workspace.lock, bestanden
uuid: d4c69e16-0596-4542-854f-bc614167ae80
exl-id: 980b8692-8aa5-481f-b6bc-33836d8a3a76
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---

# Map.lock en workspace.lock, bestanden{#folder-lock-and-workspace-lock-files}

In de map Workspaces van de installatiemap van uw Data Workbench geeft een bestand folder.lock aan of de werkruimten in die map zijn vergrendeld, terwijl een bestand workspace name.lock opgeeft of een bepaalde werkruimte is vergrendeld.

Wanneer u volledige mappen vergrendelt, kunt u deze vergrendelen op het mapniveau Workspaces of op submapniveau (tabblad). U kunt ook al uw mappen vergrendelen of ontgrendelen (op het mapniveau Workspaces) en vervolgens de uitzonderingen voor bepaalde submappen opgeven (met behulp van [!DNL folder.lock]-bestanden) of bepaalde werkruimten (met behulp van *werkruimtenaam*.lock-bestanden).

In het volgende voorbeeld van [!DNL Profile Manager] worden drie elementen gemarkeerd:

* Een [!DNL folder.lock]-bestand voor de hoofdmap Workspaces
* Een [!DNL Monthly Numbers.lock]-bestand voor het [!DNL Monthly Numbers.vw]-werkruimtebestand

* Een [!DNL folder.lock]-bestand voor de submap Workspaces\Custom

![](assets/wsp_Locking_lockFiles.png)

In dit voorbeeld is het [!DNL Workspaces folder.lock]-bestand ingesteld op vergrendeld, waardoor alle werkruimten in deze instantie van Data Workbench worden vergrendeld. De submap [!DNL folder.lock] van Workspaces\Custom is ingesteld op ontgrendeld, waardoor alle werkruimten op het tabblad [!DNL Custom] worden ontgrendeld. Tot slot wordt het [!DNL Monthly Numbers.lock] dossier geplaatst aan gesloten, die de werkruimte van Maandelijkse Aantallen sluit.

## .lock-bestanden maken {#section-c4f78b4b43c347368a376904effb41d2}

U kunt een [!DNL new folder.lock] dossier tot stand brengen gebruikend [!DNL Create menu] optie in [!DNL Profile Manager] of [!DNL Workspaces Manager]. U kunt ook een [!DNL folder.lock]- of *werkruimtenaam*.lock-bestand maken door een bestaand [!DNL .lock]-bestand naar de juiste map te kopiëren en te plakken, waarbij de naam van het bestand wordt gewijzigd (alleen voor *werkruimtenaam*.lock-bestanden) en de instelling in het bestand indien nodig wordt gewijzigd.

**Een nieuw bestand folder.lock maken**

1. Open in Data Workbench de [!DNL Workspaces Manager] door met de rechtermuisknop in een werkruimte te klikken en **[!UICONTROL Manage]** > **[!UICONTROL Profile]** > **[!UICONTROL Workspaces Manager]** te klikken.
1. Klik op de map waarvoor u een [!DNL folder.lock]-bestand wilt maken.
1. Klik in de kolom [!DNL User] voor die map met de rechtermuisknop in de cel en klik op **[!UICONTROL Create]** > **[!UICONTROL folder.lock]**. Er wordt een [!DNL new folder.lock]-bestand weergegeven. [!DNL New folder.lock] bestanden worden standaard  [] ontgrendeld.
1. (Optioneel) Als u de instelling in het bestand wilt wijzigen:

   1. Klik met de rechtermuisknop op het vinkje voor het bestand.
   1. Klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL folder.lock] dossier opent.

   1. Wijzig de instelling in [locked].
   1. Sla het bestand op en sluit het.

1. Als u deze instelling wilt instellen voor alle gebruikers die met hetzelfde werkprofiel werken, klikt u met de rechtermuisknop op het vinkje voor het bestand en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***.

De werkruimten in deze map zijn nu vergrendeld of ontgrendeld volgens de instelling in het nieuwe bestand.

**Een .lock-bestand maken van een bestaand bestand**

1. Klik in [!DNL Profile Manager] of [!DNL Workspaces Manager] met de rechtermuisknop op het vinkje voor een bestaand [!DNL .lock]-bestand en klik op **[!UICONTROL Copy]**.
1. Klik in de kolom [!DNL User] voor de map waarin u het [!DNL .lock]-bestand wilt plakken met de rechtermuisknop in de cel en klik op **[!UICONTROL Paste]**.
1. Als dit bestand wordt gebruikt om een afzonderlijke werkruimte te vergrendelen, klikt u met de rechtermuisknop op het vinkje voor het bestand [!DNL .lock] in de kolom [!DNL User] en wijzigt u de naam in het veld [!DNL File] zodat deze overeenkomt met de naam van de werkruimte die u wilt vergrendelen.

   Als u bijvoorbeeld de werkruimte [!DNL Monthly Numbers.vw] wilt vergrendelen, geeft u het bestand de naam &quot;[!DNL Monthly Numbers.lock]&quot;.Als dit bestand wordt gebruikt om een afzonderlijke werkruimte te vergrendelen, klikt u met de rechtermuisknop op het vinkje voor het bestand [!DNL .lock] in de kolom [!DNL User] en wijzigt u de naam in het veld [!DNL File] zodat deze overeenkomt met de naam van de werkruimte die u wilt vergrendelen. Als u bijvoorbeeld de werkruimte [!DNL Monthly Numbers.vw] wilt vergrendelen, geeft u het bestand de naam &quot;[!DNL Monthly Numbers.lock]&quot;.

1. U wijzigt de instelling in het bestand als volgt:

   1. Klik met de rechtermuisknop op het vinkje voor het bestand.
   1. Klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL .lock] dossier opent.

   1. Wijzig de instelling in [locked] of [unlocked].
   1. Sla het bestand op en sluit het.

1. Als u deze instelling wilt instellen voor alle gebruikers die met hetzelfde werkprofiel werken, klikt u met de rechtermuisknop op het vinkje voor het bestand en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***.

De geselecteerde werkruimten zijn nu vergrendeld of ontgrendeld volgens de instelling in het nieuwe bestand.
