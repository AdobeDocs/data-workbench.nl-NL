---
description: Stappen om om het even welke gebiedslaag ter beschikking te stellen om op de wereldvisualisatie te tonen.
title: Nieuwe laag voor terreinafbeelding beschikbaar maken
uuid: 8fb98a3e-6335-4922-a1e6-35c92b19e2ec
exl-id: bf0e6b37-4c8a-4d50-8bc9-eb70ca1cbb23
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Een nieuwe achtergrondafbeeldingslaag beschikbaar maken{#make-a-new-terrain-image-layer-available}

Stappen om om het even welke gebiedslaag ter beschikking te stellen om op de wereldvisualisatie te tonen.

1. Plaats het laagbestand en de ondersteunende afbeeldingsbestanden in de map Profiles\*profile name*\Maps in de installatiemap van de Data Workbench-server.
1. Bewerk het [!DNL order.txt]-bestand in de map Profielen\*profielnaam*\Maps om de volgorde aan te geven waarin de lagen moeten worden weergegeven. Standaard worden lagen op naam in lexicografische volgorde weergegeven.

   >[!NOTE]
   >
   >Let er bij het bewerken van het [!DNL order.txt]-bestand op dat kaartlagen die u wilt tonen, niet worden bedekt.

   Voor meer informatie over het gebruiken van [!DNL order.txt] dossiers, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse van *Gids van de Gebruiker van de Data Workbench*.

1. Selecteer in Data Workbench het gewenste profiel door met de rechtermuisknop op de titelbalk van de werkruimte te klikken en op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>* te klikken.
1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Work Online]**. Er verschijnt een X naast Online werken.
1. Open een werkruimte en op een globale visualisatie, klik met de rechtermuisknop aan en selecteer de nieuwe laag. Er verschijnt een X naast de laagnaam.
