---
description: De gegevens van de Werkbank van de Gegevens van de uitvoer naar het Doel van Adobe gebruikend TargetBulkUpload.exe van de Lijst van het Detail.
title: Exporteren naar Adobe Target
uuid: 0eb99e6f-f0b5-495e-a3b6-df30f61378a7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Exporteren naar Adobe Target{#export-to-adobe-target}

De gegevens van de Werkbank van de Gegevens van de uitvoer naar het Doel van Adobe gebruikend TargetBulkUpload.exe van de Lijst van het Detail.

De Werkbank van gegevens laat u dossiers uitvoeren om met het Doel van Adobe als deel van een geïntegreerde Wolk van de Ervaring van Adobe te integreren.

Het **[!DNL TargetBulkUpload]** dossier wordt gevonden in de omslag van Manuscripten *van de* Server \ in de dossiers van de serverinstallatie. Uitvoerbaar heeft retry logica, evenals extra logica om prestaties te optimaliseren.

U kunt het `TargetBulkUpload.cfg` dossier wijzigen en het verplaatsen naar de omslag van de *Server/Admin/van de Uitvoer* alvorens in werking te stellen uploadt manuscript. Bijvoorbeeld, kunt u een Maximum Interval van de Onderbreking aan 720 minuten (gebrek) plaatsen om uit te onderbreken upload na de gespecificeerde periode.

**Hoe werkt het?**

Nadat de gegevens met succes naar Doel worden verzonden, wordt de status van upload onophoudelijk gecontroleerd. Als upload slaagt, wordt een succesbericht geregistreerd. Als upload ontbreekt of hangend is, gaat de controle verder. U kunt het onderbrekingsinterval in het `TargetBulkUpload.cfg` dossier vormen. Als upload vast bij Doel wordt, wordt een bericht geregistreerd en de status kan nog worden gecontroleerd.

Er zijn twee logboekdossiers die in het spoor voor de teweeggebrachte uitvoer onder worden geproduceerd [!DNL /server/Trace/]:

* `targetbulkuploadexportname.log`
* `targetbulkuploadexportname.log.completed`

Het `targetbulkuploadexportname.log` dossier heeft de gedetailleerde status voor alle verslagen van veelvoudige partijen, de randserver die zij gaan, en de status (succesvol, ontbroken, gevonden niet profiel, onbekende status, en geplakt) gaan. Indien wordt vastgesteld dat een partij vast zit, wordt de partij niet verder verwerkt. Een geplakte partij URL is beschikbaar om de status te volgen. Zie de volgende voorbeeldgegevens van het `targetbulkuploadexportname.log.completed` dossier:

```
1205057 total rows 
568740 successful 
62 failed 
28964 profile not found 
112169 unknown status 
492339 stuck status
```

De geplakte statuswaarde wordt verhoogd met de totale geplakte partijgrootte ongeacht hoeveel uploads succesvol of ontbroken zijn. De totale rijenwaarde wordt ook verhoogd door het zelfde aantal geplakt partijgrootte.

>[!NOTE]
>
>Eerder, werden de gegevens DWB uitgevoerd gebruikend [!DNL ExportIntegration.exe]. Momenteel slechts worden MMP, CRS, en de uitvoer S/FTP gebruikt met dit uitvoerbaar. De integratie van het Doel van Adobe gebruikt nu [!DNL TargetBulkUpload.exe] in de Werkbank van Gegevens.

