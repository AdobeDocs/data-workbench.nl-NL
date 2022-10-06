---
description: Deze stappen zijn alleen van toepassing op het maken van submenu's en menu-items voor het menu Venster Werkruimte.
title: Een werkruimtemenu en menu-item maken
uuid: 9565fe7a-fa4c-42b6-9aa5-b652a2d62796
exl-id: 26f2b85c-ab23-41a4-bf4b-9e507952fede
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 1%

---

# Een werkruimtemenu en menu-item maken{#create-a-workspace-menu-and-menu-item}

{{eol}}

Deze stappen zijn alleen van toepassing op het maken van submenu&#39;s en menu-items voor het menu Venster Werkruimte.

U kunt de metrische menu&#39;s en de metrische menu&#39;s aanpassen door nieuwe omslagen en nieuwe afgeleide metriek en dimensies te creëren. Zie voor meer informatie [Afgeleide metriek maken en bewerken](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#concept-e41723b342a849309874b26232224a40) en [Afgeleide Dimension maken en bewerken](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-dvrd-dim.md#concept-ece3c3ea8cdf4fc796680173993bff93).

**Een nieuw menu van het werkruimtevenster maken**

1. In de [!DNL Profile Manager]klikt u op de knop **[!UICONTROL Menu]** om de inhoud ervan weer te geven.
1. In de [!DNL User] kolom voor de map Menu, klikt u op **[!UICONTROL Create]** > **[!UICONTROL Folder]**. Er verschijnt een map met de naam Nieuwe map in het dialoogvenster [!DNL File] kolom voor [!DNL Menu].

   >[!NOTE]
   >
   >U kunt ook een nieuwe map maken voor elke submap in de map Menu.

1. Wijzig de naam van de nieuwe map door met de rechtermuisknop te klikken in het dialoogvenster [!DNL User] kolom voor de map en typ de nieuwe naam in de parameter Dir.
1. Voeg de gewenste bestanden toe aan de nieuwe map.
1. (Optioneel) In het dialoogvenster [!DNL User] voor de nieuwe map klikt u op **[!UICONTROL Create]** > **[!UICONTROL order.txt]**.

   An [!DNL order.txt] wordt weergegeven in het dialoogvenster [!DNL File] wordt een vinkje voor het nieuwe bestand weergegeven in het dialoogvenster [!DNL User] kolom.

1. (Optioneel) Bewerk de [!DNL order.txt] bestand naar wens. Zie [Menu&#39;s aanpassen met Order.txt-bestanden](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).
1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het witte vinkje voor de map in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL working profile name]**>*.

**Een nieuw menu-item toevoegen aan een bestaand menu**

1. Voer een van de volgende stappen uit:

   * Maak een nieuw item (visualisatie, annotatie, enzovoort) dat u aan een menu wilt toevoegen:

      1. Open een werkruimte in Data Workbench en maak het gewenste item.
      1. Sla het item op in de volgende map:

         *Installatiemap gegevenswerkbank*\Gebruiker\*naam werkprofiel*\Work

      1. In de [!DNL Profile Manager]klikt u op de knop **[!UICONTROL Work]** om de inhoud ervan weer te geven.
      1. In de [!DNL User] klikt u met de rechtermuisknop op het vinkje voor het gewenste bestand en klikt u op **[!UICONTROL Copy]**.
      1. In de [!DNL User] kolom voor de gewenste map, klikt u op **[!UICONTROL Paste]**.

         Er wordt een kopie van het bestand weergegeven in het dialoogvenster [!DNL File] wordt een vinkje voor het nieuwe bestand weergegeven in het dialoogvenster [!DNL User] kolom.
   * Kopieer en plak een bestaand item van het ene menu (map) naar het andere:

      1. In de [!DNL Profile Manager]klikt u op de knop **[!UICONTROL Menu]** om de inhoud ervan weer te geven.
      1. In de *naam van werkprofiel* klikt u met de rechtermuisknop op het vinkje voor het gewenste bestand en klikt u op **[!UICONTROL Make Local]**.
      1. Klik met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Copy]**.
      1. In de [!DNL User] kolom voor de gewenste map, klikt u op **[!UICONTROL Paste]**. Er wordt een kopie van het bestand weergegeven in het dialoogvenster [!DNL File] wordt een vinkje voor het nieuwe bestand weergegeven in het dialoogvenster [!DNL User] kolom.


1. (Optioneel) Bewerk de [!DNL order.txt] bestand naar wens. Zie [Menu&#39;s aanpassen met Order.txt-bestanden](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).
1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het witte vinkje voor elk bestand in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
1. (Optioneel) Als u wilt voorkomen dat een menu-item in meerdere menu&#39;s wordt weergegeven, verwijdert u het corresponderende bestand uit de oorspronkelijke map door met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster *naam van werkprofiel* kolom en klikken **[!UICONTROL Remove]** > **[!UICONTROL Yes]**.

   Herhaal deze stap voor het vinkje van het bestand in het dialoogvenster [!DNL User] kolom.
