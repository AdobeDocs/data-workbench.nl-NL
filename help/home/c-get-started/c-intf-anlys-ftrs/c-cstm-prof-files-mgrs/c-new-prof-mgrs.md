---
description: De profielmanager toont alle folders verbonden aan uw werkend profiel.
solution: Analytics
title: Profielbeheer maken
topic: Data workbench
uuid: e16741e2-740b-4f57-861d-e2f57d30abbc
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Profielbeheer maken{#create-a-profile-manager}

De profielmanager toont alle folders verbonden aan uw werkend profiel.

U kunt tot subdirectory van willen toegang hebben [!DNL Profile Manager] zonder het moeten zijn volledige folderstructuur navigeren. Bijvoorbeeld, laten de [!DNL Metrics] en [!DNL Workspaces] menuopties beschikbaar op het [!DNL Manage] menu van het menu van het werkruimtevenster u toe om de de Metriek van de Manager van het Profiel en omslagen van de Werkruimten, respectievelijk te openen.

Voor meer informatie over [!DNL Profile Manager], zie [de Manager](https://docs.adobe.com/content/help/en/data-workbench/using/client/ui-analysis-features/cstm-prof-files-mgrs/c-new-prof-mgrs.html)van het Profiel.

Door gebrek hebt u toegang tot de volgende managers:

* **[!DNL Metrics Manager]:**Toont de inhoud van de omslag van de Metriek van de Manager van het Profiel. U kunt, de metriek openen uitgeven, verwijderen of kopiëren die binnen elk profiel wordt bepaald.
* **[!DNL Reports Manager]:**Toont de inhoud van de omslag van de Rapporten van de Manager van het Profiel. U kunt, rapportwerkruimten of[!DNL report.cfg]dossiers openen uitgeven, verwijderen of kopiëren.

* **[!DNL Workspaces Manager]:**Toont de inhoud van de omslag van de Werkruimten van de Manager van het Profiel. Alle dossiers voor het vormen van de lusjes van de[!DNL Worktop]lusjes worden hier gevestigd. Zie Tabs[Aanpassen](../../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-wktp-tabs/c-cstm-wktp-tabs.md)voor bureaublad.

De Werkbank van gegevens laat u toe om extra profielmanagers tot stand te brengen die één subdirectory van tonen [!DNL Profile Manager]. Elke manager die u creeert moet een [!DNL .vw] dossier hebben dat de [!DNL Profile Manager] folder specificeert de waarvan inhoud het en de eigenschappen van dat venster toont. U kunt het [!DNL .vw] dossier voor om het even welke verstrekte managers als malplaatje gebruiken.

**Een profielbeheer maken**

1. In [!DNL Profile Manager], klik de **[!UICONTROL Menu]** folder om zijn inhoud te bekijken.
1. Binnen de folder van het Menu, klik de **[!UICONTROL Admin]** folder en toen de **[!UICONTROL Profile]** folder. De [!DNL .vw] dossiers voor de bestaande managers worden hier gevestigd.
1. In de kolom van de *profielnaam* , klik het vinkje voor één van de [!DNL .vw] dossiers (bijvoorbeeld, [!DNL Workspaces.vw]) met de rechtermuisknop aan, dan klik **[!UICONTROL Make Local]**.

   Een vinkje voor het dossier verschijnt in de [!DNL User] kolom.

1. Klik het vinkje voor het [!DNL .vw] dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. Op het [!DNL Profile Path] gebied, typ de [!DNL Profile Manager] folder waarvoor u een nieuwe manager wilt tot stand brengen. Ben zeker om de schuine streep (/) na de foldernaam te omvatten.

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

1. In Blocnote, klik **[!UICONTROL File]** > **[!UICONTROL Save As]** om het uitgegeven dossier aan de de installatiemap *van de Werkbank van* Gegevens op te slaan \User\*working profiel name*\Menu\Admin\Profile Management.

   Ben zeker om de naam van het [!DNL .vw] dossier te veranderen om op de folder te wijzen [!DNL Profile Manager] waaraan het beantwoordt.

1. (Facultatief) om de veranderingen beschikbaar te maken voor alle gebruikers van het het werkprofiel, klik het vinkje voor het [!DNL .vw] dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Save to]** > &lt; **[!UICONTROL working profile name]**>.

