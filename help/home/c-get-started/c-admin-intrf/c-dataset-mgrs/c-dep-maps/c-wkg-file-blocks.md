---
description: Wanneer u datasetcomponenten op een gebiedsdeelkaart toont, hebt u de optie om de Include de vertoningsoptie van de Blokken van het Dossier toe te laten.
title: Bestandsblokken
uuid: 079dccba-ef19-4895-90bb-6c56f26e8beb
exl-id: 04b0faf1-a16d-4e46-b790-5fe2023f2ba1
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Bestandsblokken{#file-blocks}

Wanneer u datasetcomponenten op een gebiedsdeelkaart toont, hebt u de optie om de Include de vertoningsoptie van de Blokken van het Dossier toe te laten.

Wanneer deze optie wordt toegelaten, toont de kaart één enkele blauwe knoop voor alle transformaties die in één dossier van de datasetconfiguratie en één enkele groene knoop voor alle uitgebreide dimensies worden bepaald die in één dossier van de datasetconfiguratie worden bepaald. Als een [!DNL log processing dataset include]-bestand bijvoorbeeld de definities van drie transformaties bevat, wordt op de kaart één blauw knooppunt weergegeven dat de drie transformaties vertegenwoordigt. Op dezelfde manier als een [!DNL transformation dataset include] dossier de definities van twee uitgebreide afmetingen omvat, toont de kaart één groene knoop die de twee uitgebreide afmetingen vertegenwoordigt.

## Transformatieblokken {#section-c442730394264a0b850792a32eaaa2da}

Elk blauw knooppunt is een transformatieblok en heeft de volgende opties:

* Als u de invoervelden van het transformatieblok wilt weergeven, klikt u met de rechtermuisknop op het knooppunt voor het blok en klikt u op **[!UICONTROL Inputs]**.
* Als u de uitvoervelden van het transformatieblok wilt weergeven, klikt u met de rechtermuisknop op het knooppunt voor het blok en klikt u op **[!UICONTROL Outputs]**.
* Als u een transformatie in het blok wilt bewerken, klikt u met de rechtermuisknop op het knooppunt voor het blok en klikt u op **[!UICONTROL Edit Configuration]**. De callout die vertoningen bevat het volledige configuratiedossier waarin alle transformaties worden bepaald. Vervolgens kunt u de parameters naar wens bewerken. Voor meer informatie over deze parameters, zie *de Gids van de Configuratie van de Dataset*.

* Als u alle transformaties in het blok wilt zien, klikt u met de rechtermuisknop op het knooppunt voor het transformatieblok en klikt u op **[!UICONTROL Show Details]**. De callout die vertoningen bevat een andere gebiedsafbeelding die knopen voor alle transformaties in het blok toont.

## Dimension-blokken {#section-0dd581ac6dfc4153bee5300b3cfae2a0}

Elk groen knooppunt is een afmetingsblok en heeft de volgende opties:

* Als u de invoervelden of de bovenliggende dimensie van het dimensielblok wilt weergeven, klikt u met de rechtermuisknop op het knooppunt voor het blok en klikt u op **[!UICONTROL Inputs]**.
* Klik met de rechtermuisknop op het knooppunt voor het blok en klik op **[!UICONTROL Outputs]** om de uitvoerafmetingen van het afmetingsblok weer te geven.
