---
description: ongeldig
solution: Analytics
title: Het initialiseren van en het Bijwerken van de Definitie van het Schema van een Profiel
topic: Data workbench
uuid: 38e47ded-340e-4f65-b06c-f2e2254f0863
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het initialiseren van en het Bijwerken van de Definitie van het Schema van een Profiel{#initializing-and-updating-a-profile-s-schema-definition}

1. Open het profiel dat u wilt instellen **[!UICONTROL Schema Builder]** voor het profiel dat u wilt instellen.
1. Een **[!UICONTROL Loading]** bericht zal worden getoond terwijl het schema van het profiel van het Inzicht wordt teruggewonnen. De tijdsduur voor het laden van het schema is afhankelijk van de complexiteit van het profiel dat wordt geladen.
1. Wanneer volledig, zult u een samenvatting van de verschillen tussen de **[!UICONTROL Insight Schema]** in de linkerruit, en de **[!UICONTROL Dashboard Schema]** in de juiste ruit zien. Deze samenvatting zal in het lagere linkergedeelte van het **[!UICONTROL Schema Builder]** venster verschijnen.

   >[!NOTE]
   >
   >Wanneer vestiging zal het schema voor het eerst, elk metrisch, afmeting, en filter verschillend van het schema van het dashboard worden vermeld. Dit is omdat de dashboardschemavoorwerpen momenteel niet bestaan.

   ![](assets/schema_builder2.png)

1. Klik de **[!UICONTROL Synchronize with Schema]** knoop om alle metriek, afmetingen, en filters van de mening van het Schema van het Inzicht met de mening van het Schema van het Dashboard te synchroniseren.
1. Wanneer volledig, zou u een bericht moeten zien erop wijzend dat er geen gevonden verschillen zijn:

   ![](assets/diff_found.png)

1. Als er om het even welke fouten met het Schema-zulke van het Dashboard zoals dubbele metriek en afmetingen-dan zijn moet u hen manueel verbeteren alvorens u kunt bewaren.

   >[!NOTE]
   >
   >U kunt om het even welke metriek, afmetingen, of filters uit selectief verwijderen **[!UICONTROL Dashboard Schema]** dat u niet aan eind - gebruikers van het dashboard wilt verschijnen. U zult een waarschuwing ontvangen dat de punten niet aanwezig in het Schema van het Dashboard zijn, maar het zal u niet verhinderen te bewaren.

1. Wanneer klaar, klik **[!UICONTROL Save]** om uw veranderingen in het schema van het dashboard te bewaren.
1. Het dashboardsysteem zal deze schemadefinitie gebruiken om de afmetingen, de metriek, en de filters te bevolken beschikbaar aan eind - gebruikers van de dashboardinterface.
