---
description: U kunt een definitie van de Uitvoer van het Segment van de visualisatie van de Lijst van het Detail in de Cliënt van de Data Workbench gemakkelijk tot stand brengen.
title: Segment exporteren
uuid: 85c8aa72-23fe-424b-9580-6759dc8f8681
exl-id: 49998b46-f3a6-43a3-a76e-468894b27ee4
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# Segment exporteren{#segment-export}

{{eol}}

U kunt een definitie van de Uitvoer van het Segment van de visualisatie van de Lijst van het Detail in de Cliënt van de Data Workbench gemakkelijk tot stand brengen.

Daarnaast [!DNL Segment Exports] combineer automatisch hun resultaten aan één enkele server, eerder dan het veroorzaken van gedeeltelijke resultaten op elke DPU die u het gebruiken van een extern proces moet combineren. U kunt een gesegmenteerd exportbestand maken en dit opslaan in het dialoogvenster [!DNL Profile Manager]en uploadt u het uitvoerbestand naar een server van uw keuze.

**Om de server van de segmentuitvoer te vormen**

De [!DNL Segment Export] leidt tot één enkel outputdossier op de server van de segmentuitvoer, eerder dan afzonderlijke outputdossiers die op elke DPU worden gecreeerd. De segment de uitvoerserver wordt gewoonlijk gevormd om op FSU in werking te stellen.

In de map DataSet in het dialoogvenster [!DNL Profile Manager], opent u de [!DNL Segment Export.cfg] in Workstation, en specificeer het adres van uw server. (Uw adres kan een IP-adres zijn of een volledig gekwalificeerde domeinnaam.)

![](assets/segment_export_cfg.png)

Dit is IP van de server die van de Data Workbench de resultaten van de segmentuitvoer ontvangt. Dit is een eenmalige installatie. Als de [!DNL Segment Export.cfg] niet aanwezig is, wordt de uitvoer niet uitgevoerd.

**Exportmappen configureren**

Voor veiligheidsdoeleinden, moeten de uitvoerbare of partijdossiers die na een segmentuitvoer lopen in de configureerbare folder van Scripts \ van de de segmentuitvoer server verblijven.

De [!DNL .part] en de definitieve output moet in de configureerbare folder van Uitvoer verblijven. De opdracht die moet worden uitgevoerd, bestaat in opdrachtargumenten en opdrachtargumenten. Instanties van %file% in de opdrachtargumenten worden vervangen door het pad van het uitvoerbestand.

>[!NOTE]
>
>Nieuwe Data Workbench 5.4. De map \Exports wordt automatisch gemaakt. Voor eerdere exportmappen die vóór versie 5.4 waren ingesteld, was een voorvoegsel voor exporteren vereist vóór de bestandsnaam voor elk segment dat werd geëxporteerd. Het toevoegen van dit voorvoegsel is nu overbodig.

1. In [!DNL Communications.cfg] op de doelserver voor [!DNL Segment Exports], voeg een SegmentExportServer aan de lijst van servers toe. (Voorbeeld weergegeven in rood).

   ![](assets/communications_cfg_example.png)

   Exportmap: Geeft aan waar de put moet worden geplaatst [!DNL .part] en uitvoerbestanden. Dit kan een gedeelde map zijn.

   Scriptmap: Hiermee geeft u de map op waaruit alle uitvoerbare bestanden of batchbestanden worden uitgevoerd.

1. [!DNL Access Control.cfg], op de zelfde server, voeg lees-schrijf toegang tot URI /SegmentExportServer/ aan de Cluster Servers AccessGroup toe:

   ![](assets/accesscontrol_cfg_example.png)

1. Wijzig uw [!DNL .export] bestanden:

   ![](assets/segment_export_query_example.png)

1. Voor elk profiel [!DNL Segment Export.cfg] bevindt zich in de map Dataset, met de volgende inhoud:

   ```
   Segment Export = SegmentExport:
   Segment Export Server = serverInfo:
   Port = int: 80
   Address = string: 192.168.5.128 (for example) Use SSL = bool: false
   ```

1. Zorg ervoor dat de folders die in de Folder van de Uitvoer en Folder van Manuscripten worden bedoeld bestaan.

   Alleen uitvoerbare bestanden en batchbestanden in de map Scripts kunnen worden uitgevoerd als opdracht voor het exporteren van segmenten.

**Een segmentexportbestand maken**

1. Maak in een werkruimte een detailtabel met subsets van gegevens (Visualisatie > Detailtabel) en voeg kenmerken toe.
1. Maak desgewenst selecties in de werkruimte. (Alle selecties of filters worden toegepast op het exporteren.)

   ![](assets/create_segment_export_file.png)

1. Klik met de rechtermuisknop in de koptekst van de tabel Details en selecteer **[!UICONTROL Create Segment Export File]**.
1. In [!DNL Save as], typt u een naam voor de [!DNL .export] bestand.
1. Op de [!DNL .export] de parameters indien nodig configureren.

   Alle selecties of filters in de werkruimte worden opgenomen in het exportbestand.

1. Sla de [!DNL .export] bestand.

   Het opgeslagen bestand wordt weergegeven in het dialoogvenster [!DNL Profile Manager] om op te slaan op de server. Wanneer u het bestand op de server opslaat, wordt het exporteren gestart.
