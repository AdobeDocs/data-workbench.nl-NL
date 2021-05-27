---
description: Met de ReplaceURI-transformatie wordt de waarde in de interne URI-dimensie gewijzigd in een nieuwe waarde.
title: ReplaceURI
uuid: f9fc6d51-6eb6-4ace-8c19-2c0200555363
exl-id: 03a6f306-5e2e-488c-8d79-a14938dcd635
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---

# ReplaceURI{#replaceuri}

Met de ReplaceURI-transformatie wordt de waarde in de interne URI-dimensie gewijzigd in een nieuwe waarde.

Als [!DNL URI Prefix] wordt gespecificeerd, is de resulterende waarde eenvoudig het voorvoegsel van URI samengevoegd met de verstrekte inputwaarde.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is. |  |
| Invoer | De waarde die de URI moet vervangen. |  |
| URI-voorvoegsel | De waarde (tekenreeks) die aan de waarde in het veld [!DNL Input] moet worden toegevoegd. |  |

>[!NOTE]
>
>Voordat u [!DNL ReplaceURI]-transformaties toepast, moet u een nieuwe, eenvoudige dimensie maken met een bovenliggend element van [!DNL Page View]uit een kopie van cs-uri-stem of cs-uri. Neem contact op met Adobe voor hulp.

In dit voorbeeld wordt het gebruik van [!DNL ReplaceURI] getoond om de querytekenreeksen &quot;page=*pageid*&quot; te vervangen door &quot; [!DNL homepage.html]&quot; wanneer *pageid* aangeeft dat de homepage van de website is weergegeven. Het eindresultaat is een gebruikersvriendelijker mening van URI.

![](assets/cfg_TransformationType_ReplaceURI.bmp)

Voor de getoonde transformatie, de pagina

* [!DNL www.examplesite.com/info.html?page=1550]

wordt gewijzigd in

* [!DNL www.examplesite.com/homepage.html]
