---
description: Statistische correlaties meten betekenisvolle relaties om kansen te identificeren door geavanceerde datamining.
title: Correlatiematrix
uuid: 7f6bdb65-dc31-4e27-9870-4c9402ee6031
exl-id: 79c23bb9-2b4b-4fe0-bfdb-52721fbbdf0c
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Correlatiematrix{#correlation-matrix}

Statistische correlaties meten betekenisvolle relaties om kansen te identificeren door geavanceerde datamining.

Met behulp van de correlatiecoëfficiënt [Pearsons](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-pearsons.md#concept-5996cb8c89fd4df5b47b7318e7a1d29c) verschaft de correlatiematrix u relevante informatie om de volgende stappen in een marketingcampagne beter te identificeren, om het siteontwerp te verbeteren of om de analyse van de klant voor extra correlatieafhankelijkheden verder te verfijnen.

## Een correlatiematrix maken {#section-87ed12ccc1af4196a1b6534e621c4cbb}

De Matrijs van de Correlatie vergelijkt metriek over een telbare of niet tellende dimensie. De matrix kan vervolgens worden gewijzigd om correlaties binnen de visualisatie te benadrukken door kleuren te kiezen of om deze te renderen als een tekstafbeelding, een warmtekaart of beide.

1. Open een correlatiematrix.

   Klik met de rechtermuisknop [!DNL Visualization] > [!DNL Predictive Analytics] > [!DNL Correlation Matrix]. De dimensietabel wordt geopend.

   ![](assets/correlation_matrix_2.png)

   Selecteer een dimensie, zoals [!DNL Time] > [!DNL Day of the Week] in dit menu. De correlatietabel wordt geopend met de afmetingen die zijn geïdentificeerd in de hoek van de matrix en de bijbehorende metrische waarde die in de rij en kolom is geplaatst. Voor de Dag van de dimensie van de Week, **[!UICONTROL Visits]** is bijbehorende metrisch.

   ![](assets/correlation_matrix_1.png)

   De correlatie is 1.000 omdat u metrisch met zich (die op een perfecte, maar onbruikbaar, correlatie wijst.) vergelijkt

1. Wijzig een van de meetwaarden.

   Klik met de rechtermuisknop en selecteer **[!UICONTROL Change Metric]** om een metrische waarde in de rij of kolom te wijzigen. Hiermee stelt u een correlatie in tussen twee waarden.

   In dit voorbeeld wijzigt u de metrische waarde **[!UICONTROL Visits]** in de kolom in **[!UICONTROL Internal Searches]**. Klik met de rechtermuisknop en selecteer [!DNL Metric] > [!DNL Custom Events] > [!DNL Custom Event 1-10] > [!DNL Internal Searches].

   ![](assets/correlation_matrix_change_metric.png)

1. Voeg meer metriek toe aan de Matrijs van de Correlatie.

   Klik met de rechtermuisknop in een metrische kolom of rij. Voeg in het menu Metrisch bijvoorbeeld [!DNL Metric] > [!DNL Custom Events] > [!DNL Custom Event 1-10] > [!DNL Sign in Error] toe.

   ![](assets/correlation_matrix_11.png)

   De nieuwe metrische waarde wordt weergegeven in een kolom met een correlatienummer. U kunt andere metriek, zoals **[!UICONTROL Email Signups]**, toevoegen om de lijst te bouwen.

   ![](assets/correlation_matrix_6.png)

   Of voeg metriek aan rijen toe om met metriek in kolommen te vergelijken.

   ![](assets/correlation_matrix_add_metric.png)

1. (facultatief) Beperk metrisch door een afmetingselement toe te voegen.

   Klik met de rechtermuisknop in de werkruimte en selecteer **[!UICONTROL Table]**. Druk in de tabel met geopende afmetingen op Ctrl + Alt en sleep het element over een metrische waarde in een kolom of rij. Het element verschijnt naast metrisch tussen haakjes.

   Bijvoorbeeld, voor **[!UICONTROL Visits]** metrisch, kunt u het beperken door **[!UICONTROL Country]** als **[!UICONTROL New Zealand]** te selecteren.

   ![](assets/correlation_matrix_dim_element.png)

   Wanneer u een dimensie-element selecteert, verandert de correlatie in alle metriek op basis van het geselecteerde dimensie-element. Slechts metrisch zal van het Bezoek voor &quot;Nieuw Zeeland&quot;worden beperkt zodra het afmetingsvenster wordt gesloten.

   >[!NOTE]
   >
   >Als het veranderen van metrisch met een afmetingsbeperking (door **[!UICONTROL Change Metric]** met de rechtermuisknop aan te klikken en te selecteren), zal het afmetingselement dat metrisch beperkt worden verloren. U moet het dimensie-element opnieuw toevoegen.

1. Creeer een [Binair Filter](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-binary-filter.md#concept-24e1daff43c540f69019f236976da31c) om metrisch verder te beperken. Klik metrisch in de lijst met de rechtermuisknop aan en selecteer Binair Filter van het menu.

## Doelstellingen voor planning en analyse van correlatie {#section-cc322da60b7e417ba29e72b0afeb6f79}

Hier volgen algemene doelstellingen voor het maken van een correlatiematrix.

**Identificeer het verband tussen twee metriek tegen een gespecificeerde afmeting**. In het voorbeeld werd de matrix gemaakt rond de kerndimensie, Dag van de week, met de metrieke Visit, E-mailmeldingen en SignIn-fouten in vergelijking met interne zoekopdrachten, aanmelding en enquête weergegeven metrische gebeurtenissen.

**Gebruik hypothesen om de analyse** te concentreren. Na het runnen van een correlatieanalyse, moet uw volgende stap gebiedsdelen en correlatie van de metriek zoeken. Als u bijvoorbeeld begrijpt dat interne zoekopdrachten van invloed zijn op e-mailaanmelding, kunt u die relatie voorspellen en marketingcampagnes of het ontwerpen van websitenavigaties wijzigen.

**Metriek identificeren om geavanceerdere algoritmen** voor gegevensbeheer op te nemen. In de meeste gevallen zullen de belangrijkste meetgegevens worden geïdentificeerd, omdat ze van invloed zullen zijn op meerdere correlaties. U kunt nu die belangrijke metriek nemen en hen op extra gegevens toepassen ontginning analyse voor dieper inzicht.

## Opmerkingen bij de functie Matrix correleren {#section-ef3626c665ea468a9ecdad624b4132f5}

**Bij het filteren en selecteren van dimensie-elementen in een tabel worden vergelijkbare waarden gebruikt**. Als u bijvoorbeeld Dag van de week gebruikt en vervolgens klikt in een element van die kerndimensie, zoals klikken op een bepaalde dag in de tabel met de afmetingen Dag van week, wordt een-op-een-overeenkomst weergegeven met 100%, wat geen bruikbare correlatie biedt. Omdat de hoofddimensie Dag van de Week was, zal elke selectie binnen de Dag van de Week metingstabel de matrix veranderen in een één-op-één correlatie.

![](assets/correlation_matrix_10.png)

De correlatie tussen 1 en 1 (wanneer één selectie van alle elementen is gemaakt) is echter slechts op die specifieke dag. Als u meerdere selecties maakt, blijft het niet altijd een correlatie van 1 tot 1 en levert het niet altijd een overeenkomst van 100 procent op, ongeacht of u 1 of 1+ dagen van de week selecteert.

**Statistische correlaties zijn niet gelijk aan het Correlated Data Model**, de historische referentie van Adobe Analytics-producten. De statistische correlatie in de gegevenswerkbank is gebaseerd op het [Pearson Correlation model](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-pearsons.md#concept-5996cb8c89fd4df5b47b7318e7a1d29c).

**Correlatie weergeven in een verstrooiingsperceel**. Klik met de rechtermuisknop op de titel op een verstrooiingsperceel en kies [!DNL Display Correlation] in het menu [!DNL Visualization]. De waarde voor Correlatie wordt weergegeven in de rechterbovensectie van het perceel Spreiding.

>[!NOTE]
>
>In de matrix Spreidingsperceel en Parels wordt &quot;Rekenfout&quot; weergegeven als de toepassing de berekening van de correlatie Paals niet kan uitvoeren. Dit is meestal het gevolg van onvoldoende gegevens, waardoor de vergelijking probeert te delen door 0.
