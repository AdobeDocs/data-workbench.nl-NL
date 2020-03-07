---
description: Binnen de omslag van Werkruimten van uw de installatiefolder van de Werkbank van Gegevens, specificeert een folder.lock- dossier of de werkruimten in die bepaalde omslag gesloten zijn, terwijl een werkruimte name.lock- dossier specificeert of een bepaalde werkruimte gesloten is.
solution: Analytics
title: Folder.lock en werkruimte.lock- dossiers
topic: Data workbench
uuid: d4c69e16-0596-4542-854f-bc614167ae80
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Folder.lock en werkruimte.lock- dossiers{#folder-lock-and-workspace-lock-files}

Binnen de omslag van Werkruimten van uw de installatiefolder van de Werkbank van Gegevens, specificeert een folder.lock- dossier of de werkruimten in die bepaalde omslag gesloten zijn, terwijl een werkruimte name.lock- dossier specificeert of een bepaalde werkruimte gesloten is.

Wanneer het sluiten van volledige omslagen, kunt u hen op het de omslagniveau van Werkruimten of op het subfolder (lusje) niveau sluiten. U kunt ook al uw omslagen (op het de omslagniveau van Werkruimten) sluiten of openen, dan de uitzonderingen voor bepaalde sub-omslagen (gebruikend [!DNL folder.lock] dossiers) of bepaalde werkruimten (gebruikend *werkruimtenaam*.lock- dossiers) specificeren.

Het volgende voorbeeld van de [!DNL Profile Manager] hoogtepunten drie elementen:

* Een [!DNL folder.lock] dossier voor de belangrijkste omslag van Werkruimten
* Een [!DNL Monthly Numbers.lock] dossier voor het [!DNL Monthly Numbers.vw] werkruimtedossier

* Een [!DNL folder.lock] dossier voor de subfolder van de Werkruimten \ van de Douane

![](assets/wsp_Locking_lockFiles.png)

In dit voorbeeld, wordt het [!DNL Workspaces folder.lock] dossier geplaatst aan gesloten, die alle werkruimten in deze instantie van de Werkbank van Gegevens sluit. Het sub-omslagdossier van de Werkruimten \ van de Douane wordt geplaatst aan ontgrendeld, dat alle werkruimten op de [!DNL folder.lock] [!DNL Custom] tabel ontgrendelt. Tot slot wordt het [!DNL Monthly Numbers.lock] dossier geplaatst aan gesloten, die de Maandelijkse werkruimte van de Aantallen sluit.

## .lock-bestanden maken {#section-c4f78b4b43c347368a376904effb41d2}

U kunt een [!DNL new folder.lock] dossier tot stand brengen gebruikend de [!DNL Create menu] optie in [!DNL Profile Manager] of [!DNL Workspaces Manager]. U kunt een [!DNL folder.lock] of *werkruimte ook creëren - noem*.lock- dossier door een bestaand [!DNL .lock] dossier te kopiëren en te kleven in de aangewezen omslag, de naam van het dossier te veranderen (voor *werkruimte - noem*.lock- dossiers slechts), en het plaatsen in het dossier indien nodig te veranderen.

**Om een nieuw folder.lock- dossier te creëren**

1. In de Werkbank van Gegevens, open de [!DNL Workspaces Manager] door binnen een werkruimte met de rechtermuisknop te klikken en te klikken **[!UICONTROL Manage]** > **[!UICONTROL Profile]** > **[!UICONTROL Workspaces Manager]**.
1. Klik de omslag waarvoor u een [!DNL folder.lock] dossier wilt tot stand brengen.
1. In de [!DNL User] kolom voor die omslag, klik in de cel met de rechtermuisknop aan en klik **[!UICONTROL Create]** > **[!UICONTROL folder.lock]**. Er verschijnt een [!DNL new folder.lock] bestand. [!DNL New folder.lock] de dossiers worden geplaatst aan [ontgrendeld] door gebrek.
1. (Facultatief) als u het plaatsen in het dossier moet veranderen:

   1. Klik het vinkje voor het dossier met de rechtermuisknop aan.
   1. Klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL folder.lock] bestand wordt geopend.

   1. Verander het plaatsen in [gesloten].
   1. Sparen en sluit het dossier.

1. Om dit de instelling te maken voor alle gebruikers die met hetzelfde werkprofiel werken, klikt u met de rechtermuisknop op het vinkje voor het bestand en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

De werkruimten in deze omslag zijn nu gesloten of geopend volgens het plaatsen in het nieuwe dossier.

**Om een.lock- dossier van een bestaand dossier te creëren**

1. In [!DNL Profile Manager] of [!DNL Workspaces Manager], klik het vinkje voor een bestaand [!DNL .lock] dossier met de rechtermuisknop aan en klik **[!UICONTROL Copy]**.
1. In de [!DNL User] kolom voor de omslag waarin u het [!DNL .lock] dossier wilt kleven, klik in de cel met de rechtermuisknop aan en klik **[!UICONTROL Paste]**.
1. Als dit dossier wordt gebruikt om een individuele werkruimte te sluiten, klik het vinkje voor het [!DNL .lock] dossier in de [!DNL User] kolom met de rechtermuisknop aan en verander zijn naam op het [!DNL File] gebied om de naam van de werkruimte aan te passen die u wilt sluiten.

   Bijvoorbeeld, om de [!DNL Monthly Numbers.vw] werkruimte te sluiten, zou u het dossier &quot; [!DNL Monthly Numbers.lock]&quot; noemen.Als dit dossier wordt gebruikt om een individuele werkruimte te sluiten, klik het vinkje voor het [!DNL .lock] dossier in de [!DNL User] kolom met de rechtermuisknop aan en verander zijn naam op het [!DNL File] gebied om de naam van de werkruimte aan te passen die u wilt sluiten. Bijvoorbeeld, om de [!DNL Monthly Numbers.vw] werkruimte te sluiten, zou u het dossier &quot; [!DNL Monthly Numbers.lock]&quot; noemen.

1. Om het plaatsen in het dossier te veranderen:

   1. Klik het vinkje voor het dossier met de rechtermuisknop aan.
   1. Klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL .lock] bestand wordt geopend.

   1. Verander het plaatsen in [gesloten] of [ontgrendeld].
   1. Sparen en sluit het dossier.

1. Om dit de instelling te maken voor alle gebruikers die met hetzelfde werkprofiel werken, klikt u met de rechtermuisknop op het vinkje voor het bestand en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

De geselecteerde werkruimten zijn nu vergrendeld of ontgrendeld volgens de instelling in het nieuwe bestand.
