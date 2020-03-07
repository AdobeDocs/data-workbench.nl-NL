---
description: Informatie om rapporten als dossiers van Excel te produceren.
solution: Analytics
title: Rapporten genereren als Microsoft Excel-bestanden
topic: Data workbench
uuid: 0717a916-93d6-4b8e-a2ff-e9179ba4a66e
translation-type: tm+mt
source-git-commit: 2cba66a160fec9154796f093d04a422a5b0da265

---


# Rapporten genereren als Microsoft Excel-bestanden{#generating-reports-as-microsoft-excel-files}

Informatie om rapporten als dossiers van Excel te produceren.

Aan de volgende eisen moet worden voldaan:

* Microsoft Excel moet op het zelfde systeem worden geïnstalleerd zoals [!DNL Report Server].
* De gebruikersrekening waaronder het [!DNL Report Server] proces loopt moet toestemming hebben om tot Microsoft Excel toegang te hebben.

   >[!NOTE]
   >
   >
   >    
   >    
   >    * Wanneer u rapporten als dossiers van Excel produceert, opent u een nieuw geval van Excel. Voor meer informatie over dit proces, zie [http://support.microsoft.com/kb/257757](http://support.microsoft.com/kb/257757).
   >    * Hoewel de gegevenswerkbank meer dan 256 kolommen en 65.536 rijen van gegevens steunt, Microsoft Excel niet.


Als aan deze vereisten wordt voldaan, begin [!DNL Report Server] automatisch Microsoft Excel en outputgegevens van bepaalde visualisaties, afmeting en waardelegends, en tekstannotaties aan een nieuw werkboek van Excel met één visualisatie per aantekenvel.

>[!NOTE]
>
>Het gegeven wordt niet uitgevoerd van grafieken, wegbrowsers, proceskaarten, verstrooidslagen, en globes.

Tenzij u een [!DNL Custom Title] voor de visualisatie hebt gespecificeerd, wordt het type van venster (bijvoorbeeld, de Lijst van de Film) gebruikt als aantekenvelnaam.

Voor meer informatie over het specificeren [!DNL Custom Titles] voor visualisaties, zie de Gids van de Cliënt van de Werkbank van [Gegevens](https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html).

## Een sjabloonbestand gebruiken {#section-40ab11916f464b1a88214ab969da6751}

U kunt een rapport als dossier van Excel ook produceren gebruikend een malplaatjeExcel ( [!DNL .xls] of [!DNL .xlsx]) dossier. Het gebruiken van een malplaatjedossier kan de hoeveelheid tijd verminderen dat u het formatteren van uw gegevens besteedt telkens als het rapport wordt geproduceerd.

Dit malplaatjedossier moet een [!DNL .xls] of [!DNL .xlsx] dossier, niet een [!DNL .xlt] dossier zijn.

U kunt verkiezen om een malplaatje voor elk individueel rapport, een generisch malplaatje voor elk van uw rapporten, of een combinatie allebei te bepalen. Deze twee punten zijn niet wederzijds - exclusief, zodat kunt u een generisch malplaatje bepalen en dan specifieke malplaatjes ook bepalen.

Om een rapport te produceren dat een generisch malplaatje gebruikt dat u voor alle rapporten gebruikt, moet u de naam van dat dossier van Excel in de parameter van het Malplaatje Standaard van Excel in [!DNL Report.cfg] voor dat rapport vastgestelde dossier specificeren, dan plaats het malplaatjedossier in de zelfde omslag zoals [!DNL Report.cfg] voor die rapportreeks (de installatiefolder *\*ProfileName*\Reports\*ReportSetName* van de* gegevenswerkbank). Voor informatie over deze parameter, zie Parameters [Report.cfg](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

Om een rapport te produceren dat een malplaatje gebruikt dat voor een rapport specifiek is, moet u het dossier van Excel het zelfde als het dossier van de rapportwerkruimte ( [!DNL .vw]) noemen, dan plaats het malplaatjedossier in de zelfde omslag zoals het dossier van de rapportwerkruimte ( [!DNL .vw]).

Wanneer het rapport wordt geproduceerd, worden de bestaande van labels voorzien bladen in het malplaatje (elk die één visualisatie vertegenwoordigen) herhaald met de meest recente gegevens van het rapport, terwijl om het even welke nieuwe vensters die niet aanwezig in het malplaatje zoals van labels voorzien bladen zijn worden genegeerd. Om het even welke andere van labels voorzien bladen in het malplaatjedossier blijven onveranderd.

Bovendien als u een macro hebt die in het dossier van malplaatjeExcel wordt bepaald dat u automatisch zou willen lopen wanneer het rapport wordt geproduceerd, noem de macro &quot;VSExport.&quot;
