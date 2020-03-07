---
description: Het dossier van het Logboek Processing.cfg controleert de fase van de logboekverwerking van datasetconstructie, waarin het ongeordende gegeven van de gegevensbronnen (die als logboekbronnen worden bedoeld) wordt gelezen, en de filters en de transformaties worden toegepast op de gegevens.
solution: Analytics
title: Ongeveer het Dossier van de Configuratie van de Verwerking van het Logboek
topic: Data workbench
uuid: 1f5f5d75-8a24-4122-adc8-8c8aef916631
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Ongeveer het Dossier van de Configuratie van de Verwerking van het Logboek{#about-the-log-processing-configuration-file}

Het dossier van het Logboek Processing.cfg controleert de fase van de logboekverwerking van datasetconstructie, waarin het ongeordende gegeven van de gegevensbronnen (die als logboekbronnen worden bedoeld) wordt gelezen, en de filters en de transformaties worden toegepast op de gegevens.

U moet het [!DNL Log Processing.cfg] dossier uitgeven om het even welke volgende taken van de datasetconfiguratie uit te voeren:

* Het specificeren van logboekbronnen. Zie [Logbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md).
* Het bepalen van welke logboekingangen de dataset tijdens logboekverwerking ingaan. Zie de Filters [van](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md) Gegevens en de Voorwaarde van de Ingang van het [Logboek](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).

* Toelatend de splitsing van het volgen IDs met grote hoeveelheden gebeurtenisgegevens. Zie [Belangrijkste splitsing](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).
* Het vormen van een server van de gegevenswerkbank om als eenheid van de dossierserver te lopen. Zie het [Vormen van een Eenheid](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md)van de Server van het Dossier van het Inzicht.
* Het vormen van een server van de gegevenswerkbank om als gecentraliseerde normalisatieserver te lopen. Zie het [Vormen van een Eenheid](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md)van de Server van het Dossier van het Inzicht.

>[!NOTE]
>
>[!DNL Log Processing Dataset Include] de dossiers kunnen extra instructies voor de fase van de logboekverwerking van datasetconstructie bevatten. Deze dossiers bestaan binnen de folder van de Verwerking van het Logboek van de Dataset \ voor om het even welk geërft profiel. Zij bepalen typisch toepassing-specifieke parameters (zoals Web-specifieke configuratieparameters voor de toepassing van de Plaats). Voor informatie over [!DNL Log Processing Dataset Include] dossiers, zie [Dataset omvatten Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md). Voor informatie over Web-specifieke configuratieparameters voor Plaats, zie de Montages van de [Configuratie voor de Gegevens](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md)van het Web.

