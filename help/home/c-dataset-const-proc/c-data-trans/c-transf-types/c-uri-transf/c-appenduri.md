---
description: De transformatie AppendURI verstrekt een manier om informatie aan de standaardwaarde toe te voegen die uit de logboekingangen komt die worden gebruikt om de dataset te bouwen.
title: AppendURI
uuid: 8334d4f9-2bf6-4bd0-af65-8f2b0959652d
exl-id: 0d5901c0-bd13-4499-8e26-44839aeb7413
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 0%

---

# AppendURI{#appenduri}

{{eol}}

De transformatie AppendURI verstrekt een manier om informatie aan de standaardwaarde toe te voegen die uit de logboekingangen komt die worden gebruikt om de dataset te bouwen.

De transformatie plaatst een naam-waardepaar aan het einde van het interne veld dat wordt gebruikt om de URI-dimensie te maken. Het naam-waarde paar wordt gebouwd gebruikend de Belangrijkste parameter van het Koord van de Vraag als naam en waarde van de geïdentificeerde parameter van de Input als waarde van het paar. De [!DNL AppendURI] voegt bevel om het even welk aangewezen toe? en &amp; symbolen nodig om de naam-waardeparen te scheiden van de [!DNL URI] stammen en uit een vorige [!DNL AppendURI] bewerkingen die mogelijk zijn toegepast op de URI.

De [!DNL AppendURI] de transformatie werkt alleen wanneer deze is gedefinieerd in het dialoogvenster [!DNL Transformation.cfg] of een [!DNL Transformation Dataset Include] bestand.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is. |  |
| Invoer | De naam van het veld waarvan de waarde aan de URI wordt toegevoegd. |  |
| Sleutel queryreeks | The name to use in the creation of the name-value pair being appended. |  |

Neem bijvoorbeeld een website die is gemaakt met een traditionele Model-View-Controller-aanpak. In dergelijke systemen is het gebruikelijk dat één webpagina het toegangspunt tot het systeem is. Voor zo&#39;n plaats, zouden de visualisaties van verkeerspatronen in het systeem zeer oninteressant zijn en zouden geen inzichten in bezoekersgebruik en verkeersstroom verstrekken. Neem bijvoorbeeld een website die alle webaanvragen doorstuurt via een URI van het volgende formulier:

* [!DNL https://www.examplesite.com/modelview.asp?id=login&name=bob]

De modelmeningASP- pagina ontvangt al verkeer en bepaalt zijn acties die op de waarde van het identiteitskaart- gebied in de vraag worden gebaseerd. Standaard zou de URI-dimensie één item bevatten:

* [!DNL modelview.asp]

Dit zou in een vrij oninteressante afbeelding van het verkeer door de plaats resulteren, aangezien al verkeer door één enkele URI wordt gefundeerd. Om dit specifieke scenario aan te pakken en een meer informatief beeld te geven van de onderliggende architectuur van de website, [!DNL AppendURI] U kunt gebruiken om enkele unieke naam-waarde paren van het cs-uri-vraag gebied naar de dimensie van URI te verplaatsen die voor visualisaties wordt gebruikt. De hieronder getoonde transformatie geeft de details van een dergelijke transformatie:

![](assets/cfg_TransformationType_AppendURI.png)

In dit voorbeeld worden door het systeem twee pagina&#39;s gebruikt om alle aanvragen af te handelen: [!DNL modelview.asp] en [!DNL xmlmodelview.asp]. Één pagina wordt gebruikt voor browser verkeer, en andere wordt gebruikt voor systeem-aan-systeem de mededelingen van XML. Het proces van de toepassingsserver gebruikt de id naam van cs-uri-vraag om te bepalen welke actie moet worden ondernomen. Daarom kunt u de waarde uit het gebied van identiteitskaart halen en het toevoegen aan URI. Het resultaat is een verzameling URI&#39;s met een variatiebereik die bezoekersverkeer via de website weerspiegelt. Hier, a [!DNL String Match] De voorwaarde bepaalt de logboekingangen waarop de transformatie wordt toegepast door het cs-uri-stem gebied naar de twee Web-pagina&#39;s van belang te zoeken en alle anderen te negeren. De invoer (de waarde van ons naam-waardepaar) is het resultaat van cs-uri-query(id), die &quot;login is.&quot; Zoals gespecificeerd door de Belangrijkste parameter van het Koord van de Vraag, is de naam die wordt toegevoegd &quot;id.&quot; Voor de binnenkomende cs-uri-waarde van ons voorbeeld wordt de resulterende URI gebruikt door de [!DNL URI] dimensie is [!DNL /modelview.asp&id=login].
