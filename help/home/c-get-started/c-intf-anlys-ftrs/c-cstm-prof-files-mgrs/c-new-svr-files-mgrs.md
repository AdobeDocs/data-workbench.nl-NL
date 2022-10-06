---
description: Serverbeheer geeft alle mappen in de installatiemap van de Data Workbench-server weer, inclusief configuratie- en opzoekbestanden.
title: Serverbestandsbeheer maken
uuid: 9fb2163d-3756-40d2-9817-4a89bd8a38c9
exl-id: 9e0c8144-0f52-4e46-85d8-c2dcd60ddcb8
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Serverbestandsbeheer maken{#create-a-server-files-manager}

{{eol}}

Serverbeheer geeft alle mappen in de installatiemap van de Data Workbench-server weer, inclusief configuratie- en opzoekbestanden.

U wilt mogelijk een gedeelte van het dialoogvenster [!DNL Server Files Manager] zonder dat u door de volledige mapstructuur hoeft te navigeren of slechts enkele submappen hoeft weer te geven om aan een bepaalde behoefte te voldoen. U kunt bijvoorbeeld een aparte [!DNL Server Files Manager] die alleen de submappen Toegangsbeheer en Gebruikers weergeeft, zodat u uw gebruikers en hun toegang kunt beheren.

Elke manager die u creeert moet een [!DNL .vw] bestand. U kunt de [!DNL Server Files.vw] bestand als een sjabloon.

Voor meer informatie over de [!DNL Server Files Manager], zie [Serverbestandsbeheer](../../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4).

**Serverbestandsbeheer maken**

1. In de [!DNL Profile Manager]klikt u op de knop **[!UICONTROL Menu]** en vervolgens de **[!UICONTROL Admin]** directory. De [!DNL Server Files.vw] bestand bevindt zich hier.
1. In de *profielnaam* kolom, klikt u met de rechtermuisknop op het vinkje voor de [!DNL Server Files.vw] bestand en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje voor het bestand in het dialoogvenster [!DNL User] kolom.
1. Klik met de rechtermuisknop op het vinkje voor het dialoogvenster [!DNL Server Files.vw] in het [!DNL User] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De [!DNL Server Files.vw] wordt geopend.
1. Als u een map wilt verwijderen, klikt u met de rechtermuisknop op de bovenrand van het dialoogvenster [!DNL Server Files Manager] en klik op **[!UICONTROL Server Directories]** > **[!UICONTROL Remove]** > *&lt;**[!UICONTROL directory name]**>*.
1. Als u een map wilt toevoegen, klikt u met de rechtermuisknop op de bovenrand van het dialoogvenster [!DNL Server Files Manager], klikt u op **[!UICONTROL Server Directories]** > **[!UICONTROL Add]** > **[!UICONTROL Directory]**.

   Typ de URI van de map in het veld URI en klik op **[!UICONTROL OK]**.

   >[!NOTE]
   >
   >U kunt meerdere directory&#39;s toewijzen in het veld URI. Als u bijvoorbeeld [!DNL Profiles\Marketing\]bevat het serverbestandsbeheer de submap Marketing, maar geen andere submap in de map Profielen.

1. Klik met de rechtermuisknop op de bovenrand van het dialoogvenster [!DNL Server Files Manager] en klik op **[!UICONTROL Save]**.
1. Als u een nieuwe manager wilt maken, wijzigt u de bestandsnaam in het dialoogvenster [!DNL File Name] veld, klik vervolgens op **[!UICONTROL Save]**. Als u de bestaande manager wilt overschrijven, klikt u op **[!UICONTROL Save]**.
1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor het [!DNL .vw] in het [!DNL User] kolom.

   Klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
