---
description: Met de transformatie Tokenize wordt een reguliere expressie op de invoertekenreeks toegepast.
title: Tokenize
uuid: f8430e6c-ec14-4ba6-aeae-92c9f2520a63
exl-id: c1f39b5b-4717-44f6-99c7-4e6a215f3542
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# Tokenize{#tokenize}

Met de transformatie Tokenize wordt een reguliere expressie op de invoertekenreeks toegepast.

In tegenstelling tot [!DNL RETransform] hoeft [!DNL Tokenize] echter niet de gehele tekenreeks aan te passen: De reguliere expressie die voor de transformatie [!DNL Tokenize] wordt gebruikt, kan overeenkomen met een subset van de invoer. Nadat een overeenkomst wordt gevonden, [!DNL Tokenize] past opnieuw de regelmatige uitdrukking toe, die bij het karakter na het eind van de laatste gelijke begint.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Hoofdlettergevoelig | Waar of onwaar. Geeft aan of de overeenkomst hoofdlettergevoelig is. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is of als de reguliere expressie niet overeenkomt met de invoerwaarde. |  |
| Uitdrukking | De reguliere expressie die wordt gebruikt voor overeenkomsten. |  |
| Uitvoer | De namen van de uitvoertekenreeksen. U kunt voor een bepaalde invoertekenreeks meerdere uitvoerbestanden gebruiken. Het aantal uitvoerbestanden moet overeenkomen met het aantal vastgelegde subpatronen in de reguliere expressie. |  |

In het volgende voorbeeld gebruikt de transformatie [!DNL Tokenize] een reguliere expressie om de namen van de querytekenreeksen (in cs-uri-query) vast te leggen en het vastgelegde subpatroon (de naam van de query) uit te voeren naar x-pull-query-name.

![](assets/cfg_TransformationType_Tokenize.png)

Voor de querytekenreeks &quot;a=b&amp;c=d&quot; zou de uitvoer een vector zijn die &quot;a&quot; en &quot;c&quot; bevat.

Zie [Reguliere expressies](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c) voor informatie over reguliere expressies.
