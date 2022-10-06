---
description: Een rapportreeks is een inzameling van werkruimten die de Server van het Rapport produceert gebaseerd op de waarden die in een Report.cfg- configuratiedossier worden gespecificeerd.
title: Rapportsets begrijpen
uuid: 421055d7-0cf0-4664-b944-327a254a97a4
exl-id: 95609a1a-e70c-41e2-ace3-0cb09f77705a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Rapportsets begrijpen{#understanding-report-sets}

{{eol}}

Een rapportreeks is een inzameling van werkruimten die de Server van het Rapport produceert gebaseerd op de waarden die in een Report.cfg- configuratiedossier worden gespecificeerd.

In uw [!DNL Insight] installatiemap, elke submap in de &lt;*naam van werkprofiel* De map >\Reports vertegenwoordigt een set rapporten die is gemaakt. Elke rapportset heeft een eigen [!DNL Report.cfg] configuratiebestand in die submap.

>[!NOTE]
>
>In de [!DNL Profile Manager] in Data Workbench, rapportreeksen verschijnen als subfolders binnen [!DNL Reports] map. Voor meer informatie over de [!DNL Profile Manager], zie de [Gebruikershandleiding voor Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/home.html#Data_Workbench_Help).

Door specifieke configuratiemontages voor een rapportreeks in zijn te bepalen [!DNL Report.cfg] kunt u de aanmaak en distributie van de rapporten plannen, inclusief wie welke rapporten ontvangt en in welke indelingen.
