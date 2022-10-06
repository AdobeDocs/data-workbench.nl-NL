---
description: Met de ReplaceURI-transformatie wordt de waarde in de interne URI-dimensie gewijzigd in een nieuwe waarde.
title: ReplaceURI
uuid: f9fc6d51-6eb6-4ace-8c19-2c0200555363
exl-id: 03a6f306-5e2e-488c-8d79-a14938dcd635
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---

# ReplaceURI{#replaceuri}

{{eol}}

Met de ReplaceURI-transformatie wordt de waarde in de interne URI-dimensie gewijzigd in een nieuwe waarde.

Indien [!DNL URI Prefix] wordt opgegeven, is de resulterende waarde gewoon het URI-voorvoegsel dat met de opgegeven invoerwaarde is samengevoegd.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is. |  |
| Invoer | De waarde die de URI moet vervangen. |  |
| URI-voorvoegsel | De waarde (tekenreeks) die moet worden toegevoegd aan de waarde in het dialoogvenster [!DNL Input] veld. |  |

>[!NOTE]
>
>Voor het toepassen [!DNL ReplaceURI] transformaties, zou u een nieuwe eenvoudige afmeting met een ouder van moeten creëren [!DNL Page View]een kopie van de cs-uri-stem of cs-uri. Neem contact op met Adobe voor hulp.

In dit voorbeeld wordt het gebruik van [!DNL ReplaceURI] ter vervanging van &quot;page=*pageid*&quot; query strings met &quot; [!DNL homepage.html]&quot;telkens *pageid* Hiermee wordt aangegeven dat de website is weergegeven. Het eindresultaat is een gebruikersvriendelijker mening van URI.

![](assets/cfg_TransformationType_ReplaceURI.bmp)

Voor de getoonde transformatie, de pagina

* [!DNL www.examplesite.com/info.html?page=1550]

wordt gewijzigd in

* [!DNL www.examplesite.com/homepage.html]
