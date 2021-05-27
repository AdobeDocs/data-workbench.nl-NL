---
description: U kunt gegevenstransformaties bepalen die tijdens of de logboekverwerking of transformatiefase van datasetconstructie moeten worden toegepast.
title: Een transformatie definiëren
uuid: 69dd667b-e465-4c1a-a20e-4384e8988cd0
exl-id: 61ce8093-9e64-419a-bddc-dc2225c0eaab
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Een transformatie definiëren{#defining-a-transformation}

U kunt gegevenstransformaties bepalen die tijdens of de logboekverwerking of transformatiefase van datasetconstructie moeten worden toegepast.

>[!NOTE]
>
>Adobe raadt aan transformaties te definiëren in [!DNL Log Processing]- of [!DNL Transformation Dataset Include]-bestanden in plaats van in [!DNL Log Processing.cfg] of [!DNL Transformation.cfg].

De volgende transformaties werken alleen wanneer deze zijn gedefinieerd in het [!DNL Transformation.cfg]-bestand of in een [!DNL Transformation Dataset Include]-bestand:

* [](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-uri-transf/c-appenduri.md#concept-a0df05dd958645bf8219fc7b0b675ee4)AppendURII
* [CrossRows](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-crossrows.md#concept-fcace08804f54db397ed631cc13ff4f2)
* [LookupRows](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-lookuprows.md#concept-4bd9a1f13ee243e592a6a0008053134f)
* [ODBC-gegevensbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3)
* [Sessioneren](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-sessionize.md#concept-b1af95c8cba34b248f86de883d914bc0)

**Een transformatie definiëren**

1. Gebruik [!DNL Profile Manager] om het dossier van de datasetconfiguratie te openen waarin u de transformatie wilt bepalen.

   * (Aanbevolen) Een dataset openen omvat dossier, zie [Dataset omvat Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).
   * Als u het [!DNL Log Processing.cfg]-bestand wilt openen, raadpleegt u [Het configuratiebestand voor logbestanden verwerken bewerken](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5).

   * Als u het [!DNL Transformation.cfg]-bestand wilt openen, raadpleegt u [Het configuratiebestand voor transformatie bewerken](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc).

1. Klik met de rechtermuisknop **[!UICONTROL Transformations]** en klik vervolgens op **[!UICONTROL Add new]** > *&lt;**[!UICONTROL Transformation type]**>*.
1. Voer de juiste gegevens in voor de transformatie. Zie de volgende secties voor beschrijvingen van de transformatietypen en informatie over de parameters ervan:

   * [Standaardtransformaties](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-standard-transf.md#concept-25f4bdbf8fe74c4aaeb2fcd226243886)
   * [URI-transformaties](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-uri-transf/c-uri-transf.md#concept-2dfa0ffcd83d4fb69c1f42ad50dea125)
   * [Opzoekgegevens integreren](../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-int-lookup-data.md#concept-08ff70769a464f50ab14299a344f05c7)

1. Nadat u de transformaties in het configuratiebestand hebt gedefinieerd, slaat u het bestand lokaal op en slaat u het op in uw gegevenssetprofiel op de gegevenswerkbankserver.

       Tips voor het definiëren en bewerken van transformaties:
   
   * Wanneer u de configuratie van een transformatie bewerkt in een werkbankvenster, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals cut (Ctrl+x), copy (Ctrl+c), paste (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst of volledige transformatiedefinities van één configuratiedossier ( [!DNL .cfg]) aan een ander te kopiëren en te kleven.
   * Voor elke transformatie die u definieert, kunt u een of meer opmerkingsregels toevoegen aan de parameter Comments om de transformatie verder te beschrijven of notities over het gebruik ervan toe te voegen. Als u een opmerking wilt toevoegen met gebruik van de gegevenswerkbank, klikt u met de rechtermuisknop op het label **[!UICONTROL Comments]** en vervolgens op **[!UICONTROL Add new]** > **[!UICONTROL Comment Line]**.

   * U kunt de configuratie van om het even welke transformatie van [!DNL Transformation Dependency Map] openen. Nadat u de configuratie opent, kunt u het uitgeven en uw veranderingen bewaren. Voor informatie over [!DNL Transformation Dependency Maps], zie [Hulpmiddelen van de Configuratie van de Dataset](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

   * Een lege tekenreeksuitvoer van een transformatie kan een niet-lege tekenreeks in het uitvoerveld overschrijven.
