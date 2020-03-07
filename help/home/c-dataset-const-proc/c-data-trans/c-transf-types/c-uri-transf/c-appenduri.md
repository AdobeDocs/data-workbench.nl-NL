---
description: De transformatie AppendURI verstrekt een manier om informatie aan de standaardwaarde toe te voegen die uit de logboekingangen komt die worden gebruikt om de dataset te bouwen.
solution: Analytics
title: ToevoegenURI
topic: Data workbench
uuid: 8334d4f9-2bf6-4bd0-af65-8f2b0959652d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# ToevoegenURI{#appenduri}

De transformatie AppendURI verstrekt een manier om informatie aan de standaardwaarde toe te voegen die uit de logboekingangen komt die worden gebruikt om de dataset te bouwen.

De transformatie plaatst een naam-waarde paar aan het eind van het interne gebied dat wordt gebruikt om de dimensie van URI tot stand te brengen. Het naam-waarde paar wordt gebouwd gebruikend de Belangrijkste parameter van het Koord van de Vraag als naam en waarde van de geïdentificeerde parameter van de Input als waarde van het paar. Het [!DNL AppendURI] bevel voegt om het even welk aangewezen toe? en &amp; de symbolen noodzakelijk om de naam-waarde paren van de [!DNL URI] stam en van om het even welke vorige [!DNL AppendURI] verrichtingen te scheiden die op URI kunnen zijn toegepast.

De [!DNL AppendURI] transformatie werkt slechts wanneer bepaald in het [!DNL Transformation.cfg] dossier of een [!DNL Transformation Dataset Include] dossier.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde om te gebruiken als aan de voorwaarde wordt voldaan en de inputwaarde niet beschikbaar is. |  |
| Invoer | De naam van het gebied de waarvan waarde aan URI wordt toegevoegd. |  |
| String-sleutel voor query | De naam aan gebruik in de verwezenlijking van het naam-waarde paar dat wordt toegevoegd. |  |

Overweeg een website die gebruikend een traditionele model-mening-Controlemechanisme benadering werd gebouwd. In dergelijke systemen, is het gemeenschappelijk om één enkele Web-pagina te hebben het punt van toegang tot het systeem is. Voor zo&#39;n plaats, zouden de visualisaties van verkeerspatronen in het systeem zeer oninteressant zijn en zouden geen inzichten in bezoekersgebruik en verkeersstroom verstrekken. Bijvoorbeeld, overweeg een website die alle Webverzoeken door URI van de volgende vorm trekt:

* [!DNL http://www.examplesite.com/modelview.asp?id=login&name=bob]

De pagina van het modelASPIS ontvangt al verkeer en bepaalt zijn acties die op de waarde van het identiteitskaart- gebied in de vraag worden gebaseerd. Door gebrek, zou de dimensie van URI één enkele ingang bevatten:

* [!DNL modelview.asp]

Dit zou in een vrij oninteressante afbeelding van het verkeer door de plaats resulteren, aangezien al verkeer door één enkel URI wordt gesponsord. Om dit bepaalde scenario te richten en een meer informatieve mening in de onderliggende architectuur van de website te verstrekken, [!DNL AppendURI] kan worden gebruikt om enkele unieke naam-waarde paren van het cs-uri-vraaggebied aan de dimensie van URI te bewegen die voor visualisaties wordt gebruikt. De transformatie hieronder geeft de details van een dergelijke transformatie:

![](assets/cfg_TransformationType_AppendURI.png)

In dit voorbeeld, zijn er twee pagina&#39;s die door het systeem worden gebruikt om alle verzoeken te behandelen: [!DNL modelview.asp] en [!DNL xmlmodelview.asp]. Één pagina wordt gebruikt voor browser verkeer, en andere wordt gebruikt voor de mededelingen van systeem-aan-systeemXML. Het proces van de toepassingsserver gebruikt de identiteitskaart van cs-uri-vraag om te bepalen welke actie te nemen. Daarom kunt u de waarde uit het identiteitskaart- gebied halen en het toevoegen aan URI. Het resultaat is een inzameling van URIs met een waaier van variatie die op bezoekersverkeer door de website wijst. Hier, bepaalt een [!DNL String Match] voorwaarde de logboekingangen waarop de transformatie wordt toegepast door het cs-uri-stengebied voor de twee Web-pagina&#39;s van belang te zoeken en alle anderen te negeren. De input (de waarde van ons naam-waarde paar) is het resultaat van cs-uri-vraag (identiteitskaart), die &quot;login is.&quot; Zoals gespecificeerd door de Belangrijkste parameter van het Koord van de Vraag, is de naam die wordt toegevoegd &quot;identiteitskaart.&quot; Aldus, voor de inkomende cs-uri waarde van ons voorbeeld, is resulterend URI die door de [!DNL URI] afmeting wordt gebruikt [!DNL /modelview.asp&id=login].
