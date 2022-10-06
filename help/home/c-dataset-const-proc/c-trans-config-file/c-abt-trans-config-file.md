---
description: Het Transformation.cfg- dossier controleert de transformatiefase van datasetbouw waarin de extra gegevenstransformaties worden toegepast op gegevens die reeds tijdens logboekverwerking worden verwerkt om uitgebreide afmetingen voor gebruik in analyse tot stand te brengen.
title: Informatie over het configuratiebestand voor transformatie
uuid: 56e11b71-1a86-47d4-8d2a-2795532b0770
exl-id: 860562d7-6ed3-486b-9f62-1bd06878bf7e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Informatie over het configuratiebestand voor transformatie{#about-the-transformation-configuration-file}

{{eol}}

Het Transformation.cfg- dossier controleert de transformatiefase van datasetbouw waarin de extra gegevenstransformaties worden toegepast op gegevens die reeds tijdens logboekverwerking worden verwerkt om uitgebreide afmetingen voor gebruik in analyse tot stand te brengen.

U moet de [!DNL Transformation.cfg] dossier om het even welke volgende taken van de datasetconfiguratie uit te voeren:

* Gegevens van logboekverwerking filteren door het [!DNL log entry condition] voor transformatie.
* De tijdzone instellen die moet worden gebruikt voor het maken van tijddimensies en het maken van tijdconversies. Zie [Tijdzones](../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956).

>[!NOTE]
>
>[!DNL Transformation Dataset Include] bestanden kunnen aanvullende instructies bevatten voor de transformatiefase van de constructie van gegevenssets. Deze bestanden bevinden zich in de map Dataset\Transformation voor een overgeërfd profiel en definiëren doorgaans toepassingsspecifieke parameters (zoals webspecifieke configuratieparameters voor de [!DNL Site] toepassing). Voor informatie over [!DNL Transformation Dataset Include] bestanden, zie [Gegevensset met bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md). Voor informatie over web-specifieke configuratieparameters voor Plaats, zie [Configuratie-instellingen voor webgegevens](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).
