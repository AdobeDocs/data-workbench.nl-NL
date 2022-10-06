---
description: Met procesafbeeldingen kunt u de activiteitsstroom tussen elementen van een dimensie analyseren.
title: Proceskaart
uuid: f1db41a9-400e-467a-ba59-39831fb166af
exl-id: 019cee7b-a704-4b47-84c6-d3ddc277c43e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Proceskaart{#process-map}

{{eol}}

Met procesafbeeldingen kunt u de activiteitsstroom tussen elementen van een dimensie analyseren.

U maakt procesafbeeldingen door de elementen van een dimensie naar een lege tweedimensionale (2D) of driedimensionale (3D) kaart te slepen en neer te zetten. De elementen worden knooppunten op de kaart. Knooppunten zijn cirkels in 2D-proceskaarten en -balken in 3D-proceskaarten.

![](assets/vis_2DProcessMap.png)

![](assets/vis_3DProcessMap.png)

>[!NOTE]
>
>Een proceskaart krijgt zijn naam van zijn gebruik in het analyseren van de stroom van activiteit tussen de stappen in een proces. In dit type analyse vertegenwoordigt elk element op de kaart een stap in het proces.

In tegenstelling tot padbrowsers kunnen procesafbeeldingen maar weinig of net zoveel elementen bevatten als nodig zijn voor de analyse. U kiest de interessepunten en sleept ze naar de kaart. In tegenstelling tot padbrowsers geven procesafbeeldingen de activiteitsstroom in beide richtingen tussen een element en een of meer andere elementen weer.

>[!NOTE]
>
>Deze kaarten werken alleen op de meest effectieve manier als u een legenda in de werkruimte opent. Voor informatie over het gebruik van kleurlegenda bij procesafbeeldingen raadpleegt u [Kleurkoppelingen activeren](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-act-color-lnks.md#concept-2c9b9f67f2bd4cd7a5431fa21c094edc). Zie voor meer informatie over legenda [Kleurlegenda](../../../../home/c-get-started/c-analysis-vis/c-legends/c-color-leg.md#concept-f84d51dc0d6547f981d0642fc2d01358).

Elke proceskaart heeft een bijbehorende basisdimensie, groepsdimensie, niveaudimensie, en metrisch, die sleutels verstrekken om de gegevens te interpreteren die in de proceskaart worden getoond.

De standaardmontages voor de afmetingen en metrisch van een proceskaart hangen van de toepassing van de Data Workbench af die u gebruikt. Zie de toepassingshandleiding voor uw Data Workbench voor informatie over de afmetingen en metriek waarover u beschikt voor uw proceskaarten.

* **Basisdimensie:** Wanneer u een element naar een procesafbeelding sleept, sleept u een element van de basisdimensie en zet u het neer.
* **Dimensie niveau:** Elke dimensie in uw dataset heeft een bijbehorende niveaudimensie (die ook als ouder wordt bedoeld). De niveaudimensie voor uw proceskaart zou het zelfde als de niveaudimensie (of ouder) voor de de basisdimensie van uw proceskaart moeten zijn. Als u bijvoorbeeld een pagina (een element van de pagina-afmeting) naar de kaart sleept, is Paginaweergave de afmeting van het desbetreffende niveau.
* **Groepsdimensie:** De groepsdimensie bepaalt hoe de elementen van de niveaudimensie worden gegroepeerd om de verbindingen tussen knopen te vormen. Voor proceskaarten is de groepsdimensie belangrijk om drie belangrijke redenen:

   * Een verbinding tussen twee knooppunten kan niet meer dan één element van een groepsdimensie beslaan. Om dit te begrijpen, overweeg een voorbeeld gebruikend Webgegevens. Stel dat de basis-, niveau- en groepsafmetingen voor uw procesoverzicht respectievelijk Pagina, Paginaweergave en Sessie zijn. Een verbinding van pagina A aan pagina B vertelt u dat, tijdens om het even welke enige zitting, een paginamening van pagina A vóór een paginamening van pagina B zonder tussenliggende paginameningen van andere pagina&#39;s (knopen) op de kaart voorkwam. Paginaweergaven van andere pagina&#39;s van de site kunnen tijdens dezelfde sessie zijn opgetreden tussen paginaweergaven voor pagina&#39;s A en B, maar deze pagina&#39;s worden niet weergegeven op deze kaart.
   * Een verbinding tussen twee knooppunten kan meerdere elementen van de groepsdimensie vertegenwoordigen. Er kunnen bijvoorbeeld meerdere sessies zijn waarin een paginaweergave van pagina A is opgetreden vóór een paginaweergave van pagina B. Daarom staat de verbinding tussen pagina A en pagina B voor alle afzonderlijke sessies waarin een paginaweergave van pagina A is opgetreden vóór een paginaweergave van pagina B zonder tussenliggende paginaweergaven van andere pagina&#39;s (knooppunten) op de kaart.
   * Wanneer u een selectie maakt die op een knoop binnen een proceskaart wordt gebaseerd, selecteert u alle elementen van de groepsdimensie die dat knoop impliceert. Zie [Selecties maken in visualisaties](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746). Voor informatie over selecties raadpleegt u [Selecties maken in visualisaties](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746).

* **Metrisch:** De grootte van het knooppunt voor een bepaald element is evenredig met de waarde van de metrische waarde voor dat element. Grotere knooppunten geven hogere metrische waarden aan dan kleinere knooppunten.

Als u bijvoorbeeld de opdracht [!DNL Site] Voor HBX toepassing kunt u standaard elementen van de pagina-dimensie naar het procesoverzicht slepen. De grootte van elk knooppunt is gerelateerd aan de hoeveelheid sessies (gedefinieerd door de metrische sessies) waarin die pagina is weergegeven.

>[!NOTE]
>
>U kunt de standaardafmetingen of metrisch voor een proceskaart veranderen. Voor stappen om een proceskaart te vormen, zie [Proceskaarten configureren](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-proc-maps.md#task-4a95730b18a14bc790a77c013832b2d6).
