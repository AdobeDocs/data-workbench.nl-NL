---
description: Instructies om de prestaties van DPU te stemmen.
title: DPU-prestatieinstellingen
uuid: e2b87548-7eb3-4f82-a94e-8ec7c3dc27c2
exl-id: 738c3a76-f8b4-4d84-86ee-ce9b99f50dae
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# DPU-prestatieinstellingen{#dpu-performance-settings}

{{eol}}

Instructies om de prestaties van DPU te stemmen.

Voltooi de volgende parameters in * [!DNL Insight Server] installatiemap*\Components\DPU.cfg bestand.

| Parameter | Beschrijving |
|---|---|
| Aantal batches voor uitvoering | Dit is een afstemmingsparameter. De standaardwaarde is 65536. U kunt willekeurig kleine aantallen van de uitvoeringspartij specificeren. Neem contact op met Adobe voordat u wijzigingen aanbrengt in deze waarde. |
| Uitvoerbatch | Dit is een afstemmingsparameter. De standaardwaarde is 128. Neem contact op met Adobe voordat u wijzigingen aanbrengt in deze waarde. |
| Uitvoeringstijd | Dit is een afstemmingsparameter. De standaardwaarde is 0,100. Neem contact op met Adobe voordat u wijzigingen aanbrengt in deze waarde. |
| Veldgrijs bij fout | Deze parameter kan worden ingesteld op true of false. Indien ingesteld op true, [!DNL Insight Server] een bestand met de naam [!DNL Field Dump number.txt] in de map Traceren wanneer fouten optreden in de uitvoeringsengine. De [!DNL Field Dump] &lt; [!DNL number]> [!DNL .txt] is nuttig voor het oplossen van problemen. |
| Profielpad | Locatie waarin bestanden voor alle profielen moeten worden opgeslagen. De standaardlocatie is Profielen. |
| Limiet voor vraaggeheugen | Hoeveelheid geheugen (in bytes) dat [!DNL Insight Server] reserves om vraagresultaten op te slaan. De standaardwaarde is 10000000 (100 MB). Als meer ruimte voor vraagresultaten wordt vereist (bijvoorbeeld, om meer gelijktijdige gebruikers toe te staan), kan het plaatsen worden verhoogd, maar u moet blijven controleren [!DNL Insight Server’s] geheugen laden. |
| Statuspad | Locatie van systeemstatusbestanden. De standaardlocatie is Status\. |
| Threads | Een afstemmingsparameter voor [!DNL Insight Server] machines met meerdere processors. In het algemeen moet deze waarde voor elk n-core systeem worden ingesteld op n. De standaardwaarde is 1. |
| Pad gebruiker | Locatie van bestanden van gemachtigde gebruikers. De standaardlocatie is Users\. |
