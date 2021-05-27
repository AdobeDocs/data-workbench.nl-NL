---
description: Serverbeheer geeft alle mappen in de installatiemap van de Data Workbench-server weer, inclusief configuratie- en opzoekbestanden.
title: Serverbestandsbeheer maken
uuid: 9fb2163d-3756-40d2-9817-4a89bd8a38c9
exl-id: 9e0c8144-0f52-4e46-85d8-c2dcd60ddcb8
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Een serverbestandsbeheer maken{#create-a-server-files-manager}

Serverbeheer geeft alle mappen in de installatiemap van de Data Workbench-server weer, inclusief configuratie- en opzoekbestanden.

U kunt tot een gedeelte van [!DNL Server Files Manager] willen toegang hebben zonder het moeten zijn volledige folderstructuur navigeren of slechts een paar subdirectories tonen om een bepaalde behoefte te richten. Bijvoorbeeld, zou u een afzonderlijke [!DNL Server Files Manager] kunnen willen tot stand brengen die slechts het Toegangsbeheer en de subdirectories van Gebruikers toont, toelatend u om uw gebruikers en hun toegang te beheren.

Elke manager die u creeert moet een [!DNL .vw] dossier hebben. U kunt het [!DNL Server Files.vw] dossier als malplaatje gebruiken.

Voor meer informatie over [!DNL Server Files Manager], zie [De Manager van de Dossiers van de Server](../../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4).

**Serverbestandsbeheer maken**

1. Klik in [!DNL Profile Manager] op de map **[!UICONTROL Menu]** en vervolgens op de map **[!UICONTROL Admin]**. Het [!DNL Server Files.vw]-bestand bevindt zich hier.
1. Klik in de kolom *profielnaam* met de rechtermuisknop op het vinkje voor het [!DNL Server Files.vw]-bestand en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor het bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het vinkje voor het [!DNL Server Files.vw]-bestand in de kolom [!DNL User] en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL Server Files.vw] dossier opent.
1. Als u een map wilt verwijderen, klikt u met de rechtermuisknop op de bovenrand van [!DNL Server Files Manager] en klikt u op **[!UICONTROL Server Directories]** > **[!UICONTROL Remove]** > *&lt;**[!UICONTROL directory name]**>*.
1. Als u een map wilt toevoegen, klikt u met de rechtermuisknop op de bovenrand van [!DNL Server Files Manager] en klikt u op **[!UICONTROL Server Directories]** > **[!UICONTROL Add]** > **[!UICONTROL Directory]**.

   Typ de URI van de map in het veld URI en klik op **[!UICONTROL OK]**.

   >[!NOTE]
   >
   >U kunt meerdere directory&#39;s toewijzen in het veld URI. Als u bijvoorbeeld  [!DNL Profiles\Marketing\] typt, bevat de beheerder van de serverbestanden de submap Marketing, maar geen andere submap in de map Profiles.

1. Klik met de rechtermuisknop op de bovenrand van [!DNL Server Files Manager] en klik op **[!UICONTROL Save]**.
1. Als u een nieuwe manager wilt maken, wijzigt u de bestandsnaam in het veld [!DNL File Name] en klikt u op **[!UICONTROL Save]**. Als u de bestaande manager wilt overschrijven, klikt u op **[!UICONTROL Save]**.
1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor het bestand [!DNL .vw] in de kolom [!DNL User].

   Klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***.
