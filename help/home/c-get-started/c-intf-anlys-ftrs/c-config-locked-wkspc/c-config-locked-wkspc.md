---
description: De Werkbank van gegevens kan worden gevormd om slechts bepaalde gebruikers toe te staan om bepaalde werkruimten te veranderen.
solution: Analytics
title: Een vergrendelde werkruimte configureren
topic: Data workbench
uuid: 0bb264f6-20b9-43d9-903e-1b2422af21d5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Een vergrendelde werkruimte configureren{#configure-a-locked-workspace}

De Werkbank van gegevens kan worden gevormd om slechts bepaalde gebruikers toe te staan om bepaalde werkruimten te veranderen.

Terwijl een werkruimte gesloten is, kunnen de gebruikers selecties in de meeste visualisaties maken en de gegevens in lijsten sorteren maar kunnen niet de werkruimte anders veranderen. Deze functionaliteit verhindert gebruikers onbedoelde veranderingen in de werkruimten aan te brengen.

De volgende drie elementen werken samen om het sluiten van werkruimten te controleren:

* **Een map.lock- of *werkruimtetenaam*.lock-bestand:** Een [!DNL folder.lock] dossier specificeert of de werkruimten in een bepaalde omslag gesloten zijn, terwijl een [!DNL name.lock] dossier van de werkruimte specificeert of een bepaalde werkruimte gesloten is.

* **De parameter van de Ontgrendeling in het[!DNL Insight.cfg]dossier van een gebruiker:** Deze parameter specificeert of die gebruiker gesloten werkruimten tijdelijk kan openen.
* **De tijdelijk Unlock menuoptie:** Wanneer de parameter van de Ontgrendeling in de gebruiker aan waar [!DNL Insight.cfg] wordt geplaatst, verschijnt deze optie automatisch in het menu van de titelbar van elke gesloten werkruimte om een manier voor de gebruiker te verstrekken om het te openen.

Voor informatie over [!DNL folder.lock] [!DNL name.lock] en werkruimtedossiers, zie de volgende sectie. Voor informatie over het plaatsen van de Unlock parameter, zie het [Plaatsen van de Parameter](../../../../home/c-get-started/c-intf-anlys-ftrs/c-config-locked-wkspc/c-unlck-param.md#concept-b018a85c6217489aa01b17845872df7f)Unlock. Voor informatie over de [!DNL Temporarily Unlock menu] optie, zie het [Ontgrendelen van een Werkruimte](../../../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e).
