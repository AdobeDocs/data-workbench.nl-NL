---
description: De manager van de Dossiers van de Server toont alle folders in de de serverinstallatiefolder van de Werkbank van Gegevens, met inbegrip van configuratie en opiniedossiers.
solution: Analytics
title: Serverbestandsbeheer maken
topic: Data workbench
uuid: 9fb2163d-3756-40d2-9817-4a89bd8a38c9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Serverbestandsbeheer maken{#create-a-server-files-manager}

De manager van de Dossiers van de Server toont alle folders in de de serverinstallatiefolder van de Werkbank van Gegevens, met inbegrip van configuratie en opiniedossiers.

U kunt tot een gedeelte van willen toegang hebben [!DNL Server Files Manager] zonder het moeten zijn volledige folderstructuur navigeren of slechts een paar subdirectories tonen om een bepaalde behoefte te richten. Bijvoorbeeld, zou u een afzonderlijk kunnen willen tot stand brengen [!DNL Server Files Manager] die slechts het Toegangsbeheer en subdirectories van Gebruikers toont, toelatend u om uw gebruikers en hun toegang te beheren.

Elke manager die u creeert moet een [!DNL .vw] dossier hebben. U kunt het [!DNL Server Files.vw] dossier als malplaatje gebruiken.

Voor meer informatie over [!DNL Server Files Manager], zie [de Manager](../../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4)van de Dossiers van de Server.

**Om een Manager van de Dossiers van de Server te creëren**

1. In [!DNL Profile Manager], klik de **[!UICONTROL Menu]** folder, toen de **[!UICONTROL Admin]** folder. Het [!DNL Server Files.vw] bestand bevindt zich hier.
1. Klik in de kolom *profielnaam* met de rechtermuisknop op het vinkje voor het [!DNL Server Files.vw] bestand en klik op **[!UICONTROL Make Local]**. Een vinkje voor het dossier verschijnt in de [!DNL User] kolom.
1. Klik het vinkje voor het [!DNL Server Files.vw] dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL Server Files.vw] bestand wordt geopend.
1. Als u een directory wilt verwijderen, klikt u met de rechtermuisknop op de bovenste rand van de map [!DNL Server Files Manager] en klikt u **[!UICONTROL Server Directories]** > **[!UICONTROL Remove]** > *&lt;**[!UICONTROL directory name]**>*.
1. Om een folder toe te voegen, klik de hoogste grens van met de rechtermuisknop aan [!DNL Server Files Manager], klik **[!UICONTROL Server Directories]** > **[!UICONTROL Add]** > **[!UICONTROL Directory]**.

   Typ URI van de folder op het gebied van URI, en klik **[!UICONTROL OK]**.

   >[!NOTE]
   >
   >U kunt veelvoudige folders op het gebied van URI aanwijzen. Bijvoorbeeld, als u [!DNL Profiles\Marketing\] typt, bevat de manager van serverdossiers de op de markt brengende subdirectory, maar geen andere subdirectory binnen de folder van Profielen.

1. Klik de bovenkant van de hoogste grens van met de rechtermuisknop aan [!DNL Server Files Manager] en klik **[!UICONTROL Save]**.
1. Om een nieuwe manager te creëren, verander het dossier - noem op het [!DNL File Name] gebied, dan klik **[!UICONTROL Save]**. Om de bestaande manager te beschrijven, klik **[!UICONTROL Save]**.
1. (Facultatief) om de veranderingen ter beschikking te stellen van alle gebruikers van het het werk profiel, klik het vinkje voor het [!DNL .vw] dossier in de [!DNL User] kolom met de rechtermuisknop aan.

   Klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

