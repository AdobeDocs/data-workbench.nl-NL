---
description: De transformaties en de afmetingen gebruiken voorwaarden om te bepalen wanneer bepaalde instructies of acties op logboekgebieden van toepassing zijn.
solution: Analytics
title: Informatie over voorwaarden
topic: Data workbench
uuid: 882fe761-895c-4226-a019-270c50ae6da2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Informatie over voorwaarden{#about-conditions}

De transformaties en de afmetingen gebruiken voorwaarden om te bepalen wanneer bepaalde instructies of acties op logboekgebieden van toepassing zijn.

De parameter van de Voorwaarde van de Ingang van het Logboek gebruikt voorwaarden om te bepalen welke logboekingangen in het proces van de datasetconstructie zouden moeten worden omvat. Dit bijlage beschrijft de verschillende soorten voorwaarden beschikbaar binnen de server van de gegevenswerkbank.

Een voorwaarde valt in één van twee categorieën:

* **[!DNL Test Operations]:**[!DNL Compare],[!DNL Not Empty],[!DNL Range],[!DNL Regular Expression], en de[!DNL String Match]voorwaarden worden gebruikt om voor verschillende staten op de beschikbare logboekgebieden te testen.

* **[!DNL Boolean Operations]:**De[!DNL And],[!DNL Or]en[!DNL Neither]omstandigheden worden gebruikt om de hierboven beschreven testbewerkingen te combineren. Bijvoorbeeld, als u een[!DNL Range]voorwaarde en een[!DNL String Match]voorwaarde hebt die allebei vals moeten zijn om de aangewezen actie te voeren, zou u deze twee verrichtingenkinderen van de[!DNL Neither]voorwaarde maken. Merk op dat de[!DNL And]voorwaarde als wortel van al voorwaarde het testen in het systeem wordt gebruikt.

