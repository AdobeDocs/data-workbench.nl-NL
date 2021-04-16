---
description: In Profielbeheer worden alle directory's weergegeven die aan uw werkprofiel zijn gekoppeld.
title: Profielbeheer maken
uuid: e16741e2-740b-4f57-861d-e2f57d30abbc
exl-id: 43b95473-ab3e-4a80-9b91-7c221e74b096
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# Profielbeheer maken{#create-a-profile-manager}

In Profielbeheer worden alle directory&#39;s weergegeven die aan uw werkprofiel zijn gekoppeld.

U kunt tot subdirectory van [!DNL Profile Manager] willen toegang hebben zonder het moeten zijn volledige folderstructuur navigeren. Met de menuopties [!DNL Metrics] en [!DNL Workspaces] in het menu [!DNL Manage] van het menu van het werkruimtevenster kunt u bijvoorbeeld respectievelijk de mappen Metriek en Werkruimten van Profielbeheer openen.

Zie [Profielbeheer](https://docs.adobe.com/content/help/en/data-workbench/using/client/ui-analysis-features/cstm-prof-files-mgrs/c-new-prof-mgrs.html) voor meer informatie over [!DNL Profile Manager].

Standaard hebt u toegang tot de volgende managers:

* **[!DNL Metrics Manager]:** Hiermee geeft u de inhoud van de map Metrics van Profielbeheer weer. U kunt de metriek openen, bewerken, verwijderen of kopiëren die in elk profiel is gedefinieerd.
* **[!DNL Reports Manager]:** Hiermee geeft u de inhoud van de map Rapporten van Profielbeheer weer. U kunt rapportwerkruimten of [!DNL report.cfg]-bestanden openen, bewerken, verwijderen of kopiëren.

* **[!DNL Workspaces Manager]:** Hiermee geeft u de inhoud van de map Workspaces van Profielbeheer weer. Alle bestanden voor het configureren van de tabbladen van [!DNL Worktop] bevinden zich hier. Zie [Werkdesktoptabs aanpassen](../../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-wktp-tabs/c-cstm-wktp-tabs.md).

Met Data Workbench kunt u extra profielmanagers maken die één submap van de [!DNL Profile Manager] weergeven. Elke manager die u creeert moet een [!DNL .vw] dossier hebben dat [!DNL Profile Manager] folder specificeert waarvan inhoud het toont en de eigenschappen van dat venster. U kunt het [!DNL .vw] dossier voor om het even welke verstrekte managers als malplaatje gebruiken.

**Profielbeheer maken**

1. Klik in [!DNL Profile Manager] op de map **[!UICONTROL Menu]** om de inhoud ervan weer te geven.
1. Klik in de map Menu op de map **[!UICONTROL Admin]** en vervolgens op de map **[!UICONTROL Profile]**. De [!DNL .vw] dossiers voor de bestaande managers worden hier gevestigd.
1. Klik in de kolom *profielnaam* met de rechtermuisknop op het vinkje voor een van de [!DNL .vw]-bestanden (bijvoorbeeld [!DNL Workspaces.vw]) en klik vervolgens op **[!UICONTROL Make Local]**.

   Er wordt een vinkje voor het bestand weergegeven in de kolom [!DNL User].

1. Klik met de rechtermuisknop op het vinkje voor het [!DNL .vw]-bestand in de kolom [!DNL User] en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. Typ in het veld [!DNL Profile Path] de map [!DNL Profile Manager] waarvoor u een nieuwe manager wilt maken. Zorg ervoor dat u de schuine streep (/) achter de mapnaam opneemt.

   ```
   window = simpleBorderWindow:
   client = scrollWindow: 
   client = fileManager:
     Profile Path = string: directory name/
     size = v3d: (820, 5649, 0)
     scroll_offset = v3d: (0, 0, 0)
     size = v3d: (830, 881, 0)
     pos = v3d: (525, 162, 0)
     size = v3d: (830, 900, 0)
   ```

1. Klik in Kladblok op **[!UICONTROL File]** > **[!UICONTROL Save As]** om het bewerkte bestand op te slaan in de installatiemap *Data Workbench*\User\*werkprofielnaam*\Menu\Admin\Profile Management.

   Vergeet niet de naam van het [!DNL .vw]-bestand te wijzigen om de map weer te geven in de [!DNL Profile Manager] die het bestand benadert.

1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor het bestand [!DNL .vw] in de kolom [!DNL User] en klikt u op **[!UICONTROL Save to]** > &lt; **[!UICONTROL working profile name]**>.
