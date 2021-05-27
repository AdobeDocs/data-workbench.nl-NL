---
description: Het initialiseren van en het Bijwerken van de Definitie van het Schema van een Profiel
title: Het initialiseren van en het Bijwerken van de Definitie van het Schema van een Profiel
uuid: 38e47ded-340e-4f65-b06c-f2e2254f0863
exl-id: e8190909-4416-4d4a-8901-130d01906773
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Het initialiseren van en het Bijwerken van de Definitie van het Schema van een Profiel{#initializing-and-updating-a-profile-s-schema-definition}

1. Open **[!UICONTROL Schema Builder]** voor het profiel u opstelling zou willen.
1. Een **[!UICONTROL Loading]** bericht zal worden getoond terwijl het schema van het profiel van het Inzicht wordt teruggewonnen. De tijdsduur voor het laden van het schema is afhankelijk van de complexiteit van het profiel dat wordt geladen.
1. Na voltooiing wordt een overzicht weergegeven van de verschillen tussen **[!UICONTROL Insight Schema]** in het linkervenster en **[!UICONTROL Dashboard Schema]** in het rechtervenster. Deze samenvatting wordt weergegeven in het onderste gedeelte van het venster **[!UICONTROL Schema Builder]**.

   >[!NOTE]
   >
   >Wanneer het opzetten van het schema voor het eerst, zal elke metrisch, afmeting, en filter verschillend van het schema van het dashboard worden vermeld. Dit komt omdat de schemaobjecten van het dashboard op dit moment niet bestaan.

   ![](assets/schema_builder2.png)

1. Klik op de knop **[!UICONTROL Synchronize with Schema]** om alle metriek, dimensies en filters te synchroniseren vanuit de weergave Schema van het Inzicht met de weergave Schema van het dashboard.
1. Wanneer volledig, zou u een bericht moeten zien erop wijzend dat er geen verschillen worden gevonden:

   ![](assets/diff_found.png)

1. Als er fouten zijn met het dashboardschema, zoals dubbele cijfers en afmetingen, moet u deze handmatig corrigeren voordat u ze kunt opslaan.

   >[!NOTE]
   >
   >U kunt op selectieve wijze alle metriek, afmetingen of filters verwijderen uit het **[!UICONTROL Dashboard Schema]**-bestand die u niet wilt weergeven aan eindgebruikers van het dashboard. U ontvangt een waarschuwing dat er geen items aanwezig zijn in het dashboardschema, maar dit belet niet dat u het bestand opslaat.

1. Klik, indien gereed, op **[!UICONTROL Save]** om de wijzigingen in het schema van het dashboard op te slaan.
1. Het dashboardsysteem gebruikt deze schemadefinitie om de afmetingen, metriek, en filters te bevolken beschikbaar aan eind - gebruikers van de dashboardinterface.
