---
description: Informatie om rapporten als dossiers van Excel te produceren.
title: Rapporten genereren als Microsoft Excel-bestanden
uuid: 0717a916-93d6-4b8e-a2ff-e9179ba4a66e
exl-id: 4e644867-db5e-4ca9-a2bf-1193e031f2bf
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Rapporten genereren als Microsoft Excel-bestanden{#generating-reports-as-microsoft-excel-files}

{{eol}}

Informatie om rapporten als dossiers van Excel te produceren.

Aan de volgende eisen moet worden voldaan:

* Microsoft Excel moet op dezelfde computer zijn geïnstalleerd als [!DNL Report Server].
* De gebruikersaccount waaronder de [!DNL Report Server] het proces wordt uitgevoerd moet toestemming hebben om tot Microsoft Excel toegang te hebben.

   >[!NOTE]
   >
   >
   >
   >
   >    * Wanneer u rapporten als dossiers van Excel produceert, opent u een nieuw geval van Excel. Voor meer informatie over dit proces raadpleegt u [https://support.microsoft.com/kb/257757](https://support.microsoft.com/kb/257757).
   >    * Hoewel de werkbank van gegevens meer dan 256 kolommen en 65.536 rijen van gegevens steunt, Microsoft Excel niet.


Indien aan deze eisen is voldaan, [!DNL Report Server] begint automatisch Microsoft Excel en outputgegevens van bepaalde visualisaties, afmeting en waardelegends, en tekstannotaties aan een nieuw werkboek van Excel met één visualisatie per aantekenvel.

>[!NOTE]
>
>Gegevens worden niet geëxporteerd uit grafieken, padbrowsers, procesafbeeldingen, verstrooiingspunten en globes.

Tenzij u een [!DNL Custom Title] voor visualisatie wordt het type venster (bijvoorbeeld Filmtabel) gebruikt als de naam van het werkblad.

Meer informatie over het opgeven van [!DNL Custom Titles] voor visualisaties raadpleegt u de [Clientgids voor Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html).

## Een sjabloonbestand gebruiken {#section-40ab11916f464b1a88214ab969da6751}

U kunt ook een rapport als dossier van Excel produceren gebruikend een malplaatjeExcel ( [!DNL .xls] of [!DNL .xlsx]). Het gebruik van een sjabloonbestand kan de hoeveelheid tijd verminderen die u besteedt aan het opmaken van de gegevens telkens wanneer het rapport wordt gegenereerd.

Dit sjabloonbestand moet een [!DNL .xls] of [!DNL .xlsx] bestand, geen [!DNL .xlt] bestand.

U kunt verkiezen om een malplaatje voor elk individueel rapport, een generisch malplaatje voor al uw rapporten, of een combinatie allebei te bepalen. Deze twee punten sluiten elkaar niet uit, zodat kunt u een generisch malplaatje bepalen en dan specifieke malplaatjes eveneens bepalen.

Om een rapport te produceren gebruikend een generisch malplaatje dat u voor alle rapporten gebruikt, moet u de naam van dat dossier van Excel in de Standaardparameter van het Malplaatje van Excel in specificeren [!DNL Report.cfg] voor dat rapportsetbestand, plaatst u het sjabloonbestand in dezelfde map als het [!DNL Report.cfg] voor dat rapportenset (*installatiemap gegevenswerkbank*\*ProfileName*\Reports\*ReportSetName*). Voor informatie over deze parameter raadpleegt u [Report.cfg-parameters](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

Om een rapport te produceren gebruikend een malplaatje dat voor een rapport specifiek is, moet u het dossier van Excel het zelfde als rapportwerkruimte noemen ( [!DNL .vw]), plaatst u het sjabloonbestand in dezelfde map als de rapportwerkruimte ( [!DNL .vw]).

Wanneer het rapport wordt geproduceerd, worden de bestaande met tabbladen in het malplaatje (elk die één visualisatie vertegenwoordigen) opnieuw bevolkt met de meest recente gegevens van het rapport, terwijl om het even welke nieuwe vensters die niet in het malplaatje zoals van labels voorzien bladen aanwezig zijn worden genegeerd. Alle andere tabbladen in het sjabloonbestand blijven ongewijzigd.

Bovendien als u een macro hebt die in het dossier van malplaatjeExcel wordt bepaald dat u automatisch zou willen lopen wanneer het rapport wordt geproduceerd, noem de macro &quot;VSExport.&quot;
