---
description: Met afhankelijkheidskaarten kunt u de configuratie van de componenten van uw profiel visualiseren en beheren.
title: Afhankelijkheidstoewijzingen
uuid: c869267c-5fa9-43b8-b4d4-06c7a36bfa8e
exl-id: 4618c735-f507-4abc-a4b4-d52a37c64c60,733407ca-3326-406a-a642-a3ea3d3f6b8b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Afhankelijkheidstoewijzingen{#dependency-maps}

Met afhankelijkheidskaarten kunt u de configuratie van de componenten van uw profiel visualiseren en beheren.

* **Dataset-componenten:** Logbronnen, filters, velden, transformaties en uitgebreide dimensies die zijn gedefinieerd in de gegevensset  [!DNL Log Processing.cfg],  [!DNL Transformation.cfg]en  [!DNL dataset include] bestanden.

* **Componenten van het query-model:** Metriek, afmetingen en filters die zijn gedefinieerd in de mappen Dimension, Metriek en Filters.
* **Werkruimten en visualisaties:** Werkruimten, rapporten, menuopties en algemene lagen.

Voor meer informatie over het werken met de componenten van het vraagmodel, werkruimten, en visualisaties in gebiedskaarten, zie *de Gids van de Gebruiker van de Data Workbench*.

Profielcomponenten worden vertegenwoordigd door gekleurde punten (knooppunten) op de kaart. De lijnen die de knopen verbinden tonen gebiedsdelen, namelijk hoe de componenten met elkaar betrekking hebben. Een lijn tussen twee knopen betekent dat een output van de knoop op de linkerzijde een input van de knoop op het recht is, namelijk de juiste knoop van de linkerknoop afhangt.

## Dataset-componenten {#section-3e51c09c23cc40aeade2e6ad0fa7c8d2} weergeven

1. Klik met de rechtermuisknop in de afhankelijkheidskaart en klik op **[!UICONTROL Display]**.
1. Kies **[!UICONTROL Dataset]**. Links van [!DNL Dataset] wordt een X weergegeven.

Voor meer informatie over de andere vertoningsopties zie *de Gids van de Gebruiker van de Data Workbench*.

Het volgende cijfer toont een gebiedsdeelkaart de waarvan knopen de logboekbronnen, gebieden, transformaties, en uitgebreide dimensies van een dataset vertegenwoordigen.

![](assets/vis_DependencyMap.png)

* Een geel-groene knoop vertegenwoordigt één of meerdere logboekbronnen of een filter die in de dataset wordt bepaald. Een knooppunt voor een logbron wordt altijd het verst naar links op de kaart weergegeven.
* Een grijze node vertegenwoordigt een veld dat wordt weergegeven in de parameter Fields in een [!DNL Log Processing.cfg]- of [!DNL Log Processing Include]bestand.

* Een blauw knooppunt vertegenwoordigt een transformatie.
* Een groene knoop vertegenwoordigt een uitgebreide afmeting.

>[!NOTE]
>
>Als uw dataset één enkele logboekbron heeft, toont de kaart Bron van het Logboek: *logbronnaam*. Als uw dataset veelvoudige logboekbronnen heeft, toont de kaart *number* de Bronnen van het Logboek, waar het aantal de telling van logboekbronnen is. Bijvoorbeeld, als u drie logboekbronnen in uw dataset hebt, toont uw kaart 3 Bronnen van het Logboek.

Als u niet alle knooppunten op de kaart kunt zien, kunt u de kaart verplaatsen of inzoomen of uitzoomen om de volledige kaart weer te geven of om te focussen op een bepaalde sectie. Voor meer informatie over het zoemen, zie het Werken met Visualisaties hoofdstuk van *de Gids van de Gebruiker van de Data Workbench*.

Wanneer u een knoop klikt, worden alle knopen die van die knoop en alle knopen afhangen waarvan die knoop afhangt benadrukt en hun namen tonen.

![](assets/vis_DependencyMap_HighlightedPath.png)

>[!NOTE]
>
>Een gemarkeerd pad in een afhankelijkheidskaart vormt geen selectie.

Wanneer u met de rechtermuisknop op een knooppunt klikt, ziet u identificerende informatie over elke component die op de kaart wordt weergegeven en kiest u menuopties waarmee u meer details over de component kunt bekijken of de component kunt bewerken. Daarnaast kunt u zoeken in tekst en prestatiegegevens weergeven voor transformaties en uitgebreide afmetingen.

Voor informatie over deze functies voor gebiedsdeelkaarten, zie het Administratieve hoofdstuk van Interfaces van *de Gids van de Gebruiker van de Data Workbench*.
