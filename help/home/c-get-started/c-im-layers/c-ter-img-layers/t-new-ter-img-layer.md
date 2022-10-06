---
description: Stappen om om het even welke gebiedslaag ter beschikking te stellen om op de wereldvisualisatie te tonen.
title: Nieuwe laag voor terreinafbeelding beschikbaar maken
uuid: 8fb98a3e-6335-4922-a1e6-35c92b19e2ec
exl-id: bf0e6b37-4c8a-4d50-8bc9-eb70ca1cbb23
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Nieuwe laag voor terreinafbeelding beschikbaar maken{#make-a-new-terrain-image-layer-available}

{{eol}}

Stappen om om het even welke gebiedslaag ter beschikking te stellen om op de wereldvisualisatie te tonen.

1. Plaats het laagbestand en de ondersteunende afbeeldingsbestanden in de map Profiles\*profile name*\Maps in de installatiemap van de Data Workbench-server.
1. Bewerk de [!DNL order.txt] bestand in de map Profielen\*profielnaam*\Maps om de volgorde aan te geven waarin de lagen moeten worden weergegeven. Standaard worden lagen op naam in lexicografische volgorde weergegeven.

   >[!NOTE]
   >
   >Bij het bewerken van de [!DNL order.txt] , zorg ervoor dat kaartlagen die u wilt tonen niet worden bedekt.

   Voor meer informatie over het gebruik [!DNL order.txt] dossiers, zie het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse van de Eigenschappen van *Gebruikershandleiding voor Data Workbench*.

1. Selecteer in Data Workbench het gewenste profiel door met de rechtermuisknop op de titelbalk van de werkruimte te klikken en op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*.
1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Work Online]**. Er verschijnt een X naast Online werken.
1. Open een werkruimte en op een globale visualisatie, klik met de rechtermuisknop aan en selecteer de nieuwe laag. Er verschijnt een X naast de laagnaam.
