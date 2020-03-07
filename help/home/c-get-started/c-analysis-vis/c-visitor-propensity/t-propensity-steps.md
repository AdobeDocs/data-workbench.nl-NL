---
description: Volg deze stappen om de Propensity Scoring visualisatie te gebruiken.
solution: Analytics
title: Propensiteitscores instellen
topic: Data workbench
uuid: afc9aada-3bf9-4ce6-8c43-a955771065b4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Propensiteitscores instellen{#setting-up-propensity-scoring}

Volg deze stappen om de Propensity Scoring visualisatie te gebruiken.

1. Open een nieuwe werkruimte en klik **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Predictive Analytics]** > **[!UICONTROL Scoring]** > **[!UICONTROL Propensity Score]**.

   ![](assets/propensity_visualization.png)

1. Plaats de **[!UICONTROL Target]** (afhankelijke variabele).

   Plaats de afhankelijke variabele door te selecteren:

* **Afmetingen**: Klik in de werkruimte met de rechtermuisknop aan en selecteer **[!UICONTROL Table]**. Dan selecteer een elementen van de Dimensie als uw afhankelijke variabele.

   OF

* **[!UICONTROL Filter Editor]**. Klik **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Filter Editor]** om de visualisatie van de Redacteur van de Filter te openen.

   ![](assets/propensity_visualization_filter_editor.png)

   Na het selecteren van een element of een Filter van de Dimensie als afhankelijke variabele, klik **[!UICONTROL Set Target]**, ga een naam in om de afhankelijke variabele te beschrijven. Dan klik **[!UICONTROL OK]** (en zorg ervoor de filterdoos) wordt benadrukt om het Doel te plaatsen.

   ![](assets/propensity_visualization_setTarget.png)

   De naam u het doel geeft is de afhankelijke variabele die in de linkerruit zal verschijnen.
1. Voeg onafhankelijke variabelen toe.

   Voeg de onafhankelijke variabelen toe gebruikend Metriek of de Elementen van de Dimensie.

   ![](assets/propensity_visualization_metrics.png)

* **Metriek**. Van de Hoogte die toolbar rangschikt, selecteer metrisch van het **[!UICONTROL Metrics]** menu.

* **Afmetingen**: Klik in de werkruimte met de rechtermuisknop aan en selecteer **[!UICONTROL Table]**. Selecteer één of meerdere elementen van de Afmeting en sleep aan de linkerkolom onder **[!UICONTROL Independent Variables]** of aan de **[!UICONTROL Element]** doos gebruikend de `<Ctrl>` + `<Alt>` sleutels.

1. Reeks **[!UICONTROL Training Filter]**. U kunt de reeks bezoekers bepalen die u wilt scoren door te klikken **[!UICONTROL Options]** > **[!UICONTROL Set Training Filter]** van de het Scoreren van de Dichtheid toolbar. Dit zal een ondergroep van gegevens verstrekken die gebruikend slechts de bezoekers worden gebouwd die u wilt scoren. Bijvoorbeeld, die in de afgelopen maand bezocht, bezoekers die in Australië verblijven, of bezoekers die specifieke producten bekeken.

   De standaardfilter is **[!UICONTROL Train on Everyone]**, maar u kunt het veranderen door **[!UICONTROL Dimension Elements]** in een lijst te activeren of een filter te bouwen gebruikend **[!UICONTROL Filter Editor]**.

   Na het selecteren van een element van de Dimensie of het bouwen van een filter en terwijl geactiveerd, klik **Opties** > de **Vastgestelde Filter** van de Opleiding, ga een naam in om de filter te beschrijven, en klik dan **[!UICONTROL OK]**.
1. Zodra u al uw input hebt geïdentificeerd, druk op **[!UICONTROL Go]**.

   ![](assets/propensity_visualization_GO.png)

   Het het noteren proces zal beginnen door de gegevens veelvoudige tijden over te gaan. Het zal dan de resultaten als bargrafieken over een percentagelijn tonen.
1. Sparen de Score van de Propensiteit.

   Beginnend met 6.1, hebt u nu een optie wanneer het gebruiken van sparen de Score van de Volheid:

* Afmetingen
* Afmetingen en metrisch

   U kunt omhoog met twee bewaarde dossiers, zowel een afmeting als bepaald metrisch beëindigen.

   >[!NOTE]
   >
   >Als u de Score van de Volheid voor verwerking voorlegt zult u een slechts afmeting krijgen.

   De afgeleide metrisch is de bijbehorende gemiddelde metrische score.
1. Controleer de nauwkeurigheid.

   Het systeem zal een het noteren model tonen **[!UICONTROL Model Complete]** en produceren wanneer het proces volledig is.

   Als u met de rechtermuisknop op klikt, **[!UICONTROL Model Complete]** wordt de nauwkeurigheid van het scoremodel, zoals gedefinieerd door het systeem, vastgesteld. De waarden die zich van 0 percenten aan 100 percenten uitstrekken zullen de waarschijnlijkheid van de bezoekers identificeren die de **[!UICONTROL Target]** variabele aanpassen.

   De fusiematrix geeft vier tellingen door de combinatie van Actual Positive (AP), Actual Negative (AN), Predicted Positive (PP), en Voorspeld Negatief (PN). Deze aantallen worden verkregen door het resulterende scoremodel toe te passen op de 20% ingehouden testgegevens waarvan wij het ware antwoord kennen. Als de score groter is dan 50%, wordt het voorspeld als positief geval (aanpassend de bepaalde gebeurtenis).

   ![](assets/propensity_lift_gain_1.png)

<table id="table_154BDD6D294C4ED1B8C15EC33B74B199"> 
 <tbody> 
  <tr> 
   <td colname="col1"><b> Nauwkeurigheid</b> </td> 
   <td colname="col2"> Wijst erop hoe nauwkeurig het model door de correcte voorspellingen over alle voorspellingen te identificeren is. <p>(TP + TN)/(TP + FP + TN + FN) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b> terugroepen</b> </td> 
   <td colname="col2"> Identificeert de capaciteit om het het noteren model opnieuw te identificeren. <p><b>TP / (TP + FN)</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b> Nauwkeurigheid</b> </td> 
   <td colname="col2">Identificeert het niveau van discrepantie. <p>TP / (TP + FP) </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Open een Grafiek van de [Lift of van de Aanwinst](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-gain-lift-chart.md#concept-0d049f6baf534f7fb97f271843ba6c4a), of de [ModelKijker](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-model-viewer.md#concept-9f2593a8218140b7bd132a4c74e159f9).

   Klik met de rechtermuisknop op het **model Volledige** visualisatie en selecteer **[!UICONTROL Lift Chart]**, **[!UICONTROL Gain Chart]** of **[!UICONTROL Model Viewer.]**
