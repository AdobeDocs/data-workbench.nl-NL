---
description: De werkbank 6.1 van gegevens de versienota's omvatten nieuwe eigenschappen, verbeteringsvereisten, insectenmoeilijke situaties, en bekende kwesties.
solution: Analytics
title: Data Workbench 6.2 Release Notes
topic: Data workbench
uuid: 5bfb558a-ce85-4b4a-95dc-ccef337c4d1b
translation-type: tm+mt
source-git-commit: 2cba66a160fec9154796f093d04a422a5b0da265

---


# Data Workbench 6.2 Release Notes{#data-workbench-release-notes}

De werkbank 6.1 van gegevens de versienota&#39;s omvatten nieuwe eigenschappen, verbeteringsvereisten, insectenmoeilijke situaties, en bekende kwesties.

## Nieuwe functies {#section-1225066ea8f44cf68e42e019d0bca816}

De Werkbank 6.1 van gegevens omvat deze nieuwe eigenschappen:

| Kenmerken | Beschrijving |
|--- |--- |
| 64-bits Windows-upgrade | De server van de gegevenswerkbank, rapportserver, en cliëntcomponenten worden bevorderd om slechts op de werkende systemen met 64 bits van Vensters te lopen. |
| Propensiteitsscore | Het noteren van uw publiek laat u klantenloyaliteit identificeren en statistisch waarnemen wie waarschijnlijk een verkoop zal omzetten of met een verhaal of een campagne in wisselwerking staat. Het rangschikken van de dichtheid omvat nu deze visualisaties om modellen te bekijken en de veranderende correlatie van geselecteerde metriek te tonen.<ul><li>De modelKijker onderzoekt een logistiek regressiemodel dat met het Scoren van de Volheid wordt geproduceerd, tonend de coëfficiëntgewichten van elke inputvariabele (met inbegrip van de constante termijn) en hun statistische foutenwaaier. </li><li>De grafieken van de lift en van de Aanwinst worden gebruikt om de potentiële toename van een genoteerd gegevensmodel te evalueren.</li><li>De fusiematrix geeft vier tellingen door de combinatie van Actual Positive (AP), Actual Negative (AN), Predicted Positive (PP), en Voorspeld Negatief (PN).</li> <li>Beginnend met v6.1, hebt u nu een sparen optie om de aantallen te bewaren die op twee types worden gebaseerd: afmetingen, afmetingen en maatstaven.</li><li>U kunt CTRL-alt nu klikken en slepen en laten vallen om elementen in het Scoren van de Volheid en de Bouwer van de Cluster toe te voegen. Eerder om lijstelementen toe te voegen, moest u van de lijst aan de doos van Elementen slepen.</li></ul> |
| Gegevenswerkbank nu in het Chinees | De werkbank van gegevens steunt nu Vereenvoudigd Chinees voor de cliënttoepassing. De werkbank van gegevens steunt ook de Redacteur van de Methode van de Input (IME) als secundair proces van de tekstingang voor internationale talen. |
| Wiskundige functies | U kunt Wiskundige functies aan metriek, wiskundetransformaties, en aantekenvelcellen nu toevoegen om datasets verder te berekenen. |
| Statistische uitnodigingen | De lijsten bieden nu een summiere vraag-uit van statistieken voor metrische kolommen aan. De vraag-uit kan het gemiddelde, standaardafwijking, minimum en maximumwaarden, variantie, en totale telling voor de kolom tonen. Het kan in aan om het even welke selectie en evaluatie worden factored. |
| Correlatiematrix, filter | De matrijs van de Correlatie is bijgewerkt met een Binaire Filter om u waarden voor één of allebei van de gecorreleerde metriek te laten beperken, toestaand u om uw vergelijking beter te concentreren. Ook, kunt u de elementen van de Dimensie van een lijst van de Dimensie nu toevoegen door CTRL + Alt te klikken en elementen te slepen aan de matrijskolom of de rij die moeten worden geëvalueerd. |
| Fallout-label verbergen in trechter-visualisatie | Knevel tussen het tonen van en het verbergen van neervaletiketten in een visualisatie van het Kanaal door de titel met de rechtermuisknop aan te klikken en de Uitval van de Huid te selecteren. |

## Tabel kolommen sorteren{#sorting-table-columns}

De lijstkolommen van de soort alfabetisch of door verordeningen.

Om elementen in een lijst van de Dimensie beter te selecteren, kunt u tot de eerste kolom alfabetisch of door verordeningen opdracht geven door de **[!UICONTROL Sort]** menuoptie te selecteren.

# karakter zal tonen wanneer een kolom door verordeningen (het gebrek) wordt gesorteerd.

**Optie Sorteren selecteren**

Om sorterende opties tussen rangschikkend en alfabet te veranderen, klik en selecteer met de rechtermuisknop aan **[!UICONTROL Sort]**. Klik de pijl om de orde om te keren.

![](assets/sort_table_alpha.png)

>[!NOTE]
>
>U kunt andere kolommen door rangschikkend sorteren door de naam van de kolom te klikken.

## Fallout-labels verbergen in trechter

Knevel om de etiketten van de neerslag in een visualisatie van de Kranel te openen.

De visualisatie van het Kanaal identificeert waar een klant een marketing campagne verlaat of van een bepaalde omzettingsweg terwijl het in wisselwerking staan met uw website of dwars-kanaal campagne afleidt. De linkerkant van de visualisatie van de Trechter toont de resultaten van een bezoek of bezoekers, terwijl de rechterkant de &quot;Vallout&quot;van degenen toont die een gespecificeerde weg verlaten.

![](assets/c_funnel_hide_fallout.png)

Wanneer in een **[!UICONTROL Funnel]** visualisatie, kunt u de titel met de rechtermuisknop aanklikken en **[!UICONTROL Hide Fallout]** van het menu selecteren om de reserveetiketten te verbergen.

## Bekende problemen {#section-ff2180c6871c413480e15fa915c253b9}

* Wanneer het invoeren van een werkruimte, wordt een foutenmelding getoond alhoewel de invoer succesvol was.

   Werkruimte: Klik O.K. om de fout te negeren. De werkruimte wordt met succes ingevoerd.

**Vereenvoudigde Chinese lokalisatiekwesties**

* De de dialoogdoos en het bericht na het klikken &quot;voorleggen&quot;worden getoond wanneer het plaatsen van het doel in het Scoren visualisatie die onleesbaar zijn.

   Werkruimte: Geen.
* Wanneer het gebruiken van woordomslag in de visualisatie van het Aantekenvel, worden de gelokaliseerde woorden niet correct verpakt. De extra troepenkarakters worden toegevoegd aan het koord.

   Werkruimte: Geen
* Onbekwaam om te lanceren [!DNL Insight.exe] als de installatiefolder met niet-Engelse karakters wordt genoemd.

   Werkruimte: Houd standaardnamen of noem het gebruiken van slechts Engelse karakters in de omslagweg anders om uitvoerbare lijsten te lanceren.
