---
description: Als u de transformaties Categoriseren of FlatFileLookup gebruikt, wordt de raadplegingstabel geladen in het geheugen en bevolkt van een vlak dossier waarvan plaats u specificeert wanneer u de transformatie bepaalt.
title: De opzoektabel vullen
uuid: a11f3902-8853-4d22-bbfd-b2a3d143cb7b
exl-id: e83d9feb-44fe-4fa1-b559-e1f5606637b5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# De opzoektabel vullen{#populating-the-lookup-table}

{{eol}}

Als u de transformaties Categoriseren of FlatFileLookup gebruikt, wordt de raadplegingstabel geladen in het geheugen en bevolkt van een vlak dossier waarvan plaats u specificeert wanneer u de transformatie bepaalt.

Het platte bestand dat u opgeeft, moet aan de volgende vereisten voldoen:

* Elke regel in het bestand moet een rij in de opzoektabel vertegenwoordigen.
* Kolommen in het bestand moeten worden gescheiden door een ASCII-scheidingsteken. U kunt elk teken gebruiken dat geen regeleindeteken is en dat nergens in de gebeurtenisgegevens zelf wordt weergegeven. Wanneer u de transformatie definieert, geeft u op met welk teken de kolommen in het platte bestand zijn afgebakend.

Als u een [!DNL ODBCLookup] transformatie, wordt de raadplegingslijst geladen in geheugen en bevolkt van een lijst of een mening in [!DNL ODBC] database die u opgeeft. Wanneer u de transformatie definieert, moet u ook de gegevensbron, gebruikersnaam en wachtwoord opgeven die de gegevenswerkbankserver moet gebruiken om een verbinding met de database tot stand te brengen.

>[!NOTE]
>
>De lijsten van de opzoeklijst worden geladen wanneer de server van de gegevenswerkbank aanvankelijk begint de dataset te construeren. Zodra vastgesteld, moeten de raadplegingsdossiers niet worden veranderd. Als u het platte bestand wijzigt of [!DNL ODBC] lijst die voor de transformatiefase wordt gebruikt, wordt u vereist om de volledige dataset opnieuw om te zetten. Als u een vlak dossier verandert dat tijdens de fase van de logboekverwerking wordt gebruikt, worden de nieuwe raadplegingsgegevens toegepast op alle nieuwe verslagen die de dataset ingaan, maar de veranderingen worden niet met terugwerkende kracht toegepast.
