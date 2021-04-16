---
description: Stappen om een nieuwe terreinlaag beschikbaar te maken voor weergave op de wereldvisualisatie.
title: Een nieuwe Terrain Image Layer beschikbaar maken
uuid: aeeb4ab0-f55c-47b8-96e4-eafd4df4d68a
exl-id: 76374298-ed65-4fcf-b40b-be7c15784f40
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Een nieuwe laag voor terreinafbeelding beschikbaar maken{#making-a-new-terrain-image-layer-available}

Stappen om een nieuwe terreinlaag beschikbaar te maken voor weergave op de wereldvisualisatie.

1. Plaats het laagbestand en de ondersteunende afbeeldingsbestanden in de map Profiles\*profile name*\Maps in de installatiemap **[!UICONTROL Insight Server]**.
1. Bewerk het [!DNL order.txt]-bestand in de map Profielen\*profielnaam*\Maps om de volgorde aan te geven waarin de lagen moeten worden weergegeven. Standaard worden lagen op naam in lexicografische volgorde weergegeven.

   >[!NOTE]
   >
   >Let er bij het bewerken van het [!DNL order.txt]-bestand op dat kaartlagen die u wilt tonen, niet worden bedekt.

   Voor meer informatie over het gebruiken van [!DNL order.txt] dossiers, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse van *Gids van de Gebruiker van de Data Workbench*.

1. Selecteer het gewenste profiel in de gegevenswerkbank door met de rechtermuisknop op de titelbalk van de werkruimte te klikken en op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>* te klikken.
1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Work Online]**. Er verschijnt een X naast [!DNL Work Online].
1. Open een werkruimte en op een globale visualisatie, klik met de rechtermuisknop aan en selecteer de nieuwe laag. Er verschijnt een X naast de laagnaam.
