---
description: Stappen om de standaardvisualisatie te wijzigen.
title: Vorm de Interface van het Schema van de Dataset
uuid: 953909e8-3382-43cf-98c0-d4785c6d1dda
exl-id: 0227663f-4789-4780-b753-d0deb35f6144
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Vorm de Interface van het Schema van de Dataset{#configure-the-dataset-schema-interface}

Stappen om de standaardvisualisatie te wijzigen.

U kunt bepalen welk type visualisatie wordt weergegeven wanneer u op een dimensienaam in een [!DNL Dataset Schema Interface] klikt door bestanden toe te voegen aan de profielnaam \*\Context\Dimension Legend folder of the Data Workbench server installation folder. Het [!DNL Default.1d] dossier in deze omslag controleert het standaardvisualisatietype voor alle dimensies. Door een *dimensienaam*.1d- dossier (zoals [!DNL Hour.1d]) aan deze omslag toe te voegen, kunt u de standaardvisualisatie voor die bepaalde afmeting controleren.

Voor meer informatie over [!DNL Dataset Schema Interfaces], zie [De Interface van het Schema van de Dataset](../../../home/c-get-started/c-admin-intrf/c-dtst-sch-intrf.md#concept-e147b3a5b542453ca2b121e1c85bb175).

**De standaardvisualisatie wijzigen**

1. Maak in elke werkruimte een visualisatie met de gegevens die u wilt weergeven in de nieuwe standaardvisualisatie.

   Als u bijvoorbeeld wilt dat de afmetingen in een staafgrafiek worden weergegeven, maakt u een staafgrafiek die de gewenste metrisch en afmeting weergeeft.

1. Klik met de rechtermuisknop op de bovenrand van het bijschriftvenster en klik op **[!UICONTROL Save]**.
1. Klik in het venster [!DNL Save] op ![](assets/btn_folder_up.png), dubbelklik **[!UICONTROL Context]** en dubbelklik vervolgens op **[!UICONTROL Dimension Legend]**.
1. Typ in het veld [!DNL File Name] de naam van de dimensie.

   De naam van het [!DNL .1d] bestand moet exact overeenkomen met de naam van de dimensie. Bijvoorbeeld, [!DNL Hour.1d].

1. Wijzig de bestandsextensie in &quot;1d&quot; en klik op **[!UICONTROL Save]**.

   Het bestand wordt opgeslagen op de gebruikersnaam\*werkprofielnaam*\Context\Dimension Legend folder.

   De volgende keer dat u die afmeting van in [!DNL Dataset Schema Interface] klikt, toont de visualisatie die u specificeerde vertoningen.

1. (Optioneel) Deze wijziging beschikbaar stellen voor alle gebruikers van het werkprofiel:

   1. Klik in [!DNL Profile Manager] op **[!UICONTROL Context]** en vervolgens op **[!UICONTROL Dimension Legend]**.

   1. Klik met de rechtermuisknop op het vinkje naast de bestandsnaam van de nieuwe callout in de kolom [!DNL User] en klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***.
