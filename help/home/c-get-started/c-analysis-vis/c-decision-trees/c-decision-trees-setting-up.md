---
description: Opstelling een Boom van de Beslissing door een positief geval te identificeren en metrische en metrische input toe te voegen om de gegevens te evalueren en de beslissingsboom te onderzoeken.
title: Een beslissingsstructuur opbouwen
uuid: 5790d322-5460-444d-95d8-a06696f9a55f
exl-id: 06db9e77-72ea-44c7-8451-d3f195acd196
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# Een beslissingsstructuur opbouwen{#building-a-decision-tree}

{{eol}}

Opstelling een Boom van de Beslissing door een positief geval te identificeren en metrische en metrische input toe te voegen om de gegevens te evalueren en de beslissingsboom te onderzoeken.

Voer de volgende stappen uit om een beslissingsstructuur te maken.

1. Open een nieuwe werkruimte.

   Nadat u een nieuwe werkruimte hebt geopend, moet u mogelijk op **Toevoegen** > **Tijdelijk ontgrendelen**.

1. Klik met de rechtermuisknop om de opbouwfunctie voor de beslissingsstructuur te openen **[!UICONTROL Visualization]** > **Predictieve analyse** > **Classificatie** > **Beslissingsstructuur maken**.

1. Een **Positieve draagtas**.

   U kunt een positief geval voor een beslissingsboom bepalen door afmetingen in een Vinder of afmetingselementen in een lijst te selecteren, of door een filter in de Filter van het Ontwerp te ontwerpen. In feite kan het positieve geval een combinatie van veelvoudige selecties in de werkruimte met inbegrip van filters, afmetingen, elementen, en alle types van Data Workbench visualisatiewaarden zijn.

   * **Een filter ontwerpen en toepassen** als positief geval. Klik met de rechtermuisknop in de werkruimte en selecteer **[!UICONTROL Tools]** > **[!UICONTROL Filter Editor]** om een filter te ontwerpen en toe te passen.

   * Toevoegen **Dimension** als positief geval. Klik in de werkruimte met de rechtermuisknop en selecteer **Gereedschappen** > **Finders** (of selecteer **[!UICONTROL Add]** > **[!UICONTROL Finders]** in het linkerdeelvenster). Typ een naam voor een dimensie in het dialoogvenster **Zoeken** en selecteer vervolgens een dimensie.

   * Toevoegen **Metrisch** als positief geval. Klik met de rechtermuisknop en selecteer **Gereedschappen** > **Finders** of selecteer **[!UICONTROL Add]** > **[!UICONTROL Finders]** in het linkerdeelvenster om een tabel Metriek te openen. Selecteer metrisch als uw positief geval.

   * Toevoegen **Dimension Elements** als positief geval. Klik met de rechtermuisknop in de werkruimte en selecteer **[!UICONTROL Table]** om dimensie-elementen te openen, selecteert u een van de dimensie-elementen om het positieve geval in te stellen.

1. Klik op **[!UICONTROL Options]** > **[!UICONTROL Set Positive Case]**.

   Hiermee stelt u het positieve geval in en kunt u het een naam geven. De naam wordt weergegeven onder de **[!UICONTROL Positive Case]** in de werkruimte.

   >[!NOTE]
   >
   >Wanneer u het positieve geval plaatst gebruikt de Beslissingsboom de huidige werkruimteselectie, die als Bezoekers (of wat top-level teltable wordt bepaald, maar in de meeste gevallen Bezoekers) kan worden bepaald die de huidige selectie binnen de werkruimte aanpassen. Deze worden gecombineerd als één filter voor één positief geval (niet veelvoudige positieve gevallen).

   Klikken **[!UICONTROL Set Positive Case]** als er geen selectie is , zal het positieve geval duidelijk worden .

1. (optioneel) Selecteer **[!UICONTROL Set Population Filters]** de te classificeren bezoekersbevolking te omschrijven.

   Als geen populatiefilter wordt toegepast, dan wordt de trainingsreeks getrokken van alle bezoekers (gebrek is &quot;iedereen&quot;).

   >[!NOTE]
   >
   >Klik op de knop **[!UICONTROL Show Complex Filter Description]** om de het filtreren manuscripten voor de Positieve HoofdHoofdHoofdFilters en de Filter van de Bevolking te bekijken.

1. Toevoegen **Metrisch**, **Dimension**, en **Dimension Elements** als invoer.

   U kunt invoer selecteren door deze te slepen vanuit de deelvensters Finder of vanuit tabellen voor afzonderlijke dimensie-elementen. U kunt ook **[!UICONTROL Metrics]** op de werkbalk.

   * Toevoegen **Metrisch** als invoer.

      Selecteer Metriek op de werkbalk. Druk **Ctrl** + **Alt** om een of meer metriek naar de Beslissingsbouwer te slepen.

      De metrische waarde wordt weergegeven in de **Lijst met invoergegevens (metriek)** als invoer met unieke kleurcodering.

      ![](assets/decision_tree_add_Metrics_inputs.png)

   * Toevoegen **Dimension** als invoer.

      Klik in de werkruimte met de rechtermuisknop en selecteer **Gereedschappen** > **Finder** en typ de naam van de dimensie in het dialoogvenster **Zoeken** veld. Druk **Ctrl** + **Alt**, selecteert u een dimensie en sleept u de dimensie naar de beslissingsboomstructuur Builder.

      De dimensie wordt weergegeven in het dialoogvenster **Invoer (Dimension)** lijst met een unieke kleurcodering.

   * Toevoegen **Dimension Elements** als invoer.

      Klik in de werkruimte met de rechtermuisknop en selecteer een Dimension-tabel. Selecteer Dimension Elements, druk op **Ctrl** + **Alt** en sleep de geselecteerde elementen naar de beslissingsstructuur Builder.

      De dimensie-elementen worden weergegeven in de **Invoer (elementen)** lijst met een unieke kleurcodering.
   >[!IMPORTANT]
   >
   >U kunt maximaal veertien te evalueren invoeren selecteren. Er wordt een foutbericht weergegeven als er te veel invoer wordt toegevoegd.

1. Selecteren **[!UICONTROL Go]** op de werkbalk.

   De beslissingsstructuur wordt gebaseerd op de geselecteerde afmetingen en metriek. Eenvoudige metriek zoals de Toevoegingen van het Kart zal snel bouwen, terwijl de complexe dimensie zoals de Duur van het Bezoek met veelvoudige gegevenspunten langzamer met een percentage van de voltooiing zal worden getoond aangezien het omzet. De boomstructuur wordt vervolgens afgedrukt en geopend voor gebruikersinteractie. De dimensie en metrische input zullen kleur-gecodeerd verenigbaar met de knoopnamen zijn.

   ![](assets/decision_tree_builder.png)

   Het bladknooppunt wordt weergegeven als groen (true) of rood (false) als de structuur is weggehaald en als er een voorspelling is van **Waar** of **Onwaar** na de gesnoeide vertakkingen.

   >[!NOTE]
   >
   >Het trainingsvoorbeeld wordt uit de gegevensset gehaald zodat de boombouwer het kan gebruiken. De Data Workbench gebruikt 80 percenten van het monster om de boom en de resterende 20 percenten te bouwen om de nauwkeurigheid van het boommodel te beoordelen.

1. Nauwkeurigheid controleren met de **[!UICONTROL Confusion Matrix]**.

   Klikken **[!UICONTROL Options]** > **[!UICONTROL Confusion Matrix]** om de waarden Accuracy, Recall, Precision en F-Score weer te geven. Hoe dichter bij 100 procent, hoe beter de score.

   De Verwaringsmatrix geeft vier nauwkeurigheidsgetallen van het model met behulp van een combinatie van waarden:

   * Werkelijk positief (AP)
   * Voorspeld positief (PP)
   * Werkelijk negatief (AN)
   * Voorspeld negatief (PN)

   >[!TIP]
   >
   >Deze aantallen worden verkregen door het resulterende scoremodel toe te passen van de 20 percenten testgegevens ingehouden en reeds gekend als ware antwoord. Als de score groter is dan 50 procent, wordt deze voorspeld als een positief geval (dat overeenkomt met het gedefinieerde filter). Dan, Nauwkeurigheid = (TP + TN)/(TP + FP + TN + FN), Herinnering = TP / (TP + FN), en Precisie = TP / (TP + FP).

1. **De beslissingstructuur verkennen**.

   Na het produceren van een beslissingsboom, kunt u de weg van de voorspelling bekijken en alle bezoekers identificeren die aan de bepaalde criteria voldoen. De structuur geeft de invoersplitsing voor elke vertakking aan op basis van de positie en kleurcodering. Als u bijvoorbeeld het knooppunt Referring Domain selecteert, worden de knooppunten die naar die splitsing leiden, met kleurcode links van de structuur weergegeven.

   U kunt selecties maken van de bladknooppunten om vertakkingen (regelsets) van de beslissingsstructuur te selecteren.

   In dit voorbeeld: Als de duur van het bezoek minder dan 1 is, er geen campagne bestaat, bestaat minstens één paginaweergave, geen e-mailhandtekeningen, en er was minstens één bezoek. De prognoses voor deze criteria en het plaatsen van een bestelling zijn: **94,73** procent.

   ![](assets/decision_tree_explore.png)

   **Interactie beslissingsstructuur**: U kunt meerdere knooppunten in de structuur selecteren met de standaard **Ctrl ingedrukt houden en klikken** om toe te voegen, of **Shift ingedrukt houden en klikken** om te verwijderen.

   **Gekleurde knooppunten**: De kleur van de knooppunten komt overeen met de kleur van de invoerafmetingen en -waarden die door de Data Workbench worden toegewezen.

   Heldere groene en rode knooppunten op bladniveau van een gesnoeide vertakking voorspellen het knooppunt als Waar of Onwaar.

   | ![](assets/decision_tree_node_true.png) Helder groen | Identificeert dat de knoop waar evenaart en dat aan alle voorwaarden wordt voldaan. |
   |---|---|
   | ![](assets/decision_tree_node_false.png) Helder rood | Geeft aan dat het knooppunt gelijk is aan false en dat niet aan alle voorwaarden is voldaan. |

1. **De beslissingsstructuur opslaan**.

   U kunt de beslissingsstructuur in verschillende indelingen opslaan:

   ![](assets/decison_tree_save.png)

   * Predictive Markup Language (**PMML**), een op XML gebaseerde bestandsindeling die door toepassingen wordt gebruikt om besluitvormingsboommodellen te beschrijven en uit te wisselen.
   * **Tekst** het tonen van eenvoudige kolommen en rijen van waar of vals, percentages, aantal leden, en inputwaarden.
   * A **Dimension** met vertakkingen die overeenkomen met elementen van voorspelde resultaten.
