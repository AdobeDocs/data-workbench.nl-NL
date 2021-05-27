---
description: Deze stappen zijn alleen van toepassing op het maken van submenu's en menu-items voor het menu Venster Werkruimte.
title: Een werkruimtemenu en menu-item maken
uuid: 9565fe7a-fa4c-42b6-9aa5-b652a2d62796
exl-id: 26f2b85c-ab23-41a4-bf4b-9e507952fede
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 1%

---

# Een werkruimtemenu en menuopdracht maken{#create-a-workspace-menu-and-menu-item}

Deze stappen zijn alleen van toepassing op het maken van submenu&#39;s en menu-items voor het menu Venster Werkruimte.

U kunt de metrische menu&#39;s en de metrische menu&#39;s aanpassen door nieuwe omslagen en nieuwe afgeleide metriek en dimensies te creëren. Voor meer informatie, zie [Het creëren en het uitgeven Afgeleide Metriek](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#concept-e41723b342a849309874b26232224a40) en [het Creëren en het uitgeven Afgeleide Dimension](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-dvrd-dim.md#concept-ece3c3ea8cdf4fc796680173993bff93).

**Een nieuw menu van het werkruimtevenster maken**

1. Klik in [!DNL Profile Manager] op de map **[!UICONTROL Menu]** om de inhoud ervan weer te geven.
1. Klik in de kolom [!DNL User] voor de map Menu op **[!UICONTROL Create]** > **[!UICONTROL Folder]**. Een map met de naam Nieuwe map wordt in de kolom [!DNL File] voor [!DNL Menu] weergegeven.

   >[!NOTE]
   >
   >U kunt ook een nieuwe map maken voor elke submap in de map Menu.

1. Wijzig de naam van de nieuwe map door met de rechtermuisknop in de kolom [!DNL User] voor de map te klikken en de nieuwe naam in de parameter Dir te typen.
1. Voeg de gewenste bestanden toe aan de nieuwe map.
1. (Optioneel) Klik in de kolom [!DNL User] voor de nieuwe map op **[!UICONTROL Create]** > **[!UICONTROL order.txt]**.

   Er wordt een [!DNL order.txt]-bestand weergegeven in de kolom [!DNL File] voor de nieuwe map en er wordt een vinkje voor het nieuwe bestand weergegeven in de kolom [!DNL User].

1. (Optioneel) Bewerk het [!DNL order.txt]-bestand naar wens. Zie [Menu&#39;s aanpassen met Order.txt-bestanden](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).
1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het witte vinkje voor de map in de kolom [!DNL User] en klikt u op **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL working profile name]**>*.

**Een nieuw menu-item toevoegen aan een bestaand menu**

1. Voer een van de volgende stappen uit:

   * Maak een nieuw item (visualisatie, annotatie, enzovoort) dat u aan een menu wilt toevoegen:

      1. Open een werkruimte in Data Workbench en maak het gewenste item.
      1. Sla het item op in de volgende map:

         *Installatiemap* van werkbank \User\*werkprofielnaam*\Work

      1. Klik in [!DNL Profile Manager] op de map **[!UICONTROL Work]** om de inhoud ervan weer te geven.
      1. Klik in de kolom [!DNL User] met de rechtermuisknop op het vinkje voor het gewenste bestand en klik op **[!UICONTROL Copy]**.
      1. Klik in de kolom [!DNL User] voor de gewenste map op **[!UICONTROL Paste]**.

         Een kopie van het bestand wordt weergegeven in de kolom [!DNL File] voor de nieuwe map en een vinkje voor het nieuwe bestand wordt weergegeven in de kolom [!DNL User].
   * Kopieer en plak een bestaand item van het ene menu (map) naar het andere:

      1. Klik in [!DNL Profile Manager] op de map **[!UICONTROL Menu]** om de inhoud ervan weer te geven.
      1. Klik in de kolom *werkprofielnaam* met de rechtermuisknop op het vinkje voor het gewenste bestand en klik op **[!UICONTROL Make Local]**.
      1. Klik met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en klik op **[!UICONTROL Copy]**.
      1. Klik in de kolom [!DNL User] voor de gewenste map op **[!UICONTROL Paste]**. Een kopie van het bestand wordt weergegeven in de kolom [!DNL File] voor de nieuwe map en een vinkje voor het nieuwe bestand wordt weergegeven in de kolom [!DNL User].


1. (Optioneel) Bewerk het [!DNL order.txt]-bestand naar wens. Zie [Menu&#39;s aanpassen met Order.txt-bestanden](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).
1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het witte vinkje voor elk bestand in de kolom [!DNL User] en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
1. (Optioneel) Als u wilt voorkomen dat een menu-item in meerdere menu&#39;s wordt weergegeven, verwijdert u het corresponderende bestand uit de oorspronkelijke map door met de rechtermuisknop op het vinkje voor het bestand te klikken in de kolom *werkprofielnaam* en op **[!UICONTROL Remove]** > **[!UICONTROL Yes]** te klikken.

   Herhaal deze stap voor het vinkje van het bestand in de kolom [!DNL User].
