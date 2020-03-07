---
description: Het dossier Transformation.cfg controleert de transformatiefase van datasetconstructie waarin de extra gegevenstransformaties worden toegepast op gegevens die reeds tijdens logboekverwerking worden verwerkt om uitgebreide afmetingen voor gebruik in analyse tot stand te brengen.
solution: Analytics
title: Ongeveer het Dossier van de Configuratie van de Transformatie
topic: Data workbench
uuid: 56e11b71-1a86-47d4-8d2a-2795532b0770
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Ongeveer het Dossier van de Configuratie van de Transformatie{#about-the-transformation-configuration-file}

Het dossier Transformation.cfg controleert de transformatiefase van datasetconstructie waarin de extra gegevenstransformaties worden toegepast op gegevens die reeds tijdens logboekverwerking worden verwerkt om uitgebreide afmetingen voor gebruik in analyse tot stand te brengen.

U moet het [!DNL Transformation.cfg] dossier uitgeven om het even welke volgende taken van de datasetconfiguratie uit te voeren:

* Het filtreren van gegevens van logboekverwerking door het [!DNL log entry condition] voor transformatie te bepalen.
* Het plaatsen van de tijdzone die voor het creëren van tijdafmetingen en het maken van tijdomzettingen moet worden gebruikt. Zie [Tijdzones](../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956).

>[!NOTE]
>
>[!DNL Transformation Dataset Include] de dossiers kunnen extra instructies voor de transformatiefase van datasetconstructie bevatten. Deze dossiers bestaan binnen de folder van de Transformatie van de Dataset \ voor om het even welk geërft profiel, en zij bepalen typisch toepassing-specifieke parameters (zoals Web-specifieke configuratieparameters voor de [!DNL Site] toepassing). Voor informatie over [!DNL Transformation Dataset Include] dossiers, zie [Dataset omvatten Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md). Voor informatie over Web-specifieke configuratieparameters voor Plaats, zie de Montages van de [Configuratie voor de Gegevens](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)van het Web.

