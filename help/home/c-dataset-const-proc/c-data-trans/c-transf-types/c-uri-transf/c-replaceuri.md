---
description: De transformatie ReplaceURI verandert de waarde in de interne dimensie van URI in een nieuwe waarde.
solution: Analytics
title: VervangenURI
topic: Data workbench
uuid: f9fc6d51-6eb6-4ace-8c19-2c0200555363
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# VervangenURI{#replaceuri}

De transformatie ReplaceURI verandert de waarde in de interne dimensie van URI in een nieuwe waarde.

Als [!DNL URI Prefix] wordt gespecificeerd, is de resulterende waarde eenvoudig de prefix van URI die met de verstrekte inputwaarde wordt aaneengeschakeld.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde om te gebruiken als aan de voorwaarde wordt voldaan en de inputwaarde niet beschikbaar is. |  |
| Invoer | De waarde om URI te vervangen. |  |
| URI-voorvoegsel | De waarde (koord) die aan de waarde op het [!DNL Input] gebied moet worden voorgespannen. |  |

>[!NOTE]
>
>Alvorens [!DNL ReplaceURI] transformaties toe te passen, zou u een nieuwe eenvoudige afmeting met een ouder van [!DNL Page View]een exemplaar van cs-uri-stem of cs-uri-uri moeten tot stand brengen. Voor hulp met dit, contacteer Adobe.

Dit voorbeeld toont het gebruik van aan [!DNL ReplaceURI] om de &quot;page=*pageid*&quot;vraagkoorden met &quot; [!DNL homepage.html]&quot;te vervangen wanneer *pageid* erop wijst dat de homepage van de website werd bekeken. Het eindresultaat is een gebruikersvriendelijker mening van URI.

![](assets/cfg_TransformationType_ReplaceURI.bmp)

Voor de getoonde transformatie, de pagina

* [!DNL www.examplesite.com/info.html?page=1550]

wordt gewijzigd in

* [!DNL www.examplesite.com/homepage.html]

