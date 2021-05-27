---
description: Stappen om een elementpuntlaag beschikbaar te maken voor weergave op de wereldvisualisatie.
title: Nieuwe elementpuntlaag beschikbaar maken
uuid: 5f4bad2f-e98d-4224-bba8-285ad5e23da9
exl-id: 12797335-0788-4103-a581-41bc3bb3dcc9
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Nieuwe elementpuntlaag beschikbaar maken{#make-a-new-element-point-layer-available}

Stappen om een elementpuntlaag beschikbaar te maken voor weergave op de wereldvisualisatie.

1. Plaats het laagbestand en het bijbehorende opzoekbestand in de map Profielen\*profielnaam*\Maps in de installatiemap van de Data Workbench-server.
1. Als u een nieuwe afmeting voor uw laag van het elementenpunt bepaalde en uw dataset nog niet hertransformeerde, retransform nu uw dataset.
1. Bewerk het [!DNL order.txt]-bestand in de map Profielen\*profielnaam*\Maps om de volgorde aan te geven waarin de lagen moeten worden weergegeven. Standaard worden lagen op naam in lexicografische volgorde weergegeven.

   >[!NOTE]
   >
   >Let er bij het bewerken van het [!DNL order.txt]-bestand op dat kaartlagen die u wilt tonen, niet worden bedekt.

   Voor meer informatie over het gebruiken van [!DNL order.txt] dossiers, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse van *Gids van de Gebruiker van de Data Workbench*.

1. Selecteer in Data Workbench het gewenste profiel door met de rechtermuisknop op de titelbalk van de werkruimte te klikken en op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>* te klikken.
1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Work Online]**. Er verschijnt een X naast Online werken.
1. Open een werkruimte en op een globale visualisatie, klik met de rechtermuisknop aan en selecteer de nieuwe laag. Er verschijnt een X naast de laagnaam.
