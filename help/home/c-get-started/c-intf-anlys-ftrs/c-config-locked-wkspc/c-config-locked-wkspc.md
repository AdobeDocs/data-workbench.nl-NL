---
description: Data Workbench kan worden gevormd om slechts bepaalde gebruikers toe te staan om bepaalde werkruimten te veranderen.
title: Een vergrendelde werkruimte configureren
uuid: 0bb264f6-20b9-43d9-903e-1b2422af21d5
exl-id: e31a786e-064e-4f2c-9bf4-7ceafde814c0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Een vergrendelde werkruimte configureren{#configure-a-locked-workspace}

{{eol}}

Data Workbench kan worden gevormd om slechts bepaalde gebruikers toe te staan om bepaalde werkruimten te veranderen.

Terwijl een werkruimte is vergrendeld, kunnen gebruikers in de meeste visualisaties selecties maken en de gegevens in tabellen sorteren, maar kunnen ze de werkruimte niet anderszins wijzigen. Deze functionaliteit voorkomt dat gebruikers per ongeluk wijzigingen aanbrengen in de werkruimten.

De volgende drie elementen werken samen om de vergrendeling van werkruimten te beheren:

* **Een map.lock of *naam werkruimte*.lock-bestand:** A [!DNL folder.lock] bestand geeft aan of de werkruimten in een bepaalde map zijn vergrendeld, terwijl een werkruimte [!DNL name.lock] bestand geeft aan of een bepaalde werkruimte is vergrendeld.

* **De parameter Ontgrendelen in het deelvenster [!DNL Insight.cfg] bestand:** Met deze parameter wordt opgegeven of de vergrendelde werkruimten tijdelijk kunnen worden ontgrendeld.
* **De menuoptie Tijdelijk ontgrendelen:** Wanneer de parameter Unlock in de gebruikersinterface [!DNL Insight.cfg] is ingesteld op true, wordt deze optie automatisch weergegeven in het menu van de titelbalk van elke vergrendelde werkruimte, zodat de gebruiker deze kan ontgrendelen.

Voor informatie over [!DNL folder.lock] en werkruimte [!DNL name.lock] , zie de volgende sectie. Voor informatie over het instellen van de parameter Unlock raadpleegt u [De parameter Ontgrendelen instellen](../../../../home/c-get-started/c-intf-anlys-ftrs/c-config-locked-wkspc/c-unlck-param.md#concept-b018a85c6217489aa01b17845872df7f). Voor informatie over de [!DNL Temporarily Unlock menu] optie, zie [Een werkruimte ontgrendelen](../../../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e).
