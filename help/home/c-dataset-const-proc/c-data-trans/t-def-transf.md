---
description: U kunt gegevenstransformaties bepalen die tijdens of de de logboekverwerking of transformatiefase van datasetconstructie moeten worden toegepast.
solution: Analytics
title: Een transformatie definiëren
topic: Data workbench
uuid: 69dd667b-e465-4c1a-a20e-4384e8988cd0
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Een transformatie definiëren{#defining-a-transformation}

U kunt gegevenstransformaties bepalen die tijdens of de de logboekverwerking of transformatiefase van datasetconstructie moeten worden toegepast.

>[!NOTE]
>
>Adobe adviseert bepalend transformaties in of [!DNL Log Processing] of [!DNL Transformation Dataset Include] dossiers in plaats van binnen [!DNL Log Processing.cfg] of [!DNL Transformation.cfg].

De volgende transformaties werken slechts wanneer bepaald in het [!DNL Transformation.cfg] dossier of in een [!DNL Transformation Dataset Include] dossier:

* [](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-uri-transf/c-appenduri.md#concept-a0df05dd958645bf8219fc7b0b675ee4)ToevoegenURII
* [Kruisrijen](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-crossrows.md#concept-fcace08804f54db397ed631cc13ff4f2)
* [LookupRows](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-lookuprows.md#concept-4bd9a1f13ee243e592a6a0008053134f)
* [ODBC-gegevensbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3)
* [Sessionize](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-sessionize.md#concept-b1af95c8cba34b248f86de883d914bc0)

**Om een transformatie te definiëren**

1. Gebruik het [!DNL Profile Manager] om het dossier van de datasetconfiguratie te openen waarin u de transformatie wilt bepalen.

   * (Geadviseerd) om een dataset te openen omvat dossier, zie de [Dataset Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)omvat.
   * Om het [!DNL Log Processing.cfg] dossier te openen, zie het [Uitgeven van het Dossier](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5)van de Configuratie van de Verwerking van het Logboek.

   * Om het [!DNL Transformation.cfg] dossier te openen, zie het [Uitgeven van het Dossier](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc)van de Configuratie van de Transformatie.

1. Klik met de rechtermuisknop **[!UICONTROL Transformations]** en klik vervolgens op **[!UICONTROL Add new]** > *&lt;**[!UICONTROL Transformation type]**>*.
1. Voer de juiste gegevens in voor uw transformatie. Voor beschrijvingen van de transformatietypen en informatie over hun parameters, zie de volgende secties:

   * [Standaardtransformaties](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-standard-transf.md#concept-25f4bdbf8fe74c4aaeb2fcd226243886)
   * [URI-transformaties](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-uri-transf/c-uri-transf.md#concept-2dfa0ffcd83d4fb69c1f42ad50dea125)
   * [Integratie van zoekgegevens](../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-int-lookup-data.md#concept-08ff70769a464f50ab14299a344f05c7)

1. Nadat u uw transformatie(s) in het configuratiebestand hebt gedefinieerd, slaat u het bestand lokaal op en slaat u het op in uw datasetprofiel op de gegevenswerkbankserver.

       Tips voor het definiëren en bewerken van transformaties:
   
   * Wanneer u de configuratie van een transformatie bewerkt in een venster van een gegevensbank, kunt u sneltoetsen gebruiken voor de basisbewerkingsfuncties, zoals cut (Ctrl+x), copy (Ctrl+c), paste (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klik+drag) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst of volledige transformatiedefinities van één configuratiedossier () aan een andere te kopiëren en te kleven. [!DNL .cfg]
   * Voor om het even welke transformatie die u bepaalt, kunt u één of meerdere commentaarlijnen aan de parameter van Commentaren toevoegen om de transformatie verder te beschrijven of nota&#39;s over zijn gebruik toe te voegen. Om een commentaar toe te voegen die gegevenswerkbank gebruikt, klik het **[!UICONTROL Comments]** etiket met de rechtermuisknop aan, dan klik **[!UICONTROL Add new]** > **[!UICONTROL Comment Line]**.

   * U kunt de configuratie van om het even welke transformatie van een openen [!DNL Transformation Dependency Map]. Nadat u de configuratie opent, kunt u het uitgeven en uw veranderingen bewaren. Voor informatie over [!DNL Transformation Dependency Maps], zie de Hulpmiddelen van de Configuratie van de [Dataset](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

   * Een lege koordoutput van een transformatie kan een niet lege koord op het outputgebied beschrijven.

