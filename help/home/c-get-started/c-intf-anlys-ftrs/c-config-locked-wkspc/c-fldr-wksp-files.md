---
description: In de map Workspaces van de installatiemap van uw Data Workbench geeft een bestand folder.lock aan of de werkruimten in die map zijn vergrendeld, terwijl een bestand workspace name.lock opgeeft of een bepaalde werkruimte is vergrendeld.
title: Map.lock en workspace.lock, bestanden
uuid: d4c69e16-0596-4542-854f-bc614167ae80
exl-id: 980b8692-8aa5-481f-b6bc-33836d8a3a76
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---

# Map.lock en workspace.lock, bestanden{#folder-lock-and-workspace-lock-files}

{{eol}}

In de map Workspaces van de installatiemap van uw Data Workbench geeft een bestand folder.lock aan of de werkruimten in die map zijn vergrendeld, terwijl een bestand workspace name.lock opgeeft of een bepaalde werkruimte is vergrendeld.

Wanneer u volledige mappen vergrendelt, kunt u deze vergrendelen op het mapniveau Workspaces of op submapniveau (tabblad). U kunt ook al uw mappen vergrendelen of ontgrendelen (op het mapniveau Workspaces) en vervolgens de uitzonderingen voor bepaalde submappen opgeven (met [!DNL folder.lock] bestanden) of bepaalde werkruimten (gebruiken *naam werkruimte*.lock files).

In het volgende voorbeeld van het [!DNL Profile Manager] benadrukt drie elementen:

* A [!DNL folder.lock] bestand voor de hoofdmap Workspaces
* A [!DNL Monthly Numbers.lock] bestand voor de [!DNL Monthly Numbers.vw] werkruimtebestand

* A [!DNL folder.lock] bestand voor de submap Workspaces\Custom

![](assets/wsp_Locking_lockFiles.png)

In dit voorbeeld wordt [!DNL Workspaces folder.lock] bestand is ingesteld op vergrendeld, waardoor alle werkruimten in deze instantie van Data Workbench worden vergrendeld. De submap Workspaces\Custom [!DNL folder.lock] bestand is ingesteld op ontgrendeld, waardoor alle werkruimten op het tabblad [!DNL Custom] tab. Tot slot [!DNL Monthly Numbers.lock] bestand is ingesteld op vergrendeld, waardoor de werkruimte Maandnummers wordt vergrendeld.

## .lock-bestanden maken {#section-c4f78b4b43c347368a376904effb41d2}

U kunt een [!DNL new folder.lock] bestand met de [!DNL Create menu] in de [!DNL Profile Manager] of de [!DNL Workspaces Manager]. U kunt ook een [!DNL folder.lock] of *naam werkruimte*.lock-bestand door een bestaand bestand te kopiëren en te plakken [!DNL .lock] bestand naar de juiste map, waarbij de naam van het bestand wordt gewijzigd (voor *naam werkruimte*.lock files only), en het veranderen van het plaatsen in het dossier indien nodig.

**Een nieuw bestand folder.lock maken**

1. Open in Data Workbench de [!DNL Workspaces Manager] door met de rechtermuisknop in een werkruimte te klikken en te klikken **[!UICONTROL Manage]** > **[!UICONTROL Profile]** > **[!UICONTROL Workspaces Manager]**.
1. Klik op de map waarvoor u een [!DNL folder.lock] bestand.
1. In de [!DNL User] voor die map klikt u met de rechtermuisknop in de cel en klikt u op **[!UICONTROL Create]** > **[!UICONTROL folder.lock]**. A [!DNL new folder.lock] wordt weergegeven. [!DNL New folder.lock] bestanden worden ingesteld op [ontgrendeld] standaard.
1. (Optioneel) Als u de instelling in het bestand wilt wijzigen:

   1. Klik met de rechtermuisknop op het vinkje voor het bestand.
   1. Klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. De [!DNL folder.lock] wordt geopend.

   1. De instelling wijzigen in [vergrendeld].
   1. Sla het bestand op en sluit het.

1. Als u deze instelling wilt instellen voor alle gebruikers die met hetzelfde werkprofiel werken, klikt u met de rechtermuisknop op het vinkje voor het bestand en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

De werkruimten in deze map zijn nu vergrendeld of ontgrendeld volgens de instelling in het nieuwe bestand.

**Een .lock-bestand maken van een bestaand bestand**

1. In de [!DNL Profile Manager] of [!DNL Workspaces Manager], klikt u met de rechtermuisknop op het vinkje voor een bestaande [!DNL .lock] bestand en klik op **[!UICONTROL Copy]**.
1. In de [!DNL User] kolom voor de map waarin u de [!DNL .lock] bestand, klikt u met de rechtermuisknop in de cel en klikt u op **[!UICONTROL Paste]**.
1. Als dit bestand wordt gebruikt om een afzonderlijke werkruimte te vergrendelen, klikt u met de rechtermuisknop op het vinkje voor de [!DNL .lock] in het [!DNL User] kolom en wijzig zijn naam in [!DNL File] veld dat overeenkomt met de naam van de werkruimte die u wilt vergrendelen.

   Als u bijvoorbeeld het dialoogvenster [!DNL Monthly Numbers.vw] werkruimte, zou u het dossier &quot; [!DNL Monthly Numbers.lock].&quot;Als dit bestand wordt gebruikt om een afzonderlijke werkruimte te vergrendelen, klikt u met de rechtermuisknop op het vinkje voor de [!DNL .lock] in het [!DNL User] kolom en wijzig zijn naam in [!DNL File] veld dat overeenkomt met de naam van de werkruimte die u wilt vergrendelen. Als u bijvoorbeeld het dialoogvenster [!DNL Monthly Numbers.vw] werkruimte, zou u het dossier &quot; [!DNL Monthly Numbers.lock].&quot;

1. U wijzigt de instelling in het bestand als volgt:

   1. Klik met de rechtermuisknop op het vinkje voor het bestand.
   1. Klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. De [!DNL .lock] wordt geopend.

   1. De instelling wijzigen in [vergrendeld] of [ontgrendeld].
   1. Sla het bestand op en sluit het.

1. Als u deze instelling wilt instellen voor alle gebruikers die met hetzelfde werkprofiel werken, klikt u met de rechtermuisknop op het vinkje voor het bestand en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

De geselecteerde werkruimten zijn nu vergrendeld of ontgrendeld volgens de instelling in het nieuwe bestand.
