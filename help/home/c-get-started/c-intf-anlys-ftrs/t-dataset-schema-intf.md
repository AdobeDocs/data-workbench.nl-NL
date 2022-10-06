---
description: Stappen om de standaardvisualisatie te wijzigen.
title: Vorm de Interface van het Schema van de Dataset
uuid: 953909e8-3382-43cf-98c0-d4785c6d1dda
exl-id: 0227663f-4789-4780-b753-d0deb35f6144
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Vorm de Interface van het Schema van de Dataset{#configure-the-dataset-schema-interface}

{{eol}}

Stappen om de standaardvisualisatie te wijzigen.

U kunt bepalen welk type visualisatie wordt weergegeven wanneer u op een dimensienaam in een [!DNL Dataset Schema Interface] door bestanden toe te voegen aan de map Profielen\*profielnaam*\Context\Dimension Legend van de installatiemap van de Data Workbench-server. De [!DNL Default.1d] Het bestand in deze map bepaalt het standaardvisualisatietype voor alle afmetingen. Door een *dimensienaam*.1d-bestand (zoals [!DNL Hour.1d]) aan deze map, kunt u de standaardvisualisatie voor die bepaalde dimensie bepalen.

Meer informatie over [!DNL Dataset Schema Interfaces], zie [De interface van het Dataset-schema](../../../home/c-get-started/c-admin-intrf/c-dtst-sch-intrf.md#concept-e147b3a5b542453ca2b121e1c85bb175).

**De standaardvisualisatie wijzigen**

1. Maak in elke werkruimte een visualisatie met de gegevens die u wilt weergeven in de nieuwe standaardvisualisatie.

   Als u bijvoorbeeld wilt dat de afmetingen in een staafgrafiek worden weergegeven, maakt u een staafgrafiek die de gewenste metrisch en afmeting weergeeft.

1. Klik met de rechtermuisknop op de bovenrand van het bijschriftvenster en klik op **[!UICONTROL Save]**.
1. In de [!DNL Save] venster, klikt u op ![](assets/btn_folder_up.png), dubbelklikken **[!UICONTROL Context]** en dubbelklik vervolgens **[!UICONTROL Dimension Legend]**.
1. In de [!DNL File Name] veld, typt u de naam van de dimensie.

   De naam van de [!DNL .1d] bestand moet exact overeenkomen met de naam van de dimensie. Bijvoorbeeld, [!DNL Hour.1d].

1. Wijzig de bestandsextensie in &quot;1d&quot; en klik op **[!UICONTROL Save]**.

   Het bestand wordt opgeslagen in de map User\*working profile name*\Context\Dimension Legend.

   De volgende keer dat u op die dimensie klikt in een [!DNL Dataset Schema Interface], wordt de door u opgegeven visualisatie weergegeven.

1. (Optioneel) Deze wijziging beschikbaar stellen voor alle gebruikers van het werkprofiel:

   1. In de [!DNL Profile Manager], klikt u op **[!UICONTROL Context]** en klik vervolgens op **[!UICONTROL Dimension Legend]**.

   1. Klik met de rechtermuisknop op het vinkje naast de bestandsnaam van het nieuwe bijschrift in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
