---
description: Het groeperen van de bezoeker laat u hefboomwerkings klantenkenmerken om bezoekers dynamisch te categoriseren en clusterreeksen te produceren die op geselecteerde gegevensinput worden gebaseerd, waarbij groepen worden geïdentificeerd die gelijkaardige belangen en gedrag voor klantenanalyse en het richten hebben.
solution: Analytics
title: Bezoekersclustering
topic: Data workbench
uuid: 0c16aaa0-1d86-43a6-a7e2-b43b3ea80dc5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bezoekersclustering{#visitor-clustering}

Het groeperen van de bezoeker laat u hefboomwerkings klantenkenmerken om bezoekers dynamisch te categoriseren en clusterreeksen te produceren die op geselecteerde gegevensinput worden gebaseerd, waarbij groepen worden geïdentificeerd die gelijkaardige belangen en gedrag voor klantenanalyse en het richten hebben.

**Clusterproces**

Het het groeperen proces vereist u om metriek en afmetingselementen te identificeren als input te gebruiken, en staat u toe om een specifieke doelpopulatie te kiezen om deze elementen toe te passen om gespecificeerde clusters tot stand te brengen. Wanneer u het het groeperen proces in werking stelt, gebruikt het systeem metrische en afmetrische input om aangewezen aanvankelijke centra voor het gespecificeerde aantal clusters te bepalen. Deze centra worden dan gebruikt als uitgangspunt om het K-Means algoritme toe te passen.

![](assets/K_algorithm.png)

* De eerste centra worden intelligent gekozen via een Canopy Clustering pass.
* De clusters van gegevens worden gecreeerd door elk gegevenspunt aan het meest dichtbijgelegen centrum te associëren.
* Het gemiddelde van elk van de K-clusters wordt het nieuwe centrum.
* Het algoritme wordt herhaald in stappen 2 en 3 tot de convergentie wordt bereikt. Dit kan veelvoudig passeren.

Het **[!UICONTROL Maximum Iterations]** in het **[!UICONTROL Options]** menu staat de analist toe om het maximumaantal herhalingen te specificeren die door het het groeperen algoritme moeten worden uitgevoerd. Het plaatsen van deze optie kan in snellere voltooiing van het zich groeperende proces resulteren dat op het maximum van herhalingen wordt gebaseerd ten koste van nauwkeurige convergentie van de clustercentra.

>[!NOTE]
>
>Zodra de clusters zijn gedefinieerd, kan de clusterdimensie worden opgeslagen voor gebruik, net als elke andere dimensie. Het kan ook in de Ontdekkingsreiziger van de Cluster worden geladen om de scheiding van clustercentra te onderzoeken.

In de Bouwer van de Cluster, kunt u **[!UICONTROL Options]** > selecteren **[!UICONTROL Algorithm]** om algoritmen te selecteren wanneer het bepalen van clusters. Momenteel, zijn er 3 gesteunde algoritmen:

* KMeans
* Kant`++`
* Maximalisering van verwachtingen

Er zijn 2 manieren om het groeperende proces in werking te stellen:

* Methode 1 - klik **[!UICONTROL Go]** in het venster van de clustervisualisatie.
* Methode 2 - klik **[!UICONTROL Submit]** in het venster van de clustervisualisatie, dat direct de het groeperen baan naar de Server verzendt. U kunt de vooruitgang door de &quot;Gedetailleerde Status voor Vraag&quot;optie volgen.

![](assets/dwb_visitorclustering.png)

Het algoritme heeft de volgende beperkingen:

1. Als u Methode 1 gebruikt, kunt u om het even welke gesteunde het groeperen zich algoritmen selecteren.
1. Als u Methode 2 gebruikt, kunt u gemiddelden of gemiddelden++ selecteren. De optie voor maximalisatie van verwachtingen is niet beschikbaar.

>[!NOTE]
>
>In het [!DNL DPU.cfg] dossier, wordt de waarde voor &quot;Vraag, de Grens van het Geheugen&quot;geplaatst aan 500 MB door gebrek. Deze waarde moet worden verhoogd terwijl het runnen van veelvoudige het groeperen van banen. Bijvoorbeeld, als u 5 het groeperen van banen in parallel in werking stelt, verhoog deze waarde tot 1 GB. Er is geen manier om de groeperende baan te annuleren zonder de Server opnieuw te beginnen.

**Aanbevelingen**

Het aantal herhalingen (aantal keer wordt het gegeven afgetast) en de convergentiedrempel dat u vormt, beïnvloedt grosso modo de het groeperen prestaties. De volgende lijst verstrekt een bredere richtlijn die u kunt volgen:

| Aantal clusters | Algoritme | Interferenties | Convergentiedrempel | Normalisatie |
|---|---|---|---|---|
| 6 | Kant | 25,50 | 1e-3 | Min-Max |
| 6 | Kant | 25,50 | 1e-6 | Min-Max |
| 6 | Midden++ | 50 | 1e-6 | Min-Max |
