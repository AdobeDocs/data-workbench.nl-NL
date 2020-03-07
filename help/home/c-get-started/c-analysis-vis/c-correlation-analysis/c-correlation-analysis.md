---
description: Statistische correlaties meten betekenisvolle relaties om kansen te identificeren door middel van geavanceerde datamining.
solution: Analytics
title: Correlatiematrix
topic: Data workbench
uuid: 7f6bdb65-dc31-4e27-9870-4c9402ee6031
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Correlatiematrix{#correlation-matrix}

Statistische correlaties meten betekenisvolle relaties om kansen te identificeren door middel van geavanceerde datamining.

Door gebruik te maken van de correlatiecoëfficiënt [van](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-pearsons.md#concept-5996cb8c89fd4df5b47b7318e7a1d29c)personen, biedt de correlatiematrix u relevante informatie om de volgende stappen in een marketingcampagne beter te kunnen identificeren, om het ontwerp van de site te verbeteren of om een diepgaande analyse van de klant door te zetten voor extra correlatieafhankelijkheden.

## Een correlatiematrix maken {#section-87ed12ccc1af4196a1b6534e621c4cbb}

De Matrijs van de Correlatie vergelijkt metriek over een telbare of niet-telbare dimensie. De matrijs kan dan worden gewijzigd om correlaties binnen de visualisatie te benadrukken door kleur te plukken of het terug te geven als tekstkaart, warmtekaart, of allebei.

1. Open een correlatiematrix.

   Klik met de rechtermuisknop [!DNL Visualization] > [!DNL Predictive Analytics] > [!DNL Correlation Matrix]. De afmetingstabel wordt geopend.

   ![](assets/correlation_matrix_2.png)

   Selecteer een afmeting, zoals [!DNL Time] > [!DNL Day of the Week] van dit menu. De correlatietabel wordt geopend met de dimensie die in de hoek van de matrix wordt geïdentificeerd en de bijbehorende metrisch die in de rij en kolom wordt geplaatst. Voor de Dag van de afmeting van de Week, **[!UICONTROL Visits]** is bijbehorende metrisch.

   ![](assets/correlation_matrix_1.png)

   De correlatie is 1.000 omdat u metrisch tegen zich vergelijkt (die op een perfecte, maar onbruikbare, correlatie wijst.)

1. Verander één van de metriek.

   Klik en selecteer met de rechtermuisknop **[!UICONTROL Change Metric]** om metrisch in of de rij of kolom te veranderen. Dit plaatst - omhoog een correlatie tussen twee metriek van waarde.

   Bijvoorbeeld, verander **[!UICONTROL Visits]** metrisch in de kolom in **[!UICONTROL Internal Searches]**. Klik met de rechtermuisknop en selecteer [!DNL Metric] > [!DNL Custom Events] > [!DNL Custom Event 1-10] > [!DNL Internal Searches].

   ![](assets/correlation_matrix_change_metric.png)

1. Voeg meer metriek aan de Matrijs van de Correlatie toe.

   Klik in een metrische kolom of een rij met de rechtermuisknop aan. Bijvoorbeeld, van het Metrische menu, voeg toe [!DNL Metric] > [!DNL Custom Events] > [!DNL Custom Event 1-10] > [!DNL Sign in Error].

   ![](assets/correlation_matrix_11.png)

   Nieuwe metrisch zal in een kolom met een correlatienummer verschijnen. U kunt andere metriek, zoals toevoegen **[!UICONTROL Email Signups]**, om de lijst uit te bouwen.

   ![](assets/correlation_matrix_6.png)

   Of voeg metriek aan rijen toe om tegen metriek in kolommen te vergelijken.

   ![](assets/correlation_matrix_add_metric.png)

1. (facultatief) beperk metrisch door een afmetingselement toe te voegen.

   Klik in de werkruimte met de rechtermuisknop aan en selecteer **[!UICONTROL Table]**. Van de open afmetingslijst, druk CTRL + Alt en sleep het element over metrisch in een kolom of een rij. Het element zal naast metrisch tussen haakjes verschijnen.

   Bijvoorbeeld, voor **[!UICONTROL Visits]** metrisch, kunt u het beperken door te selecteren **[!UICONTROL Country]** zoals **[!UICONTROL New Zealand]**.

   ![](assets/correlation_matrix_dim_element.png)

   Bericht dat wanneer u een afmetingselement selecteert, de correlatie in alle metriek verandert die op het geselecteerde afmetingselement wordt gebaseerd. Slechts zal metrisch Bezoek voor &quot;Nieuw Zeeland&quot;worden beperkt zodra het afmetingsvenster wordt gesloten.

   >[!NOTE]
   >
   >Als het veranderen van metrisch met een afmetingsbeperking (door met de rechtermuisknop aan te klikken en te selecteren **[!UICONTROL Change Metric]**), zal het afmetingselement dat metrisch beperkt worden verloren. U zult het afmetingselement moeten opnieuw toevoegen.

1. Creeer een [Binaire Filter](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-binary-filter.md#concept-24e1daff43c540f69019f236976da31c) om metrisch verder te beperken. Klik metrisch in de lijst met de rechtermuisknop aan en selecteer Binaire Filter van het menu.

## Doelstellingen voor het plannen en analyseren van correlatie {#section-cc322da60b7e417ba29e72b0afeb6f79}

Het volgende is algemene doelstellingen voor de bouw van een Matrijs van de Correlatie.

**Identificeer het verband tussen twee metriek tegen een gespecificeerde afmeting**. In het voorbeeld, werd de matrijs gebouwd rond de kernafmeting, Dag van de Week, met het metrieke Bezoek, E-mailSignups, en SignIn Fouten in vergelijking met Interne Onderzoeken, Login, en Onderzoek toonde metrische gebeurtenissen.

**Ontwikkelen van hypotheses om de analyse** te concentreren. Na het runnen van een correlatieanalyse, moet uw volgende stap gebiedsdelen en correlatie van de metriek zoeken. Bijvoorbeeld, verstrekt het begrip dat de interne onderzoeken een effect op e-mailsign-ups hebben een weg om die verhouding te voorspellen en marketing campagnes of het ontwerp van de Webnavigatie te wijzigen.

**Identificeer metriek om geavanceerdere algoritmen** voor het exploiteren van gegevens te omvatten. In de meeste gevallen, zullen de belangrijkste metriek worden geïdentificeerd omdat zij zullen worden gezien beïnvloedend veelvoudige correlaties. U kunt die zeer belangrijke metriek nu nemen en hen toepassen op extra gegevens mijnenanalyse voor dieper inzicht.

## Opmerkingen over de correlatiematrix {#section-ef3626c665ea468a9ecdad624b4132f5}

**Het filtreren en het selecteren op afmetingselementen binnen een lijst vergelijken als waarden**. Bijvoorbeeld, geeft het gebruiken van Dag van de afmeting van de Week en dan het klikken in een element van die kernafmeting, zoals het klikken op een specifieke dag binnen de de afmetingslijst van de Dag van Week, één aan één gelijke bij 100% terug die geen bruikbare correlatie verstrekt. Omdat de worteldimensie Dag van de Week was, zal om het even welke selectie binnen de Dag van de de afmetingslijst van de Week de matrijs veranderen om een één-op-één correlatie te zijn.

![](assets/correlation_matrix_10.png)

Nochtans, is 1 tot 1 correlatie (wanneer één enkele selectie van alle elementen) slechts op die specifieke dag wordt gemaakt. Als u veelvoudige selecties maakt dan blijft het niet noodzakelijk een 1 tot 1 correlatie, en zal niet altijd een 100 percentengelijke ongeacht het selecteren van 1 of 1+ dagen van de week opleveren.

**De statistische correlaties zijn niet gelijk aan het Correlated Model** van Gegevens, de historische verwijzing van de producten van de Analyse van Adobe. De statistische correlatie in de gegevenswerkbank is gebaseerd op het [Pearson Correlatiemodel](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-pearsons.md#concept-5996cb8c89fd4df5b47b7318e7a1d29c).

**De Correlatie van de vertoning in een Plot** van de Scatter. Klik de titel op een Plot van de Scatter met de rechtermuisknop aan en kies [!DNL Display Correlation] van het [!DNL Visualization] menu. De waarde van de Correlatie zal in de hogere juiste sectie van het Plot van de Scatter tonen.

>[!NOTE]
>
>De matrijs van het Plot van de Vervanger en van Pearsons zal &quot;de Fout van de Berekening&quot;tonen als de toepassing niet de correlatieberekening van Pearsons kan in werking stellen. Dit is gewoonlijk toe te schrijven aan ontoereikende gegevens, die de vergelijking kunnen veroorzaken om te proberen om door 0 te verdelen.
