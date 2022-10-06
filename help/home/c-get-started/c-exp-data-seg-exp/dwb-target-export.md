---
description: De gegevens van de Data Workbench van de uitvoer naar Adobe Target gebruikend TargetBulkUpload.exe van de Lijst van het Detail.
title: Exporteren naar Adobe Target
uuid: 0eb99e6f-f0b5-495e-a3b6-df30f61378a7
exl-id: 41e885bb-182a-4983-98e8-65eec1da9fe9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Exporteren naar Adobe Target{#export-to-adobe-target}

{{eol}}

De gegevens van de Data Workbench van de uitvoer naar Adobe Target gebruikend TargetBulkUpload.exe van de Lijst van het Detail.

Met Data Workbench kunt u bestanden exporteren en integreren met Adobe Target als onderdeel van een geïntegreerde Adobe Experience Cloud.

De **[!DNL TargetBulkUpload]** bestand is gevonden in het dialoogvenster *Server\Scripts* in de serverinstallatiebestanden. Het uitvoerbare bestand heeft een logica voor opnieuw proberen en aanvullende logica voor het optimaliseren van de prestaties.

U kunt de `TargetBulkUpload.cfg` bestand en verplaatsen naar *Server/beheerder/export* map voordat het uploadscript wordt uitgevoerd. U kunt bijvoorbeeld een max. time-outinterval instellen op 720 minuten (standaard) om een time-out in te stellen voor de upload na de opgegeven periode.

**Hoe werkt het**

Nadat de gegevens naar Target zijn verzonden, wordt de status van de upload voortdurend gecontroleerd. Als het uploaden slaagt, wordt een succesbericht geregistreerd. Als het uploaden mislukt of in behandeling is, gaat de controle verder. U kunt het timeout interval configureren in het dialoogvenster `TargetBulkUpload.cfg` bestand. Als het uploaden bij Doel vastloopt, wordt een bericht geregistreerd en kan de status nog steeds worden gecontroleerd.

Er worden twee logbestanden gegenereerd in de tracering voor de geactiveerde export onder [!DNL /server/Trace/]:

* `targetbulkuploadexportname.log`
* `targetbulkuploadexportname.log.completed`

De `targetbulkuploadexportname.log` bestand heeft de gedetailleerde status voor alle records van meerdere batches, de Edge-server waarnaar deze gaan en de status (geslaagd, mislukt, profiel niet gevonden, status onbekend en geplakt). Indien wordt vastgesteld dat een partij vast zit, wordt de partij niet verder verwerkt. Er is een vastgezette batch-URL beschikbaar om de status bij te houden. Zie de volgende voorbeeldgegevens van de `targetbulkuploadexportname.log.completed` bestand:

```
1205057 total rows 
568740 successful 
62 failed 
28964 profile not found 
112169 unknown status 
492339 stuck status
```

De waarde voor de status &#39;plak&#39; wordt verhoogd met de totale omvang van de geplakte batch, ongeacht het aantal uploads dat is gelukt of mislukt. De totale rijwaarde wordt ook verhoogd met hetzelfde aantal geplakte batch-grootten.

>[!NOTE]
>
>Eerder werden DWB-gegevens geëxporteerd met de [!DNL ExportIntegration.exe]. Momenteel worden slechts de uitvoer MMP, CRS, en S/FTP gebruikt met dit uitvoerbare dossier. Adobe Target-integratie gebruikt nu de [!DNL TargetBulkUpload.exe] in de Data Workbench.
