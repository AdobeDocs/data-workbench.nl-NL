---
description: Transformatiefunctionaliteit (Transform) wordt uitgevoerd op een computer met een gegevenswerkbankserver om het exporteren van logbrongegevens voor gebruik door andere toepassingen mogelijk te maken.
title: Informatie over transformatiefunctionaliteit
uuid: f797f283-025b-4fb5-a110-84a9483dccaa
exl-id: db5d6329-407d-43f3-92fc-1b40f7289916
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Informatie over transformatiefunctionaliteit{#about-transformation-functionality}

{{eol}}

Transformatiefunctionaliteit (Transform) wordt uitgevoerd op een computer met een gegevenswerkbankserver om het exporteren van logbrongegevens voor gebruik door andere toepassingen mogelijk te maken.

[!DNL Transform] kan lezen [!DNL .vsl] bestanden, logbestanden, XML-bestanden en ODBC-gegevens en exporteer de gegevens als [!DNL .vsl] bestanden, tekstbestanden of tekstbestanden met scheidingstekens die kunnen worden gebruikt door DataWarehouse-laadroutines, auditbureaus of andere doelen. De gegevensextractie en -transformatie kunnen doorlopend of op een andere geplande basis worden uitgevoerd.

>[!NOTE]
>
>Doorgaans [!DNL Transform] is geconfigureerd op een gegevenswerkbankserver-FSU. Nochtans, kan uw implementatie configuratie op een serverDPU van de gegevenswerkbank vereisen. Neem voor meer informatie contact op met Adobe.

U kunt informatie over geheugengebruik weergeven voor [!DNL Transform] in de gedetailleerde interface van de Status. Raadpleeg het hoofdstuk Administratieve interfaces van het dialoogvenster *Gebruikershandleiding voor Data Workbench*.

De functie voor segmentexport biedt een andere manier om gegevens uit een Adobe-toepassing te exporteren. [!DNL Transform] laat u toe om onverwerkte gegevens naar een extern doel uit te voeren, maar de eigenschap van de segmentuitvoer laat u toe om verwerkte gegevens van de dataset uit te voeren en vereist dat de uitgevoerde gegevens als dimensie in de dataset worden bepaald. Voor meer informatie over de segmentuitvoer raadpleegt u de *Gebruikershandleiding voor Data Workbench*.
