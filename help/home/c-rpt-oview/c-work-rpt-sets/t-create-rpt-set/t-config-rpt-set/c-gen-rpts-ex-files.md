---
description: Informatie om rapporten als dossiers van Excel te produceren.
title: Rapporten genereren als Microsoft Excel-bestanden
uuid: 0717a916-93d6-4b8e-a2ff-e9179ba4a66e
exl-id: 4e644867-db5e-4ca9-a2bf-1193e031f2bf
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Rapporten genereren als Microsoft Excel-bestanden{#generating-reports-as-microsoft-excel-files}

Informatie om rapporten als dossiers van Excel te produceren.

Aan de volgende eisen moet worden voldaan:

* Microsoft Excel moet op dezelfde computer zijn geïnstalleerd als [!DNL Report Server].
* De gebruikersaccount waaronder het proces [!DNL Report Server] wordt uitgevoerd, moet toestemming hebben om toegang te krijgen tot Microsoft Excel.

   >[!NOTE]
   >
   >
   >    
   >    
   >    * Wanneer u rapporten als dossiers van Excel produceert, opent u een nieuw geval van Excel. Zie [http://support.microsoft.com/kb/257757](http://support.microsoft.com/kb/257757) voor meer informatie over dit proces.
   >    * Hoewel de werkbank van gegevens meer dan 256 kolommen en 65.536 rijen van gegevens steunt, Microsoft Excel niet.


Als aan deze vereisten wordt voldaan, [!DNL Report Server] begint automatisch Microsoft Excel en outputgegevens van bepaalde visualisaties, afmeting en waardelegends, en tekstannotaties aan een nieuw werkboek van Excel met één visualisatie per aantekenvel.

>[!NOTE]
>
>Gegevens worden niet geëxporteerd uit grafieken, padbrowsers, procesafbeeldingen, verstrooiingspunten en globes.

Tenzij u een [!DNL Custom Title] voor visualisatie hebt gespecificeerd, wordt het type van venster (bijvoorbeeld, de Lijst van de Film) gebruikt als aantekenvelsnaam.

Voor meer informatie over het specificeren van [!DNL Custom Titles] voor visualisaties, zie [de Gids van de Cliënt van de Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html).

## Een sjabloonbestand gebruiken {#section-40ab11916f464b1a88214ab969da6751}

U kunt een rapport ook produceren als dossier van Excel gebruikend een malplaatjeExcel ( [!DNL .xls] of [!DNL .xlsx]) dossier. Het gebruik van een sjabloonbestand kan de hoeveelheid tijd verminderen die u besteedt aan het opmaken van de gegevens telkens wanneer het rapport wordt gegenereerd.

Dit sjabloonbestand moet een [!DNL .xls]- of [!DNL .xlsx]-bestand zijn, geen [!DNL .xlt]-bestand.

U kunt verkiezen om een malplaatje voor elk individueel rapport, een generisch malplaatje voor al uw rapporten, of een combinatie allebei te bepalen. Deze twee punten sluiten elkaar niet uit, zodat kunt u een generisch malplaatje bepalen en dan specifieke malplaatjes eveneens bepalen.

Om een rapport te produceren gebruikend een generisch malplaatje dat u voor alle rapporten gebruikt, moet u de naam van dat dossier van Excel in de Standaardparameter van het Malplaatje van Excel in [!DNL Report.cfg] voor dat dossier van de rapportreeks specificeren, dan plaats het malplaatjedossier in de zelfde omslag zoals [!DNL Report.cfg] voor die rapportreeks (*gegevens werkbench installatiemap*\*ProfileName*\Reports\*ReportSetName*). Voor informatie over deze parameter, zie [Parameters Report.cfg](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

Om een rapport te produceren gebruikend een malplaatje dat voor een rapport specifiek is, moet u het dossier van Excel het zelfde als het dossier van de rapportwerkruimte ( [!DNL .vw]) noemen, dan plaats het malplaatjedossier in de zelfde omslag zoals het dossier van de rapportwerkruimte ( [!DNL .vw]).

Wanneer het rapport wordt geproduceerd, worden de bestaande met tabbladen in het malplaatje (elk die één visualisatie vertegenwoordigen) opnieuw bevolkt met de meest recente gegevens van het rapport, terwijl om het even welke nieuwe vensters die niet in het malplaatje zoals van labels voorzien bladen aanwezig zijn worden genegeerd. Alle andere tabbladen in het sjabloonbestand blijven ongewijzigd.

Bovendien als u een macro hebt die in het dossier van malplaatjeExcel wordt bepaald dat u automatisch zou willen lopen wanneer het rapport wordt geproduceerd, noem de macro &quot;VSExport.&quot;
