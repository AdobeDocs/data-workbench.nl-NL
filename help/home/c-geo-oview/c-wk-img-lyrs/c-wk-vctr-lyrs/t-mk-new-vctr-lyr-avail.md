---
description: Stappen om een vectorlaag beschikbaar te maken voor weergave op de wereldvisualisatie.
title: Een nieuwe vectorlaag beschikbaar maken
uuid: 7e88f183-b0aa-452d-b124-7cd970be9bb9
exl-id: aaa1a680-3733-43c3-9d14-5aaa5f4aad6e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# Een nieuwe vectorlaag beschikbaar maken{#making-a-new-vector-layer-available}

Stappen om een vectorlaag beschikbaar te maken voor weergave op de wereldvisualisatie.

1. Plaats het laagbestand en de [!DNL .vec]- of [!DNL .tsv]-bestanden in de map Profiles\*profile name*\Maps in de installatiemap van de gegevenswerkbankserver.
1. Bewerk het [!DNL order.txt]-bestand in de map Profielen\*profielnaam*\Maps om de volgorde aan te geven waarin de lagen moeten worden weergegeven. Standaard worden lagen op naam in lexicografische volgorde weergegeven.

   >[!NOTE]
   >
   >Let er bij het bewerken van het [!DNL order.txt]-bestand op dat kaartlagen die u wilt tonen, niet worden bedekt.

   Voor meer informatie over het gebruiken van [!DNL order.txt] dossiers, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse van *Gids van de Gebruiker van de Data Workbench*.

1. Selecteer het gewenste profiel in de gegevenswerkbank door met de rechtermuisknop op de titelbalk van de werkruimte te klikken en op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>* te klikken.
1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Work Online]**. Er verschijnt een X naast [!DNL Work Online].
1. Open een werkruimte en op een globale visualisatie, klik met de rechtermuisknop aan en selecteer de nieuwe laag. Er verschijnt een X naast de laagnaam.
