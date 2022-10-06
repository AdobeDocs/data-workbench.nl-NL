---
description: Stappen om een nieuwe terreinlaag beschikbaar te maken voor weergave op de wereldvisualisatie.
title: Een nieuwe Terrain Image Layer beschikbaar maken
uuid: aeeb4ab0-f55c-47b8-96e4-eafd4df4d68a
exl-id: 76374298-ed65-4fcf-b40b-be7c15784f40
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Een nieuwe Terrain Image Layer beschikbaar maken{#making-a-new-terrain-image-layer-available}

{{eol}}

Stappen om een nieuwe terreinlaag beschikbaar te maken voor weergave op de wereldvisualisatie.

1. In de map Profielen\*profielnaam*\Maps in de map **[!UICONTROL Insight Server]** installatiemap, plaatst u het laagbestand en de ondersteunende afbeeldingsbestanden.
1. Bewerk de [!DNL order.txt] bestand in de map Profielen\*profielnaam*\Maps om de volgorde aan te geven waarin de lagen moeten worden weergegeven. Standaard worden lagen op naam in lexicografische volgorde weergegeven.

   >[!NOTE]
   >
   >Bij het bewerken van de [!DNL order.txt] , zorg ervoor dat kaartlagen die u wilt tonen niet worden bedekt.

   Voor meer informatie over het gebruik [!DNL order.txt] dossiers, zie het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse van de Eigenschappen van *Gebruikershandleiding voor Data Workbench*.

1. Selecteer in de werkbank Gegevens het gewenste profiel door met de rechtermuisknop op de titelbalk van de werkruimte te klikken en op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*.
1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Work Online]**. Er verschijnt een X naast [!DNL Work Online].
1. Open een werkruimte en op een globale visualisatie, klik met de rechtermuisknop aan en selecteer de nieuwe laag. Er verschijnt een X naast de laagnaam.
