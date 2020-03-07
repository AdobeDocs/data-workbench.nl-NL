---
description: Opstelling een Boom van de Beslissing door een positief geval te identificeren en metrische en afmetrische input toe te voegen om de gegevens te evalueren en de besluitboom te onderzoeken.
title: Een beslissingshiërarchie opbouwen
uuid: 5790d322-5460-444d-95d8-a06696f9a55f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Een beslissingshiërarchie opbouwen{#building-a-decision-tree}

Opstelling een Boom van de Beslissing door een positief geval te identificeren en metrische en afmetrische input toe te voegen om de gegevens te evalueren en de besluitboom te onderzoeken.

Volg deze stappen om een beslissingsboom te bouwen.

1. Open een nieuwe werkruimte.

   Na het openen van een nieuwe werkruimte, zou u kunnen moeten klikken **toevoegt** > **tijdelijk opent**.

1. Om de Bouwer van de Boom van de Beslissing te openen, klik **[!UICONTROL Visualization]** > **Predictive Analytics** > **Classificatie** met de rechtermuisknop aan > de Bouwer van de **Beslissingsboom**.

1. Plaats een **Positieve Geval**.

   U kunt een positief geval voor een besluitboom bepalen door afmetingen in een Vinder of afmetingselementen in een lijst te selecteren, of door een filter in de Filter van het Ontwerp te ontwerpen. In feite, kan het positieve geval een combinatie veelvoudige selecties in de werkruimte met inbegrip van filters, afmetingen, elementen, en alle types van de visualisatiewaarden van de Werkbank van Gegevens zijn.

   * **Ontwerp en pas een Filter** toe als positief geval. Klik in de werkruimte met de rechtermuisknop aan en selecteer **[!UICONTROL Tools]** > **[!UICONTROL Filter Editor]** om een filter te ontwerpen en toe te passen.

   * Voeg **Afmetingen** toe als positief geval. In de werkruimte, klik en selecteer **Hulpmiddelen** met de rechtermuisknop aan > **Vinders** (of selecteer **[!UICONTROL Add]** > **[!UICONTROL Finders]** in de linkerruit). Typ een afmetingsnaam op het gebied van het **Onderzoek** en selecteer dan een afmeting.

   * Voeg **Metriek** als positief geval toe. Klik en selecteer **Hulpmiddelen** > **Vinders** met de rechtermuisknop aan of selecteer **[!UICONTROL Add]** > **[!UICONTROL Finders]** in de linkerruit om een lijst van Metriek te openen. Selecteer metrisch als uw positief geval.

   * Voeg de Elementen **van de** Dimensie als positief geval toe. Klik in de werkruimte met de rechtermuisknop aan en selecteer **[!UICONTROL Table]** aan open afmetingselementen, dan selecteer uit de afmetingselementen om uw positief geval te plaatsen.

1. Klik op **[!UICONTROL Options]** > **[!UICONTROL Set Positive Case]**.

   Dit plaatst het positieve geval en laat u het noemen. De naam zal onder de **[!UICONTROL Positive Case]** rubriek in de werkruimte verschijnen.

   >[!NOTE]
   >
   >Wanneer u het positieve geval plaatst gebruikt de Boom van de Beslissing de huidige werkruimteselectie, die als Bezoekers (of wat top-level teltable wordt bepaald, maar in de meeste gevallen Bezoekers) kan worden bepaald die de huidige selectie binnen de werkruimte aanpassen. Deze worden gecombineerd als één filter voor één enkel positief geval (niet meerdere positieve gevallen).

   Het klikken **[!UICONTROL Set Positive Case]** wanneer er geen selectie is zal de positieve zaak ontkrachten.

1. (facultatief) selecteer **[!UICONTROL Set Population Filters]** om de te classificeren bezoekerspopulatie te bepalen.

   Als geen populatiefilter wordt toegepast, dan wordt de opleidingsreeks getrokken van alle bezoekers (het gebrek is &quot;iedereen&quot;).

   >[!NOTE]
   >
   >Klik **[!UICONTROL Show Complex Filter Description]** om de het filtreren manuscripten voor de Positieve Geval en de Filter van de Bevolking te bekijken.

1. Voeg **Metriek**, **Dimensies**, en de Elementen **van de** Dimensie als input toe.

   U kunt input selecteren door van de panelen van de Vinder of van lijsten voor individuele afmetingselementen te slepen en te laten vallen. U kunt van het **[!UICONTROL Metrics]** menu in de toolbar ook selecteren.

   * Voeg **Metriek** als input toe.

      Selecteer Metriek van de toolbar. Druk **CTRL** + **Alt** om één of meerdere metriek aan de Bouwer van de Boom van de Beslissing te slepen.

      Metrisch zal in de van de **Input (Metriek) lijst** als input met unieke kleur-codering verschijnen.

      ![](assets/decision_tree_add_Metrics_inputs.png)

   * Voeg **Afmetingen** als input toe.

      In de werkruimte, klik en selecteer **Hulpmiddelen** met de rechtermuisknop aan > **Vinder** en typ de afmetingsnaam op het gebied van het **Onderzoek** . De pers **CTRL** + **Alt**, selecteert een afmeting, en sleept de afmeting aan de Bouwer van de Boom van het Besluit.

      De dimensie zal in de **Input (Afmetingen)** lijst met een unieke kleur-codering verschijnen.

   * Voeg de Elementen **van de** Dimensie als input toe.

      In de werkruimte, klik en selecteer een lijst van de Dimensie met de rechtermuisknop aan. Selecteer de Elementen van de Dimensie, druk **CTRL** + **Alt**, en sleep de geselecteerde elementen aan de Bouwer van de Boom van het Besluit.

      De afmetingselementen zullen in de lijst van de **Input (Elementen)** met een unieke kleur-codering verschijnen.
   >[!IMPORTANT]
   >
   >U kunt maximaal veertien te evalueren ingangen selecteren. Een foutenmelding zal verschijnen als teveel input wordt toegevoegd.

1. Selecteer **[!UICONTROL Go]** op de werkbalk.

   De besluitboom zal gebaseerd op de geselecteerde afmetingen en de metriek bouwen. De eenvoudige metriek zoals de Toevoegingen van het Kart zullen snel bouwen, terwijl de complexe afmeting zoals de Duur van het Bezoek met veelvoudige gegevenspunten langzamer met een percentage van de getoonde voltooiing zal bouwen aangezien het omzet. De boomkaart zal dan voor gebruikersinteractie snoeien en openen. De afmeting en de metrische input zullen kleur-gecodeerd verenigbaar met de knoopnamen zijn.

   ![](assets/decision_tree_builder.png)

   De bladknoopvertoningen als groen (waar) of rood (vals) als de boom is gesnoeid en als er een voorspelling van **Waar** of **Vals** na de gesnoeide takken is.

   >[!NOTE]
   >
   >De trainingssteekproef wordt getrokken uit de dataset voor de te gebruiken boombouwer. De Werkbank van gegevens gebruikt 80 percent van de steekproef om de boom en de resterende 20 percenten te bouwen om de nauwkeurigheid van het boommodel te beoordelen.

1. Controleer de nauwkeurigheid met behulp van de **[!UICONTROL Confusion Matrix]**.

   Klik **[!UICONTROL Options]** > **[!UICONTROL Confusion Matrix]** om de waarden van de Nauwkeurigheid, het Herinneren, de Nauwkeurigheid en F-Score te bekijken. Hoe dichter bij 100 procent, hoe beter de score.

   De fusiematrix geeft vier nauwkeurigheidsgetallen van het model met behulp van een combinatie van waarden:

   * Werkelijk positief (AP)
   * Voorspeld positief (PP)
   * Werkelijk negatief (AN)
   * Voorspeld negatief (PN)
   >[!TIP]
   >
   >Deze aantallen worden verkregen door het resulterende het noteren model van de 20 percenten het testen gegevens toe te passen die worden ingehouden en reeds gekend als het ware antwoord. Als de score groter is dan 50 percenten, wordt het voorspeld als positief geval (dat de bepaalde filter aanpast). Dan, Nauwkeurigheid = (TP + TN)/(TP + FP + TN + FN), Rappel = TP / (TP + FN), en Precision = TP / (TP + FP).

1. **Onderzoek de beslissingsboom**.

   Na het produceren van een besluitboom, kunt u de weg van de voorspelling bekijken en alle bezoekers identificeren die aan de bepaalde criteria voldoen. De boom identificeert de inputspleet voor elke tak die op zijn positie en kleur-codering wordt gebaseerd. Bijvoorbeeld, als u de Refering knoop van het Domein selecteert, zijn de knopen die tot die verdeling leiden vermeld door kleur-code links van de boom.

   U kunt selecties van de bladknopen maken om takken (regelreeksen) van de besluitboom te selecteren.

   Bij dit voorbeeld: Als de duur van het bezoek minder dan 1 is, er geen campagne bestaat, er bestaan minstens één paginamening, geen e-mailberichten, en er was minstens één bezoek. De projecties op deze criteria en het plaatsen van een orde zijn **94.73** percenten.

   ![](assets/decision_tree_explore.png)

   **Interactie** beslissingshiërarchie: U kunt veelvoudige knopen op de boom selecteren gebruikend de standaard **CTRL-Klik** om toe te voegen, of **verschuiving-Klik** om te schrappen.

   **Kleurgecodeerde knooppunten**: De kleur van de knopen past de kleur van de inputafmetingen en de metriek aan zoals die door de Werkbank van Gegevens wordt toegewezen.

   De heldere groene en rode knopen op het bladniveau van een gesnoeide tak voorspellen de knoop waar of Vals.

   | ![](assets/decision_tree_node_true.png) Heldergroen | Identificeert dat de knoop waar evenaart en dat aan alle voorwaarden wordt voldaan. |
   |---|---|
   | ![](assets/decision_tree_node_false.png) Helder rood | Identificeert dat de knoop vals evenaart en niet aan alle voorwaarden wordt voldaan. |

1. **Sla de beslissingshiërarchie** op.

   U kunt de beslissingshiërarchie in verschillende indelingen opslaan:

   ![](assets/decison_tree_save.png)

   * Predictive Markup Language (**PMML**), een op XML gebaseerd dossierformaat dat door toepassingen wordt gebruikt om besluitvormingsboommodellen te beschrijven en te ruilen.
   * **Tekst** die eenvoudige kolommen en rijen van waar of vals toont, percentages, aantal leden, en inputwaarden.
   * Een **dimensie** met bijkantoren die overeenkomt met voorspelde uitkomstelementen.

