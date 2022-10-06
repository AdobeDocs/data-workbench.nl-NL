---
description: Het initialiseren van en het Bijwerken van de Definitie van het Schema van een Profiel
title: Het initialiseren van en het Bijwerken van de Definitie van het Schema van een Profiel
uuid: 38e47ded-340e-4f65-b06c-f2e2254f0863
exl-id: e8190909-4416-4d4a-8901-130d01906773
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Het initialiseren van en het Bijwerken van de Definitie van het Schema van een Profiel{#initializing-and-updating-a-profile-s-schema-definition}

{{eol}}

1. Open de **[!UICONTROL Schema Builder]** voor het profiel dat u wilt instellen.
1. A **[!UICONTROL Loading]** Het bericht wordt weergegeven terwijl het schema wordt opgehaald uit het Insight-profiel. De tijdsduur voor het laden van het schema is afhankelijk van de complexiteit van het profiel dat wordt geladen.
1. Wanneer u klaar bent, ziet u een overzicht van de verschillen tussen de **[!UICONTROL Insight Schema]** in het linkerdeelvenster en in het dialoogvenster **[!UICONTROL Dashboard Schema]** in het rechterdeelvenster. Deze samenvatting wordt weergegeven in het onderste gedeelte van het dialoogvenster **[!UICONTROL Schema Builder]** venster.

   >[!NOTE]
   >
   >Wanneer het opzetten van het schema voor het eerst, zal elke metrisch, afmeting, en filter verschillend van het schema van het dashboard worden vermeld. Dit komt omdat de schemaobjecten van het dashboard op dit moment niet bestaan.

   ![](assets/schema_builder2.png)

1. Klik op de knop **[!UICONTROL Synchronize with Schema]** om alle metriek, afmetingen, en filters van de mening van het Schema van het Inzicht met de mening van het Schema van het Schema van het Dashboard te synchroniseren.
1. Wanneer volledig, zou u een bericht moeten zien erop wijzend dat er geen verschillen worden gevonden:

   ![](assets/diff_found.png)

1. Als er fouten zijn met het dashboardschema, zoals dubbele cijfers en afmetingen, moet u deze handmatig corrigeren voordat u ze kunt opslaan.

   >[!NOTE]
   >
   >U kunt metingen, afmetingen of filters selectief verwijderen uit het dialoogvenster **[!UICONTROL Dashboard Schema]** dat u niet aan eindgebruikers van het dashboard wilt verschijnen. U ontvangt een waarschuwing dat er geen items aanwezig zijn in het dashboardschema, maar dit belet niet dat u het bestand opslaat.

1. Klik, indien gereed, op **[!UICONTROL Save]** om de wijzigingen in het schema van het dashboard op te slaan.
1. Het dashboardsysteem gebruikt deze schemadefinitie om de afmetingen, metriek, en filters te bevolken beschikbaar aan eind - gebruikers van de dashboardinterface.
