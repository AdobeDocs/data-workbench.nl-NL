---
description: Stappen om een vectorlaag beschikbaar te maken voor weergave op de wereldvisualisatie.
title: Een nieuwe vectorlaag beschikbaar maken
uuid: 7e88f183-b0aa-452d-b124-7cd970be9bb9
exl-id: aaa1a680-3733-43c3-9d14-5aaa5f4aad6e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# Een nieuwe vectorlaag beschikbaar maken{#making-a-new-vector-layer-available}

{{eol}}

Stappen om een vectorlaag beschikbaar te maken voor weergave op de wereldvisualisatie.

1. Plaats in de map Profielen\*profielnaam*\Maps in de installatiemap van de gegevenswerkbankserver het laagbestand en de [!DNL .vec] of [!DNL .tsv] bestanden.
1. Bewerk de [!DNL order.txt] bestand in de map Profielen\*profielnaam*\Maps om de volgorde aan te geven waarin de lagen moeten worden weergegeven. Standaard worden lagen op naam in lexicografische volgorde weergegeven.

   >[!NOTE]
   >
   >Bij het bewerken van de [!DNL order.txt] , zorg ervoor dat kaartlagen die u wilt tonen niet worden bedekt.

   Voor meer informatie over het gebruik [!DNL order.txt] dossiers, zie het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse van de Eigenschappen van *Gebruikershandleiding voor Data Workbench*.

1. Selecteer in de werkbank Gegevens het gewenste profiel door met de rechtermuisknop op de titelbalk van de werkruimte te klikken en op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*.
1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Work Online]**. Er verschijnt een X naast [!DNL Work Online].
1. Open een werkruimte en op een globale visualisatie, klik met de rechtermuisknop aan en selecteer de nieuwe laag. Er verschijnt een X naast de laagnaam.
