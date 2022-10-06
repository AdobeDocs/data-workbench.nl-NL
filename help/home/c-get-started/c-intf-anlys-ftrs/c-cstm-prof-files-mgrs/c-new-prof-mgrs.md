---
description: In Profielbeheer worden alle directory's weergegeven die aan uw werkprofiel zijn gekoppeld.
title: Profielbeheer maken
uuid: e16741e2-740b-4f57-861d-e2f57d30abbc
exl-id: 43b95473-ab3e-4a80-9b91-7c221e74b096
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Profielbeheer maken{#create-a-profile-manager}

{{eol}}

In Profielbeheer worden alle directory&#39;s weergegeven die aan uw werkprofiel zijn gekoppeld.

U wilt mogelijk toegang krijgen tot een submap van het dialoogvenster [!DNL Profile Manager] zonder dat u door de volledige mapstructuur hoeft te navigeren. De [!DNL Metrics] en [!DNL Workspaces] de menuopties beschikbaar op [!DNL Manage] in het menu van het werkruimtevenster kunt u respectievelijk de mappen Metriek en Werkruimte van Profielbeheer openen.

Voor meer informatie over de [!DNL Profile Manager], zie [Profielbeheer](https://experienceleague.adobe.com/docs/data-workbench/using/client/ui-analysis-features/cstm-prof-files-mgrs/c-new-prof-mgrs.html).

Standaard hebt u toegang tot de volgende managers:

* **[!DNL Metrics Manager]:** Hiermee geeft u de inhoud van de map Metrics van Profielbeheer weer. U kunt de metriek openen, bewerken, verwijderen of kopiëren die in elk profiel is gedefinieerd.
* **[!DNL Reports Manager]:** Hiermee geeft u de inhoud van de map Reports van Profielbeheer weer. U kunt rapportwerkruimten of [!DNL report.cfg] bestanden.

* **[!DNL Workspaces Manager]:** Hiermee geeft u de inhoud van de map Workspaces van Profielbeheer weer. Alle bestanden voor het configureren van de [!DNL Worktop]De tabbladen van de gebruiker staan hier. Zie [Tabs voor bureaublad aanpassen](../../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-wktp-tabs/c-cstm-wktp-tabs.md).

Met Data Workbench kunt u extra profielmanagers maken die één submap weergeven vanuit de [!DNL Profile Manager]. Elke manager die u creeert moet een [!DNL .vw] bestand dat de [!DNL Profile Manager] map waarvan de inhoud wordt weergegeven en de eigenschappen van dat venster. U kunt de [!DNL .vw] bestand voor een van de opgegeven managers als een sjabloon.

**Profielbeheer maken**

1. In de [!DNL Profile Manager]klikt u op de knop **[!UICONTROL Menu]** om de inhoud ervan weer te geven.
1. Klik in de map Menu op de knop **[!UICONTROL Admin]** en vervolgens de **[!UICONTROL Profile]** directory. De [!DNL .vw] bestanden voor de bestaande managers bevinden zich hier.
1. In de *profielnaam* kolom, klikt u met de rechtermuisknop op het vinkje voor een van de [!DNL .vw] bestanden (bijvoorbeeld [!DNL Workspaces.vw]), klikt u vervolgens op **[!UICONTROL Make Local]**.

   Er verschijnt een vinkje voor het bestand in het dialoogvenster [!DNL User] kolom.

1. Klik met de rechtermuisknop op het vinkje voor het dialoogvenster [!DNL .vw] in het [!DNL User] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. In de [!DNL Profile Path] veld, typt u de [!DNL Profile Manager] map waarvoor u een nieuwe manager wilt maken. Zorg ervoor dat u de schuine streep (/) achter de mapnaam opneemt.

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

1. Klik in Kladblok op **[!UICONTROL File]** > **[!UICONTROL Save As]** om het bewerkte bestand op te slaan in de *Installatiemap Data Workbench*\User\*working profile name*\Menu\Admin\Profile Management.

   Zorg ervoor dat u de naam van de [!DNL .vw] bestand om de map in de [!DNL Profile Manager] waarop zij betrekking heeft.

1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor het [!DNL .vw] in het [!DNL User] kolom en klik op **[!UICONTROL Save to]** > &lt; **[!UICONTROL working profile name]**>.
