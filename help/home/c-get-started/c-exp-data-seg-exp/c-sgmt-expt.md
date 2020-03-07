---
description: U kunt een definitie van de Uitvoer van het Segment van de visualisatie van de Lijst van het Detail in de Cliënt van de Werkbank van Gegevens gemakkelijk tot stand brengen.
solution: Analytics
title: Uitvoer segment
topic: Data workbench
uuid: 85c8aa72-23fe-424b-9580-6759dc8f8681
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Uitvoer segment{#segment-export}

U kunt een definitie van de Uitvoer van het Segment van de visualisatie van de Lijst van het Detail in de Cliënt van de Werkbank van Gegevens gemakkelijk tot stand brengen.

Bovendien combineren [!DNL Segment Exports] automatisch hun resultaten aan één enkele server, eerder dan het veroorzaken van gedeeltelijke resultaten op elke DPU die u het gebruiken van een extern proces moet combineren. U kunt een dossier van de segmentuitvoer tot stand brengen, bewaart het aan, [!DNL Profile Manager]en uploadt het outputdossier aan een server van uw keus.

**Om de server van de segmentuitvoer te vormen**

De [!DNL Segment Export] eigenschap leidt tot één enkel outputdossier op de server van de segmentuitvoer, eerder dan afzonderlijke outputdossiers die op elke DPU worden gecreeerd. De server van de segmentuitvoer wordt gewoonlijk gevormd om op FSU te lopen.

In de folder van de Dataset \ in [!DNL Profile Manager], open [!DNL Segment Export.cfg] in Werkstation, en specificeer het adres van uw server. (Uw adres zou IP kunnen zijn of volledig - gekwalificeerde domeinnaam.):

![](assets/segment_export_cfg.png)

Dit is IP van de server van de Werkbank van Gegevens die de resultaten van de segmentuitvoer ontvangt. Dit is een eenmalige installatie. Als de uitvoer niet aanwezig [!DNL Segment Export.cfg] is, loopt de uitvoer niet.

**Om de uitvoerfolders te vormen**

Voor veiligheidsdoeleinden, moeten de uitvoerbare lijsten of de partijdossiers die na een segmentuitvoer lopen in de configureerbare folder van Manuscripten \ van de server van de segmentuitvoer verblijven.

De [!DNL .part] en definitieve output moet in de configureerbare folder van Uitvoer verblijven. Het te lopen bevel bestaat in de Argumenten van het Bevel en van het Bevel. De instanties van %file% in de Argumenten van het Bevel zullen met de weg van het outputdossier worden vervangen.

>[!NOTE]
>
>Nieuw aan Werkbank 5.4 van Gegevens, wordt de omslag van de Uitvoer \ automatisch gecreeerd. De vorige de folderopstelling van de uitvoer vóór versie 5.4 vereiste een prefix van de Uitvoer \ vóór filename voor elke segmentuitvoer. Het toevoegen van deze prefix is nu overtollig.

1. In [!DNL Communications.cfg] op de bestemmingsserver voor [!DNL Segment Exports], voeg een SegmentExportServer aan de lijst van servers toe. (Voorbeeld in rood).

   ![](assets/communications_cfg_example.png)

   Exportmap: Specificeert waar te te zetten [!DNL .part] en outputdossiers. Dit kan een gedeelde folder zijn.

   Scripts Directory: Specificeert de folder van waar alle uitvoerbare of partijdossiers in werking worden gesteld.

1. [!DNL Access Control.cfg], op de zelfde server, voeg read-write toegang tot URI /SegmentExportServer/ aan de Server AccessGroup van de Servers van de Cluster toe:

   ![](assets/accesscontrol_cfg_example.png)

1. Je [!DNL .export] bestanden wijzigen:

   ![](assets/segment_export_query_example.png)

1. Voor elk profiel, [!DNL Segment Export.cfg] wordt het gevestigd in de folder Dataset \, met de volgende inhoud:

   ```
   Segment Export = SegmentExport:
   Segment Export Server = serverInfo:
   Port = int: 80
   Address = string: 192.168.5.128 (for example) Use SSL = bool: false
   ```

1. Zorg ervoor dat de folders die in de Folder van de Uitvoer en de Folder van Manuscripten worden bedoeld bestaan.

   Slechts kunnen uitvoerbare lijsten en partijdossiers in de folder van Manuscripten als bevel van de segmentuitvoer worden in werking gesteld.

**Om een dossier van de segmentuitvoer te creëren**

1. In een werkruimte, creeer een Lijst die van het Detail ondergroepen van gegevens (Visualisatie > de Lijst van het Detail) toont en voeg attributen toe.
1. Indien gewenst, maak selecties in de werkruimte. (Om het even welke selecties of filters worden toegepast op de uitvoer.)

   ![](assets/create_segment_export_file.png)

1. In de kopbal van de Lijst van het Detail, klik en selecteer met de rechtermuisknop aan **[!UICONTROL Create Segment Export File]**.
1. In, typ [!DNL Save as]een naam voor het [!DNL .export] dossier.
1. Voor het [!DNL .export] dossier, vorm zonodig de parameters.

   Om het even welke selecties of filters in de werkruimte worden opgenomen in het de uitvoerdossier.

1. Sla het [!DNL .export] bestand op.

   Het opgeslagen dossier toont in [!DNL Profile Manager] voor u om aan de server op te slaan. Wanneer u sparen het dossier aan de server, de uitvoer begint.

