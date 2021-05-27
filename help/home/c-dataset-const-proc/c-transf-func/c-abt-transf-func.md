---
description: Transformatiefunctionaliteit (Transform) wordt uitgevoerd op een computer met een gegevenswerkbankserver om het exporteren van logbrongegevens voor gebruik door andere toepassingen mogelijk te maken.
title: Informatie over transformatiefunctionaliteit
uuid: f797f283-025b-4fb5-a110-84a9483dccaa
exl-id: db5d6329-407d-43f3-92fc-1b40f7289916
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Info over Transformatiefunctionaliteit{#about-transformation-functionality}

Transformatiefunctionaliteit (Transform) wordt uitgevoerd op een computer met een gegevenswerkbankserver om het exporteren van logbrongegevens voor gebruik door andere toepassingen mogelijk te maken.

[!DNL Transform] U kunt  [!DNL .vsl] bestanden, logbestanden, XML-bestanden en ODBC-gegevens lezen en de gegevens exporteren als  [!DNL .vsl] bestanden, tekstbestanden of tekstbestanden met scheidingstekens die kunnen worden gebruikt door routines voor het laden van DataWarehouse, controlebureaus of andere doelen. De gegevensextractie en -transformatie kunnen doorlopend of op een andere geplande basis worden uitgevoerd.

>[!NOTE]
>
>[!DNL Transform] is doorgaans geconfigureerd op een gegevenswerkbankserver FSU. Nochtans, kan uw implementatie configuratie op een serverDPU van de gegevenswerkbank vereisen. Neem voor meer informatie contact op met Adobe.

U kunt informatie over geheugengebruik voor [!DNL Transform] in de Gedetailleerde interface van de Status bekijken. Voor meer informatie, zie het Administratieve hoofdstuk van Interfaces van *de Gids van de Gebruiker van de Data Workbench*.

De functie voor segmentexport biedt een andere manier om gegevens uit een Adobe-toepassing te exporteren. [!DNL Transform] laat u toe om onverwerkte gegevens naar een extern doel uit te voeren, maar de eigenschap van de segmentuitvoer laat u toe om verwerkte gegevens van de dataset uit te voeren en vereist dat de uitgevoerde gegevens als dimensie in de dataset worden bepaald. Voor meer informatie over segmentuitvoer, zie *de Gids van de Gebruiker van de Data Workbench*.
