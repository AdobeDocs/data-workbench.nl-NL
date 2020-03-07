---
description: De transformatie Tokenize past dynamisch een regelmatige uitdrukking tegen het inputkoord toe.
solution: Analytics
title: Tokeniseren
topic: Data workbench
uuid: f8430e6c-ec14-4ba6-aeae-92c9f2520a63
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Tokeniseren{#tokenize}

De transformatie Tokenize past dynamisch een regelmatige uitdrukking tegen het inputkoord toe.

Nochtans, in tegenstelling tot [!DNL RETransform], moet [!DNL Tokenize] niet het volledige koord aanpassen: de regelmatige uitdrukking die voor de [!DNL Tokenize] transformatie wordt gebruikt kan een ondergroep van de input aanpassen. Nadat een gelijke wordt gevonden, past opnieuw de regelmatige uitdrukking toe, die bij het karakter na het eind van de laatste gelijke begint. [!DNL Tokenize]

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Gevallengevoelig | Waar of vals. Specificeert of de gelijke case-sensitive is. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde om te gebruiken als de voorwaarde wordt voldaan aan en de inputwaarde of niet beschikbaar is of de regelmatige uitdrukking past niet de inputwaarde aan. |  |
| Uitdrukking | De regelmatige uitdrukking die voor aanpassing wordt gebruikt. |  |
| Resultaten | De namen van de outputkoorden. U kunt veelvoudige output voor een bepaald inputkoord hebben. Het aantal outputs moet overeenstemmen met het aantal het vangen van sub-patronen in de regelmatige uitdrukking. |  |

In het volgende voorbeeld, gebruikt de [!DNL Tokenize] transformatie een regelmatige uitdrukking om de namen van de vraagkoorden (in cs-uri-vraag) en output te vangen het gevangen sub-patroon (de vraagnaam) aan x-pull-vraag-naam.

![](assets/cfg_TransformationType_Tokenize.png)

Voor het vraagkoord &quot;a=b&amp;c=d,&quot;zou de output een vector zijn die &quot;a&quot;en &quot;c.&quot;bevat

Voor informatie over regelmatige uitdrukkingen, zie [Regelmatige Uitdrukkingen](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).
