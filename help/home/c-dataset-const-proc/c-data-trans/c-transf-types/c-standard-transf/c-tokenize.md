---
description: Met de transformatie Tokenize wordt een reguliere expressie op de invoertekenreeks toegepast.
title: Tokenize
uuid: f8430e6c-ec14-4ba6-aeae-92c9f2520a63
exl-id: c1f39b5b-4717-44f6-99c7-4e6a215f3542
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# Tokenize{#tokenize}

{{eol}}

Met de transformatie Tokenize wordt een reguliere expressie op de invoertekenreeks toegepast.

Anders dan [!DNL RETransform], [!DNL Tokenize] hoeft niet overeen te komen met de gehele tekenreeks: de reguliere expressie die wordt gebruikt voor de [!DNL Tokenize] transformatie kan overeenkomen met een subset van de invoer. Nadat een overeenkomst is gevonden, [!DNL Tokenize] Hiermee wordt de reguliere expressie opnieuw toegepast, te beginnen bij het teken na het einde van de laatste overeenkomst.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Hoofdlettergevoelig | Waar of onwaar. Geeft aan of de overeenkomst hoofdlettergevoelig is. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is of als de reguliere expressie niet overeenkomt met de invoerwaarde. |  |
| Uitdrukking | De reguliere expressie die wordt gebruikt voor overeenkomsten. |  |
| Uitvoer | De namen van de uitvoertekenreeksen. U kunt voor een bepaalde invoertekenreeks meerdere uitvoerbestanden gebruiken. Het aantal uitvoerbestanden moet overeenkomen met het aantal vastgelegde subpatronen in de reguliere expressie. |  |

In het volgende voorbeeld wordt [!DNL Tokenize] transformatie gebruikt een reguliere expressie om de namen van de querytekenreeksen vast te leggen (in cs-uri-query) en het vastgelegde subpatroon (de naam van de query) uit te voeren naar x-pull-query-name.

![](assets/cfg_TransformationType_Tokenize.png)

Voor de querytekenreeks &quot;a=b&amp;c=d&quot; zou de uitvoer een vector zijn die &quot;a&quot; en &quot;c&quot; bevat.

Voor informatie over reguliere expressies raadpleegt u [Reguliere expressies](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).
