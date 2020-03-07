---
description: Verbindingen met extra informatie over specifieke parameters in het dossier van het Logboek Processing.cfg.
solution: Analytics
title: Parameters voor logboekverwerking
topic: Data workbench
uuid: 97b25665-f588-4f44-8f71-2382600d1b6f
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Parameters voor logboekverwerking{#log-processing-parameters}

Verbindingen met extra informatie over specifieke parameters in het dossier van het Logboek Processing.cfg.

<!--
c_data_filters.xml
-->

## Gegevensfilters {#data-filters}

De filters die in het [!DNL Log Processing.cfg] dossier worden bepaald omvatten het volgende:

* Eindtijd
* Hash Drempel
* Begintijd

Het filtreren dat door deze parameters wordt bepaald komt voor nadat de logboekingangen de decoders en na transformaties maar vóór hun evaluatie door [!DNL Log Entry Condition]verlaten. In het algemeen, resulteert het veranderen van om het even welk van deze parameters in veranderingen in de samenstelling van de dataset.

De geadviseerde techniek om [!DNL Sensor] gegevensbronnen te gebruiken om een dataset te construeren die een specifieke periode behandelt is de parameters van de Tijd van het Begin en van de Tijd van het Eind voor de dataset te gebruiken.

Het gebruiken van de parameters van de Tijd van het Begin en van de Tijd van het Eind is aangewezen aan andere technieken, zoals het bewegen van logboekdossiers om hen door folder te scheiden. Door de begin en eindtijden voor de dataset te plaatsen, gebruikt de server van de gegevenswerkbank automatisch die logboekingangen die binnen het bepaalde interval voorkwamen. Veronderstellend dat de Tijd van het Eind in het verleden is, werkt de server van de gegevenswerkbank typisch de dataset bij gebruikend de zelfde reeks logboekingangen, zelfs als de dataset door, bijvoorbeeld, toevoegend een nieuwe transformatie wordt bijgewerkt.

<!--
c_log_entry_con.xml
-->

## Logboekinvoer

In wezen, is het een het filtreren proces op de beschikbare logboekingangen. Als de [!DNL Log Entry Condition] winst een waarde van vals, de logboekingang uit de beschikbare reeks logboekingangen wordt gefiltreerd.

Het [!DNL Log Entry Condition] wordt beschreven door het gebruik van condities (zie [Voorwaarden](../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md)) en kan om het even welke inputgebieden gebruiken die door [!DNL Sensor] (zie de Gids van de Werkbank van *Gegevens[!DNL Sensor]) worden verzameld of om het even welke uitgebreide gebieden die door transformaties in het* [!DNL Log Processing.cfg] dossier worden geproduceerd om de testvoorwaarden te bepalen. [!DNL Log Entry] de omstandigheden worden toegepast tijdens de verwerking van het stamhout en kunnen desgewenst tijdens de verwerking worden toegepast.

Dit voorbeeld toont het gebruik van [!DNL log entry condition] voor websitegegevens aan. U kunt gebruiken [!DNL Log Entry Condition] om datasets tot stand te brengen die zich op een specifiek gedeelte van de website of bezoekers concentreren die één of andere specifieke actie op de plaats uitvoeren.

Het [!DNL Log Entry Condition] in dit voorbeeld leidt tot een dataset die slechts die logboekingangen omvat die deel van de opslag van de plaats uitmaken. Door het [!DNL RECondition test] met het passende patroon [!DNL "/store/.*"] en het [!DNL cs-uri-stem] [!DNL "/store/"] gebied als input aan de regelmatige uitdrukking te gebruiken, slechts zijn de Web-pagina&#39;s die met het koord beginnen inbegrepen in de dataset.

![](assets/cfg_LogProcessing_LogEntryCondition.png)

<!--
c_key_split.xml
-->

## Sleutelsplitsing {#key-split}

Het aantal het volgen IDs in de dataset wordt kunstmatig verhoogd, maar het totale aantal logboekingangen die door de server van de gegevenswerkbank worden verwerkt wordt niet kunstmatig verhoogd, daardoor bewarend het totale aantal telbare gebeurtenissen in de dataset. Nadat de gegevens voor één enkel element worden verdeeld, wordt het gegeven altijd geassocieerd met twee verschillende volgende IDs en kan niet worden verwant.

Bijvoorbeeld, als u met Webgegevens werkt, vertegenwoordigt elke volgende identiteitskaart een unieke bezoeker. Als u sleutel het verdelen toelaat, worden de bezoekers in uw dataset met grote hoeveelheden gebeurtenisgegevens verdeeld in veelvoudige bezoekers. Terwijl het aantal bezoekers in de dataset kunstmatig wordt verhoogd, wordt het totale aantal telbare gebeurtenissen zoals paginameningen of reserveringen niet kunstmatig verhoogd. Na splitsing kunnen de gegevens voor de subbezoekers niet worden gerelateerd.

De zeer belangrijke splitsing gebruikt een probabilistisch algoritme. Dientengevolge, is er een afweging tussen geheugengebruik, de mislukkingswaarschijnlijkheid, de belangrijkste het verdelen drempel ( [!DNL Split Key Bytes]), en de datasetgrootte. Met de geadviseerde montages (zoals hieronder vermeld), is het mislukkingstarief laag. Van de elementen waarvan de gebeurtenisgegevens de belangrijkste het splitsen drempel overschrijden, zal ongeveer 1 op 22.000 (gewoonlijk minder dan 1 per dataset) sommige van hun gegevens beknot eerder dan gesplitst hebben.

De geadviseerde waarden voor elke parameter (zonder en met zeer belangrijke splitsing) worden getoond in de volgende lijst.

| Parameter | Geen sleutelsplitsing | Key Splitsing |
|---|---|---|
| Maximum aantal sleutelbytes groeperen | 1e6 | 2e6 |
| Splitsen Key Bucket-ruimte | 6e6 | 6e6 |
| Sleutelbytes splitsen | 0 | 1e6 |
| Splitsing van de belangrijkste ruimteverhouding | 10 | 10 |

[!DNL Group Maximum Key Bytes] specificeert de maximumhoeveelheid gebeurtenisgegevens die voor één enkele volgende identiteitskaart kunnen worden verwerkt Gegevens die deze grens overschrijden, worden gefilterd uit het proces voor de samenstelling van de dataset. [!DNL Split Key Bytes] vertegenwoordigt het aantal bytes waarbij één enkele volgende identiteitskaart in veelvoudige elementen wordt gesplitst. De elementen worden verdeeld bij ongeveer dit aantal bytes volgens een kansverdeling. [!DNL Split Key Space Ratio] en [!DNL Split Key Bucket Space] controleer het geheugengebruik en de mislukkingssnelheid van zeer belangrijke splitsing.

>[!NOTE]
>
>[!DNL Group Maximum Key Bytes], [!DNL Split Key Bytes], [!DNL Split Key Space Ratio], en [!DNL Split Key Bucket Space] allen moet voor zeer belangrijke splitsing worden verklaard behoorlijk te werken. Verander niet de waarden van deze parameters zonder Adobe te raadplegen.

