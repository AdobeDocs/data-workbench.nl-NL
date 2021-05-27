---
description: Voer de volgende stappen uit om de visualisatie voor waardenscores te gebruiken.
title: Correctie van volheid instellen
uuid: afc9aada-3bf9-4ce6-8c43-a955771065b4
exl-id: e16a7062-636e-44a9-a07d-343d48bf1b4c
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Propensiteitscores instellen{#setting-up-propensity-scoring}

Voer de volgende stappen uit om de visualisatie voor waardenscores te gebruiken.

1. Open een nieuwe werkruimte en klik **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Predictive Analytics]** > **[!UICONTROL Scoring]** > **[!UICONTROL Propensity Score]**.

   ![](assets/propensity_visualization.png)

1. Stel de **[!UICONTROL Target]** (de afhankelijke variabele) in.

   Stel de afhankelijke variabele in door te selecteren:

* **Dimension-elementen**: Klik met de rechtermuisknop in de werkruimte en selecteer  **[!UICONTROL Table]**. Selecteer vervolgens een Dimension-element als afhankelijke variabele.

   OF

* **[!UICONTROL Filter Editor]**. Klik **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Filter Editor]** om de visualisatie van de Redacteur van de Filter te openen.

   ![](assets/propensity_visualization_filter_editor.png)

   Nadat u een Dimension-element of -filter als afhankelijke variabele hebt geselecteerd, klikt u op **[!UICONTROL Set Target]** en voert u een naam in om de afhankelijke variabele te beschrijven. Klik vervolgens op **[!UICONTROL OK]** (en controleer of het filtervak is gemarkeerd) om het doel in te stellen.

   ![](assets/propensity_visualization_setTarget.png)

   De naam u het doel geeft is de afhankelijke variabele die in de linkerruit zal verschijnen.
1. Onafhankelijke variabelen toevoegen.

   Voeg de onafhankelijke variabelen toe met Metriek of Dimension Elements.

   ![](assets/propensity_visualization_metrics.png)

* **Cijfers**. Selecteer een metrische waarde in het menu **[!UICONTROL Metrics]** op de werkbalk Volheid scoren.

* **Dimension-elementen**: Klik met de rechtermuisknop in de werkruimte en selecteer  **[!UICONTROL Table]**. Selecteer een of meer Dimension-elementen en sleep deze naar de linkerkolom onder **[!UICONTROL Independent Variables]** of naar het vak **[!UICONTROL Element]** met de toetsen `<Ctrl>` + `<Alt>`.

1. **[!UICONTROL Training Filter]** instellen. U kunt de set bezoekers definiëren die u wilt scoren door op **[!UICONTROL Options]** > **[!UICONTROL Set Training Filter]** te klikken op de werkbalk voor het scoren van eigenschappen. Dit zal een ondergroep gegevens verstrekken die slechts de bezoekers worden gebouwd die u wilt scoren. Bijvoorbeeld: bezoekers die de afgelopen maand een bezoek hebben gebracht, bezoekers die in Australië wonen of bezoekers die bepaalde producten hebben bekeken.

   Het standaardfilter is **[!UICONTROL Train on Everyone]**, maar u kunt het veranderen door **[!UICONTROL Dimension Elements]** in een lijst te activeren of een filter te bouwen gebruikend **[!UICONTROL Filter Editor]**.

   Nadat u een Dimension-element hebt geselecteerd of een filter hebt gemaakt, klikt u op **Opties** > **Trainingsfilter instellen**, voert u een naam in om het filter te beschrijven en klikt u op **[!UICONTROL OK]**.
1. Wanneer u al uw invoer hebt geïdentificeerd, drukt u op **[!UICONTROL Go]**.

   ![](assets/propensity_visualization_GO.png)

   Het scoringsproces begint door de gegevens meerdere keren door te geven. Vervolgens worden de resultaten als staafdiagrammen over een percentastregel weergegeven.
1. Score voor volheid opslaan.

   Vanaf 6.1 hebt u nu een optie wanneer u de Score voor volheid opslaan gebruikt:

* Dimension
* Dimension en metrisch

   U kunt uiteindelijk twee opgeslagen bestanden gebruiken, zowel een dimensie als een gedefinieerde metrische waarde.

   >[!NOTE]
   >
   >Als u de Score van de Volheid voor verwerking indient, zult u een dimensie slechts krijgen.

   De afgeleide metrische waarde is de bijbehorende gemiddelde metrische score.
1. Controleren op nauwkeurigheid.

   Het systeem geeft **[!UICONTROL Model Complete]** weer en genereert een scoremodel wanneer het proces is voltooid.

   Als u met de rechtermuisknop op **[!UICONTROL Model Complete]** klikt, wordt de nauwkeurigheid van het scoremodel, zoals gedefinieerd door het systeem, vastgesteld. Waarden tussen 0 en 100 procent geven de waarschijnlijkheid aan dat bezoekers de variabele **[!UICONTROL Target]** gebruiken.

   De fusiematrix geeft vier tellingen door de combinatie van Actual Positive (AP), Actual Negative (AN), Predicted Positive (PP), en Predicted Negative (PN). Deze aantallen worden verkregen door het resulterende scoremodel toe te passen op de 20% ingehouden testgegevens waarvan we het ware antwoord kennen. Als de score groter is dan 50%, wordt deze voorspeld als een positief geval (overeenkomend met de gedefinieerde gebeurtenis).

   ![](assets/propensity_lift_gain_1.png)

<table id="table_154BDD6D294C4ED1B8C15EC33B74B199"> 
 <tbody> 
  <tr> 
   <td colname="col1"><b> Nauwkeurigheid</b> </td> 
   <td colname="col2"> Geeft aan hoe nauwkeurig het model is door de juiste voorspellingen voor alle voorspellingen te identificeren. <p>(TP + TN)/(TP + FP + TN + FN) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b> Herstellen</b> </td> 
   <td colname="col2"> Hiermee wordt aangegeven of het scoremodel opnieuw kan worden geïdentificeerd. <p><b>TP / (TP + FN)</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b> Precisie</b> </td> 
   <td colname="col2">Hiermee wordt het discrepantieniveau aangegeven. <p>TP / (TP + FP) </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Open een [Lift- of versterkingsdiagram](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-gain-lift-chart.md#concept-0d049f6baf534f7fb97f271843ba6c4a) of de [Modelviewer](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-model-viewer.md#concept-9f2593a8218140b7bd132a4c74e159f9).

   Klik met de rechtermuisknop op **Model Volledig** en selecteer **[!UICONTROL Lift Chart]**, **[!UICONTROL Gain Chart]** of **[!UICONTROL Model Viewer.]**
