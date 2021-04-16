---
description: Koppelingen naar aanvullende informatie over specifieke parameters in het bestand Log Processing.cfg.
title: Parameters voor logverwerking
uuid: 97b25665-f588-4f44-8f71-2382600d1b6f
exl-id: f373e954-6827-4afa-9557-73e0a884a602
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 1%

---

# Parameters voor logverwerking{#log-processing-parameters}

Koppelingen naar aanvullende informatie over specifieke parameters in het bestand Log Processing.cfg.

<!--
c_data_filters.xml
-->

## Gegevensfilters {#data-filters}

De filters die in het [!DNL Log Processing.cfg] dossier worden bepaald omvatten het volgende:

* Eindtijd
* Hash-drempel
* Begintijd

Filteren die door deze parameters wordt bepaald komt voor nadat de logboekingangen de decoders en na transformaties maar vóór hun evaluatie door [!DNL Log Entry Condition] verlaten. Over het algemeen leidt het wijzigen van een van deze parameters tot wijzigingen in de samenstelling van de gegevensset.

De geadviseerde techniek om [!DNL Sensor] gegevensbronnen te gebruiken om een dataset te construeren die een specifieke periode behandelt is de parameters van de Tijd van het Begin en van de Eind van het Eind voor de dataset te gebruiken.

Het gebruik van de parameters Begintijd en Eindtijd heeft de voorkeur boven andere technieken, zoals het verplaatsen van logbestanden om deze op directory te scheiden. Door de begin en eindtijden voor de dataset te plaatsen, gebruikt de server van de gegevenswerkbank automatisch slechts die logboekingangen die binnen het bepaalde interval voorkwamen. Ervan uitgaande dat de Tijd van het Eind in het verleden is, werkt de server van de gegevenswerkbank typisch de dataset bij gebruikend de zelfde reeks logboekingangen, zelfs als de dataset door, bijvoorbeeld, het toevoegen van een nieuwe transformatie wordt bijgewerkt.

<!--
c_log_entry_con.xml
-->

## Logboekvermelding

In wezen is het een filterproces op de beschikbare logboekingangen. Als [!DNL Log Entry Condition] een waarde van vals terugkeert, wordt de logboekingang gefilterd uit de beschikbare reeks logboekingangen.

De [!DNL Log Entry Condition] wordt beschreven door het gebruik van voorwaardenbewerkingen (zie [Voorwaarden](../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md)) en kan alle invoervelden gebruiken die worden verzameld door [!DNL Sensor] (zie de *Data Workbench [!DNL Sensor] Guide*) of alle uitgebreide velden die worden geproduceerd door transformaties in het [!DNL Log Processing.cfg]-bestand om de testvoorwaarden te definiëren. [!DNL Log Entry] de voorwaarden worden toegepast tijdens logboekverwerking en kunnen facultatief tijdens transformatie worden toegepast.

In dit voorbeeld wordt het gebruik van de [!DNL log entry condition] voor websitegegevens getoond. Met de [!DNL Log Entry Condition] kunt u gegevenssets maken die zich richten op een specifiek gedeelte van de website of bezoekers die een bepaalde specifieke handeling op de site uitvoeren.

[!DNL Log Entry Condition] in dit voorbeeld leidt tot een dataset die slechts die logboekingangen omvat die deel van de opslag van de plaats uitmaken. Door [!DNL RECondition test] met het passende patroon [!DNL "/store/.*"] en het [!DNL cs-uri-stem] gebied als input aan de regelmatige uitdrukking te gebruiken, worden slechts Web-pagina&#39;s die met het koord [!DNL "/store/"] beginnen inbegrepen in de dataset.

![](assets/cfg_LogProcessing_LogEntryCondition.png)

<!--
c_key_split.xml
-->

## Key split {#key-split}

Het aantal het volgen IDs in de dataset wordt kunstmatig verhoogd, maar het totale aantal logboekingangen die door de server van de gegevenswerkbank worden verwerkt wordt niet kunstmatig verhoogd, daardoor bewarend het totale aantal telbare gebeurtenissen in de dataset. Nadat de gegevens voor één element zijn gesplitst, worden de gegevens voorgoed gekoppeld aan twee verschillende id&#39;s voor reeksspatiëring en kunnen ze niet meer worden gekoppeld.

Als u bijvoorbeeld met webgegevens werkt, vertegenwoordigt elke volgende-id een unieke bezoeker. Als u sleutelsplitsing inschakelt, worden de bezoekers in uw gegevensset met grote hoeveelheden gebeurtenisgegevens gesplitst in meerdere bezoekers. Hoewel het aantal bezoekers in de gegevensset kunstmatig wordt verhoogd, wordt het totale aantal telbare gebeurtenissen zoals paginaweergaven of boekingen niet kunstmatig verhoogd. Na het splitsen kunnen de gegevens voor de subbezoekers niet meer worden gerelateerd.

Bij sleutelsplitsing wordt een probabilistisch algoritme gebruikt. Dientengevolge, is er een compromis tussen geheugengebruik, de mislukkingswaarschijnlijkheid, de belangrijkste het splitsen drempel ( [!DNL Split Key Bytes]), en de datasetgrootte. Met de aanbevolen instellingen (zoals hieronder vermeld) is de foutfrequentie laag. Van die elementen waarvan de gebeurtenisgegevens de belangrijkste splitsingsdrempel overschrijden, zullen ongeveer 1 op 22.000 (gewoonlijk minder dan 1 per dataset) sommige van hun gegevens afgebroken eerder dan verdeeld hebben.

De aanbevolen waarden voor elke parameter (zonder en met sleutelsplitsing) worden weergegeven in de volgende tabel.

| Parameter | Geen sleutelsplitsing | Key Splitsen |
|---|---|---|
| Maximaal aantal sleutelbytes groeperen | 1e6 | 2e6 |
| Emmertje splitsen | 6e6 | 6e6 |
| Sleutelbytes splitsen | 0 | 1e6 |
| Splitsen van keyspatie | 10 | 10 |

[!DNL Group Maximum Key Bytes] geeft de maximale hoeveelheid gebeurtenisgegevens op die voor één tracking-id kan worden verwerkt. Gegevens die deze limiet overschrijden, worden gefilterd uit het constructieproces van de gegevensset. [!DNL Split Key Bytes] vertegenwoordigt het aantal bytes waarbij één enkele het volgen identiteitskaart in veelvoudige elementen wordt gesplitst. Elementen worden bij ongeveer dit aantal bytes gesplitst op basis van een waarschijnlijkheidsverdeling. [!DNL Split Key Space Ratio] en  [!DNL Split Key Bucket Space] regelt u het geheugengebruik en de foutsnelheid van sleutelsplitsing.

>[!NOTE]
>
>[!DNL Group Maximum Key Bytes],  [!DNL Split Key Bytes],  [!DNL Split Key Space Ratio]en  [!DNL Split Key Bucket Space] alles moet worden gedeclareerd om sleutelsplitsing naar behoren te laten werken. Wijzig de waarden van deze parameters niet zonder Adobe te raadplegen.
