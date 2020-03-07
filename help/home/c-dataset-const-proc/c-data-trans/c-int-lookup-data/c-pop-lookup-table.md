---
description: Als u de transformaties Categoriseert of FlatFileLookup gebruikt, wordt de raadplegingslijst geladen in geheugen en bevolkt van een vlak dossier de waarvan plaats u specificeert wanneer u de transformatie bepaalt.
solution: Analytics
title: Het bevolken van de Lijst van de Raadpleging
topic: Data workbench
uuid: a11f3902-8853-4d22-bbfd-b2a3d143cb7b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het bevolken van de Lijst van de Raadpleging{#populating-the-lookup-table}

Als u de transformaties Categoriseert of FlatFileLookup gebruikt, wordt de raadplegingslijst geladen in geheugen en bevolkt van een vlak dossier de waarvan plaats u specificeert wanneer u de transformatie bepaalt.

Het vlakke dossier u specificeert moet aan de volgende vereisten voldoen:

* Elke lijn in het dossier moet een rij in de raadplegingslijst vertegenwoordigen.
* De kolommen in het dossier moeten door een afbakening van ASCII worden gescheiden. U kunt om het even welk karakter gebruiken dat geen lijn-beëindigend karakter is en niet overal binnen de gebeurtenisgegevens zelf verschijnt. Wanneer u de transformatie bepaalt, specificeert u welk karakter is gebruikt om de kolommen in het vlakke dossier te afbakenen.

Als u een [!DNL ODBCLookup] transformatie gebruikt, wordt de raadplegingslijst geladen in geheugen en bevolkt van een lijst of een mening in een [!DNL ODBC] gegevensbestand dat u specificeert. Wanneer u de transformatie bepaalt, moet u de gegevensbron, de gebruikersnaam, en het wachtwoord ook specificeren dat de server van de gegevenswerkbank moet gebruiken om een verbinding aan het gegevensbestand te vestigen.

>[!NOTE]
>
>De lijsten van de Raadpleging worden geladen wanneer de server van de gegevenswerkbank aanvankelijk begint construerend de dataset. Zodra gevestigd, zijn de raadplegingsdossiers niet bedoeld om worden veranderd. Als u het vlakke dossier of de [!DNL ODBC] lijst verandert dat voor de transformatiefase wordt gebruikt, moet u de volledige dataset retransform. Als u een vlak dossier verandert dat tijdens de fase van de logboekverwerking wordt gebruikt, wordt het nieuwe raadplegingsgegeven toegepast op alle nieuwe verslagen die de dataset ingaan, maar de veranderingen worden niet retroactief toegepast.

