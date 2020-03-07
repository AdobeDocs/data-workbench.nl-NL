---
description: Gelijkaardig aan de transformatie AppendURI, beïnvloedt de transformatie PrependURI het interne gebied dat door de server van de gegevenswerkbank wordt gebruikt om de dimensie van URI te construeren.
solution: Analytics
title: PrependURI
topic: Data workbench
uuid: 3f2fb1a7-83f7-481e-b892-0937acd379f9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# PrependURI{#prependuri}

Gelijkaardig aan de transformatie AppendURI, beïnvloedt de transformatie PrependURI het interne gebied dat door de server van de gegevenswerkbank wordt gebruikt om de dimensie van URI te construeren.

De [!DNL PrependURI] transformatie werkt door de waarde op het geïdentificeerde inputgebied aan de voorzijde van de waarde momenteel in URI toe te voegen.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde om te gebruiken als aan de voorwaarde wordt voldaan en de inputwaarde niet beschikbaar is. |  |
| Invoer | De naam van het gebied de waarvan waarde aan URI wordt voorbereid. |  |

Het volgende voorbeeld stelt eenvoudig het s-dns gebied op URI voor, die de vertegenwoordiging van de dimensie van URI uitbreidt om het domein te omvatten dat door het cliëntapparaat wordt gevraagd.

![](assets/cfg_TransformationType_PrependURI.png)

In dit voorbeeld, die het s-dns- gebied aan URI vooraf instelt

* [!DNL /modelview.asp&id=login]

resulteert in volgende URL:

* [!DNL www.adobe.com/modelview.asp?id=login]

Nu wordt URI uitgebreid om het gevraagde domein te omvatten.
