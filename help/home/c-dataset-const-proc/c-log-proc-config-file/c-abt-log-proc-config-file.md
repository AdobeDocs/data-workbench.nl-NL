---
description: Het dossier van Logboek Processing.cfg controleert de fase van de logboekverwerking van datasetconstructie, waarin de ongeordende gegevens van de gegevensbronnen (die als logboekbronnen worden bedoeld) worden gelezen, en de filters en de transformaties worden toegepast op de gegevens.
title: Het configuratiebestand voor logbestanden verwerken
uuid: 1f5f5d75-8a24-4122-adc8-8c8aef916631
exl-id: 11ee3298-272d-46c8-bcfe-e485b01606b1
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Info over het configuratiebestand {#about-the-log-processing-configuration-file} voor de logbestandverwerking

Het dossier van Logboek Processing.cfg controleert de fase van de logboekverwerking van datasetconstructie, waarin de ongeordende gegevens van de gegevensbronnen (die als logboekbronnen worden bedoeld) worden gelezen, en de filters en de transformaties worden toegepast op de gegevens.

U moet het [!DNL Log Processing.cfg] dossier uitgeven om het even welke volgende taken van de datasetconfiguratie uit te voeren:

* Logbronnen opgeven. Zie [Logbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md).
* Bepalen welke logingangen de dataset tijdens logboekverwerking ingaan. Zie [Gegevensfilters](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md) en [Logboekinvoervoorwaarde](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).

* Het splitsen van tracking-id&#39;s met grote hoeveelheden gebeurtenisgegevens inschakelen. Zie [Key Splitting](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).
* Een gegevensworkbench-server configureren om als een bestandsservereenheid te worden uitgevoerd. Zie [Een Eenheid van de Server van het Dossier van de Server van het Inzicht vormen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).
* Het vormen van een server van de gegevenswerkbank om als gecentraliseerde normalisatieserver te lopen. Zie [Een Eenheid van de Server van het Dossier van de Server van het Inzicht vormen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

>[!NOTE]
>
>[!DNL Log Processing Dataset Include] de dossiers kunnen extra instructies voor de fase van de logboekverwerking van datasetbouw bevatten. Deze bestanden staan in de map Gegevensset\Log Processing voor een overgeërfd profiel. Zij bepalen typisch toepassing-specifieke parameters (zoals Web-specifieke configuratieparameters voor de toepassing van de Plaats). Voor informatie over [!DNL Log Processing Dataset Include] dossiers, zie [Dataset omvat Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md). Voor informatie over web-specific configuratieparameters voor Plaats, zie [Montages van de Configuratie voor Gegevens van het Web](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md).
