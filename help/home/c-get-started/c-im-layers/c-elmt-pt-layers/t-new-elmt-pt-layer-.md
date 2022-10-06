---
description: Stappen om een elementpuntlaag beschikbaar te maken voor weergave op de wereldvisualisatie.
title: Nieuwe elementpuntlaag beschikbaar maken
uuid: 5f4bad2f-e98d-4224-bba8-285ad5e23da9
exl-id: 12797335-0788-4103-a581-41bc3bb3dcc9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Nieuwe elementpuntlaag beschikbaar maken{#make-a-new-element-point-layer-available}

{{eol}}

Stappen om een elementpuntlaag beschikbaar te maken voor weergave op de wereldvisualisatie.

1. Plaats het laagbestand en het bijbehorende opzoekbestand in de map Profielen\*profielnaam*\Maps in de installatiemap van de Data Workbench-server.
1. Als u een nieuwe afmeting voor uw laag van het elementenpunt bepaalde en uw dataset nog niet hertransformeerde, retransform nu uw dataset.
1. Bewerk de [!DNL order.txt] bestand in de map Profielen\*profielnaam*\Maps om de volgorde aan te geven waarin de lagen moeten worden weergegeven. Standaard worden lagen op naam in lexicografische volgorde weergegeven.

   >[!NOTE]
   >
   >Bij het bewerken van de [!DNL order.txt] , zorg ervoor dat kaartlagen die u wilt tonen niet worden bedekt.

   Voor meer informatie over het gebruik [!DNL order.txt] dossiers, zie het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse van de Eigenschappen van *Gebruikershandleiding voor Data Workbench*.

1. Selecteer in Data Workbench het gewenste profiel door met de rechtermuisknop op de titelbalk van de werkruimte te klikken en op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*.
1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Work Online]**. Er verschijnt een X naast Online werken.
1. Open een werkruimte en op een globale visualisatie, klik met de rechtermuisknop aan en selecteer de nieuwe laag. Er verschijnt een X naast de laagnaam.
