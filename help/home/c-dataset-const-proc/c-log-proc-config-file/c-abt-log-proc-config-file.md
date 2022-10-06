---
description: Het dossier van Logboek Processing.cfg controleert de fase van de logboekverwerking van datasetconstructie, waarin de ongeordende gegevens van de gegevensbronnen (die als logboekbronnen worden bedoeld) worden gelezen, en de filters en de transformaties worden toegepast op de gegevens.
title: Het configuratiebestand voor logbestanden verwerken
uuid: 1f5f5d75-8a24-4122-adc8-8c8aef916631
exl-id: 11ee3298-272d-46c8-bcfe-e485b01606b1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Het configuratiebestand voor logbestanden verwerken{#about-the-log-processing-configuration-file}

{{eol}}

Het dossier van Logboek Processing.cfg controleert de fase van de logboekverwerking van datasetconstructie, waarin de ongeordende gegevens van de gegevensbronnen (die als logboekbronnen worden bedoeld) worden gelezen, en de filters en de transformaties worden toegepast op de gegevens.

U moet de [!DNL Log Processing.cfg] dossier om het even welke volgende taken van de datasetconfiguratie uit te voeren:

* Logbronnen opgeven. Zie [Logbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md).
* Bepalen welke logingangen de dataset tijdens logboekverwerking ingaan. Zie [Gegevensfilters](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md) en [Voorwaarde logbestandvermelding](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).

* Het splitsen van tracking-id&#39;s met grote hoeveelheden gebeurtenisgegevens inschakelen. Zie [Key Splitsen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).
* Een gegevensworkbench-server configureren om als een bestandsservereenheid te worden uitgevoerd. Zie [Een Insight Server-bestandsservereenheid configureren](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).
* Het vormen van een server van de gegevenswerkbank om als gecentraliseerde normalisatieserver te lopen. Zie [Een Insight Server-bestandsservereenheid configureren](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

>[!NOTE]
>
>[!DNL Log Processing Dataset Include] de dossiers kunnen extra instructies voor de fase van de logboekverwerking van datasetbouw bevatten. Deze bestanden staan in de map Gegevensset\Log Processing voor een overgeërfd profiel. Zij bepalen typisch toepassing-specifieke parameters (zoals Web-specifieke configuratieparameters voor de toepassing van de Plaats). Voor informatie over [!DNL Log Processing Dataset Include] bestanden, zie [Gegevensset met bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md). Voor informatie over web-specifieke configuratieparameters voor Plaats, zie [Configuratie-instellingen voor webgegevens](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md).
