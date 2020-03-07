---
description: De functionaliteit van de transformatie (Transform) loopt op een de servermachine van de gegevenswerkbank om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.
solution: Analytics
title: Informatie over transformatiefunctionaliteit
topic: Data workbench
uuid: f797f283-025b-4fb5-a110-84a9483dccaa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Informatie over transformatiefunctionaliteit{#about-transformation-functionality}

De functionaliteit van de transformatie (Transform) loopt op een de servermachine van de gegevenswerkbank om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.

[!DNL Transform] kan [!DNL .vsl] dossiers, logboekdossiers, de dossiers van XML, en ODBC- gegevens lezen en de gegevens uitvoeren als [!DNL .vsl] dossiers, tekstdossiers, of afgebakende tekstdossiers die door het laden DataWarehouse routines, controlebureaus, of andere doelstellingen kunnen worden gebruikt. De gegevensextractie en -transformatie kan op een continue of andere geplande basis worden uitgevoerd.

>[!NOTE]
>
>Typisch, [!DNL Transform] wordt gevormd op een server FSU van de gegevenswerkbank. Nochtans, kan uw implementatie configuratie op een server DPU van de gegevenswerkbank vereisen. Voor meer informatie, contacteer Adobe.

U kunt de informatie van het geheugengebruik voor [!DNL Transform] in de Gedetailleerde interface van de Status bekijken. Voor meer informatie, zie het Administratieve hoofdstuk van Interfaces van de Gids *van de Gebruiker van de Werkbank van* Gegevens.

De eigenschap van de segmentuitvoer verstrekt een ander middel om gegevens van een toepassing van Adobe uit te voeren. [!DNL Transform] laat u toe om onverwerkte gegevens naar een extern doel uit te voeren, maar de eigenschap van de segmentuitvoer laat u aan output verwerkte gegevens van de dataset toe en vereist dat de uitgevoerde gegevens als dimensie in de dataset worden bepaald. Voor meer informatie over de segmentuitvoer, zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.
