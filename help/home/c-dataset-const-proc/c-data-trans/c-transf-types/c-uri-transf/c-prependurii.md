---
description: Net als bij de AppendURI-transformatie beïnvloedt de PrependURI-transformatie het interne veld dat door de gegevenswerkbench-server wordt gebruikt om de URI-dimensie te maken.
title: PrependURI
uuid: 3f2fb1a7-83f7-481e-b892-0937acd379f9
exl-id: c39d9241-ed66-446e-b59d-fdb11942d0e8
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---

# PrependURI{#prependuri}

Net als bij de AppendURI-transformatie beïnvloedt de PrependURI-transformatie het interne veld dat door de gegevenswerkbench-server wordt gebruikt om de URI-dimensie te maken.

De transformatie [!DNL PrependURI] werkt door de waarde in het geïdentificeerde inputgebied aan de voorzijde van de waarde momenteel in URI toe te voegen.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is. |  |
| Invoer | De naam van het veld waarvan de waarde aan de URI wordt toegevoegd. |  |

In het volgende voorbeeld wordt het veld s-dns eenvoudig toegevoegd aan de URI, waarbij de representatie van de URI-dimensie wordt uitgebreid met het domein dat door het clientapparaat wordt aangevraagd.

![](assets/cfg_TransformationType_PrependURI.png)

In dit voorbeeld wordt het veld s-dns vooraf ingesteld op de URI

* [!DNL /modelview.asp&id=login]

resulteert in de volgende URL:

* [!DNL www.adobe.com/modelview.asp?id=login]

Nu wordt URI uitgebreid om het gevraagde domein te omvatten.
