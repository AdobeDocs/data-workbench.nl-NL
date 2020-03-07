---
description: Instructies om prestaties te stemmen DPU.
solution: Insight
title: Instellingen voor DPU-prestaties
uuid: e2b87548-7eb3-4f82-a94e-8ec7c3dc27c2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Instellingen voor DPU-prestaties{#dpu-performance-settings}

Instructies om prestaties te stemmen DPU.

Voltooi de volgende parameters in het * [!DNL Insight Server] installatiefolder*\Components\DPU.cfg- dossier.

| Parameter | Beschrijving |
|---|---|
| Aantal batterijen uitvoeren | Dit is een het stemmen parameter. De standaardwaarde is 65536. U kunt willekeurig kleine aantallen van de uitvoeringspartij specificeren. Tevreden om Adobe te contacteren alvorens om het even welke veranderingen in deze waarde aan te brengen. |
| Batches uitvoeren | Dit is een het stemmen parameter. De standaardwaarde is 128. Tevreden om Adobe te contacteren alvorens om het even welke veranderingen in deze waarde aan te brengen. |
| Uitvoeringstijd | Dit is een het stemmen parameter. De standaardwaarde is 0.100. Tevreden om Adobe te contacteren alvorens om het even welke veranderingen in deze waarde aan te brengen. |
| Veldpomp bij fout | Deze parameter kan aan waar of vals worden geplaatst. Als de reeks aan waar, [!DNL Insight Server] tot een dossier leidt dat [!DNL Field Dump number.txt] in zijn folder van het Spoor wordt genoemd wanneer de fouten van de uitvoeringsmotor voorkomen. De [!DNL Field Dump] &lt; [!DNL number]> [!DNL .txt] is handig voor het oplossen van problemen. |
| Profielpad | Plaats waarin u bestanden voor alle profielen wilt opslaan. De standaardlocatie is Profielen\. |
| Zoekgeheugenlimiet | Hoeveelheid geheugen (in bytes) dat [!DNL Insight Server] reserveert om vraagresultaten op te slaan. De standaardwaarde is 10000000 (100 MB.) Als meer ruimte voor vraagresultaten wordt vereist (bijvoorbeeld, om meer gelijktijdige gebruikers toe te staan), kan het plaatsen worden verhoogd, maar u moet de [!DNL Insight Server’s] geheugenlading blijven controleren. |
| State Path | Plaats van systeemstatusbestanden. De standaardlocatie is Status\. |
| Draad | Een afstelling van prestaties voor [!DNL Insight Server] machines met meerdere processors. In het algemeen, voor om het even welk n-kernsysteem, zou deze waarde aan n moeten worden geplaatst. De standaardwaarde is 1. |
| Gebruikerspad | Locatie van bestanden van geautoriseerde gebruikers. De standaardlocatie is Gebruikers\. |

