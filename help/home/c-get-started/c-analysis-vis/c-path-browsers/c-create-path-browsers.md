---
description: U kunt een padbrowser maken op basis van een grafiek, tabel of procesafbeelding.
title: Padbrowsers maken
uuid: 84a5e587-fb02-461b-aec8-1b6ad473ebc3
exl-id: 9fa11b84-da73-447a-8b10-7eab381e3f66
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Padbrowsers maken{#creating-path-browsers}

U kunt een padbrowser maken op basis van een grafiek, tabel of procesafbeelding.

**Een padbrowser maken op basis van een grafiek of tabel**

1. Voeg een padbrowser toe aan uw werkruimte. De visualisatie is leeg, behalve het label (Reeks van...) in de linkerbovenhoek.
1. Open een grafiek of een lijst die de afmeting tonen waarvan elementen u op wegbrowser wilt tonen. Als u bijvoorbeeld met websitegegevens werkt, opent u een paginagrafiek of tabel en identificeert u de pagina die u als basis wilt instellen.
1. Druk op Ctrl+Alt en sleep het gewenste element naar de padbrowser. Het label in de linkerbovenhoek van de padbrowser verandert om de basisdimensie weer te geven waarvan u het element naar de padbrowser sleept.

>[!NOTE]
>
>Als u een element naar een padbrowser sleept, kan de basisdimensie die aan de padbrowser is gekoppeld, veranderen, maar niet de afmetingen van het niveau, de groepsdimensie of de metrische waarde. Daarom moet u voorzichtigheid in het kiezen van een basisafmeting uitoefenen die wanneer gebruikt met de het niveauafmeting van de wegbrowser, groepsafmeting, en metrisch steek houdt. Om de niveauafmeting, groepsafmeting, of metrisch te veranderen, moet u het dossier van de wegbrowser [!DNL *.vw] in een tekstredacteur zoals Blocnote uitgeven. Zie [Padbrowsers configureren](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-path-brwsr.md#task-bbb3ddaa140a414f984b697c2b8202a3).

**Een padbrowser maken op basis van een proceskaart**

>[!NOTE]
>
>Een wegbrowser die van een proceskaart wordt gecreeerd toont slechts de elementen die op de proceskaart worden getoond. Andere elementen van de basisdimensie worden niet weergegeven.

1. Maak een procesafbeelding. Zie [Proceskaarten maken](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-create-proc-maps.md#concept-daf5b14dae7a442191611b1b9c1122bf).
1. Sleep het gewenste element van de proceskaart aan wegbrowser. Het element wordt de basis van de padbrowser.

>[!NOTE]
>
>Wanneer u een wegbrowser van een proceskaart creeert, wegbrowser negeert de elementen van de niveaudimensie zonder bijbehorende elementen van de basisdimensie. Wanneer u een knoop van een proceskaart op wegbrowser sleept, wordt de de basisdimensie van de wegbrowser (genoemd Kaart) bepaald door de proceskaart, en zijn elementen zijn beperkt tot de elementen op de proceskaart. Dientengevolge, hebben sommige elementen van de het niveauafmeting van de wegbrowser geen bijbehorende basisafmetingselementen en niet vertegenwoordigd in wegbrowser.
