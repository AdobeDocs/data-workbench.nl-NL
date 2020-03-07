---
description: Stappen om de standaardvisualisatie te veranderen.
solution: Analytics
title: Vorm de Interface van het Schema van de Dataset
topic: Data workbench
uuid: 953909e8-3382-43cf-98c0-d4785c6d1dda
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# Vorm de Interface van het Schema van de Dataset{#configure-the-dataset-schema-interface}

Stappen om de standaardvisualisatie te veranderen.

U kunt controleren welk type van visualisatievertoningen wanneer u een afmetingsnaam in a klikt [!DNL Dataset Schema Interface] door dossiers aan de Profielen toe te voegen \*profielnaam*\Context\Dimension Legend folder of the Data Workbench server installation folder. Het [!DNL Default.1d] dossier in deze omslag controleert het standaard visualisatietype voor alle afmetingen. Door een *afmetingsnaam*.1d- dossier (zoals [!DNL Hour.1d]) aan deze omslag toe te voegen, kunt u de standaardvisualisatie voor die bepaalde afmeting controleren.

Voor meer informatie over [!DNL Dataset Schema Interfaces], zie [de Interface](../../../home/c-get-started/c-admin-intrf/c-dtst-sch-intrf.md#concept-e147b3a5b542453ca2b121e1c85bb175)van het Schema van de Dataset.

**Om de standaardvisualisatie te veranderen**

1. In om het even welke werkruimte, creeer een visualisatie die de gegevens bevat die u in de nieuwe standaardvisualisatie wilt verschijnen.

   Bijvoorbeeld, als u de afmeting in een bargrafiek wilt tonen, creeer een visualisatie die van de bargrafiek de gewenste metrisch en afmeting toont.

1. Klik de hoogste grens van het callout venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. Klik in het [!DNL Save] venster op ![](assets/btn_folder_up.png), dubbelklik **[!UICONTROL Context]** en dubbelklik op **[!UICONTROL Dimension Legend]**.
1. Typ in het [!DNL File Name] veld de naam van de afmeting.

   De naam van het [!DNL .1d] dossier moet de naam van de afmeting precies aanpassen. Bijvoorbeeld, [!DNL Hour.1d].

1. Verander de dossieruitbreiding in &quot;1d&quot;en klik **[!UICONTROL Save]**.

   Het bestand wordt opgeslagen in de gebruikersnaam\*werkprofielnaam*\Context\Dimension Legend folder.

   De volgende tijd dat u die afmeting van in [!DNL Dataset Schema Interface]een klikt, de visualisatie die u vertoningen specificeerde.

1. (Facultatief) om deze verandering aan alle gebruikers van het werkprofiel beschikbaar te stellen:

   1. In [!DNL Profile Manager], klik **[!UICONTROL Context]**, dan klik **[!UICONTROL Dimension Legend]**.

   1. Klik met de rechtermuisknop op het vinkje naast de bestandsnaam van de nieuwe callout in de [!DNL User] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

