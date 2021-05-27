---
description: Data Workbench kan worden gevormd om slechts bepaalde gebruikers toe te staan om bepaalde werkruimten te veranderen.
title: Een vergrendelde werkruimte configureren
uuid: 0bb264f6-20b9-43d9-903e-1b2422af21d5
exl-id: e31a786e-064e-4f2c-9bf4-7ceafde814c0
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Een vergrendelde werkruimte configureren{#configure-a-locked-workspace}

Data Workbench kan worden gevormd om slechts bepaalde gebruikers toe te staan om bepaalde werkruimten te veranderen.

Terwijl een werkruimte is vergrendeld, kunnen gebruikers in de meeste visualisaties selecties maken en de gegevens in tabellen sorteren, maar kunnen ze de werkruimte niet anderszins wijzigen. Deze functionaliteit voorkomt dat gebruikers per ongeluk wijzigingen aanbrengen in de werkruimten.

De volgende drie elementen werken samen om de vergrendeling van werkruimten te beheren:

* **Een bestand met de naam *folder.lock of*werkruimte:** Een  [!DNL folder.lock] bestand geeft aan of de werkruimten in een bepaalde map zijn vergrendeld, terwijl een  [!DNL name.lock] bestand van een werkruimte aangeeft of een bepaalde werkruimte is vergrendeld.

* **De parameter Ontgrendelen in het  [!DNL Insight.cfg] bestand van een gebruiker:** Deze parameter geeft aan of die gebruiker vergrendelde werkruimten tijdelijk kan ontgrendelen.
* **De menuoptie Tijdelijk ontgrendelen:** Wanneer de parameter Ontgrendelen in de gebruikersinterface  [!DNL Insight.cfg] is ingesteld op true, wordt deze optie automatisch weergegeven in het menu van de titelbalk van elke vergrendelde werkruimte, zodat de gebruiker deze kan ontgrendelen.

Zie de volgende sectie voor informatie over [!DNL folder.lock]- en werkruimte [!DNL name.lock]-bestanden. Zie [De parameter Ontgrendelen instellen](../../../../home/c-get-started/c-intf-anlys-ftrs/c-config-locked-wkspc/c-unlck-param.md#concept-b018a85c6217489aa01b17845872df7f) voor informatie over het instellen van de parameter Ontgrendelen. Zie [Een werkruimte ontgrendelen](../../../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e) voor informatie over de optie [!DNL Temporarily Unlock menu].
