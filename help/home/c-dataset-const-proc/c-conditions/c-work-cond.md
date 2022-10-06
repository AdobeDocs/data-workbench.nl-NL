---
description: Informatie over het toevoegen, verwijderen of kopiëren van een voorwaarde.
title: Werken met omstandigheden
uuid: b6f52b40-26aa-429b-9ff5-3f3b9c9d57a9
exl-id: 0792b308-aa0b-4741-be0c-4f7cc28f3e09
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# Werken met omstandigheden{#working-with-conditions}

{{eol}}

Informatie over het toevoegen, verwijderen of kopiëren van een voorwaarde.

* [Om een Voorwaarde aan een Dossier van de Configuratie van de Dataset toe te voegen](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-3e2a34db047b462585502f69722f6511)
* [Om een Voorwaarde uit een Dossier van de Configuratie van de Dataset te verwijderen](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-677270f93f1648c3a268ca2aea7d4540)
* [Een voorwaarde kopiëren](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-00617bcf2c274f428686b2ec7f2d1db8)

## Om een Voorwaarde aan een Dossier van de Configuratie van de Dataset toe te voegen {#section-3e2a34db047b462585502f69722f6511}

1. Tijdens het werken in uw datasetprofiel, gebruik [!DNL Profile Manager] om het gegevensbestand van de datasetconfiguratie te openen dat u wilt uitgeven.

   * Als u het dialoogvenster [!DNL Log Processing.cfg] bestand, zie [Het configuratiebestand voor logbestanden verwerken bewerken](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5).

   * Als u het dialoogvenster [!DNL Transformation.cfg] bestand, zie [Het configuratiebestand voor transformatie bewerken](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc).

   * Als u een [!DNL Dataset Include] bestand, zie [Gegevensset met bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. Zoek in het configuratiebestand van de gegevensset de parameter Voorwaarde of Voorwaarde voor logbestandvermelding die u wilt definiëren.
1. Klik met de rechtermuisknop op de parameter en klik op **[!UICONTROL Add new]**. Kies een van de volgende voorwaardetypen:

   * [!DNL Not Empty]
   * [!DNL String Match]
   * [!DNL Regular Expression]
   * [!DNL Range]
   * [!DNL And]
   * [!DNL Or]
   * [!DNL Neither]
   * [!DNL Compare]

1. Bewerk de parameters van de voorwaarde naar wens. Zie de desbetreffende sectie van dit aanhangsel voor beschrijvingen van de parameters van elke voorwaarde.
1. Als u uw wijzigingen wilt opslaan, klikt u met de rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager,] Klik met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > &lt;* **[!UICONTROL profile name]***>, waarbij de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot het dossier behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## Om een Voorwaarde uit een Dossier van de Configuratie van de Dataset te verwijderen {#section-677270f93f1648c3a268ca2aea7d4540}

1. Klik met de rechtermuisknop op de naam van de voorwaarde of op het nummer dat overeenkomt met de voorwaarde die u wilt verwijderen.
1. Klikken **[!UICONTROL Remove]** &lt;* **[!UICONTROL #number]***>, waarbij het getal het getal is dat overeenkomt met de voorwaarde die u wilt verwijderen.

## Een voorwaarde kopiëren {#section-00617bcf2c274f428686b2ec7f2d1db8}

U kunt een voorwaarde van één plaats aan een andere plaats in het zelfde dossier kopiëren, of u kunt een voorwaarde van één dossier van de datasetconfiguratie aan een andere kopiëren.

1. Klik met de rechtermuisknop op de naam van de voorwaarde of op het nummer dat overeenkomt met de voorwaarde die u wilt kopiëren en klik op **[!UICONTROL Copy]**.
1. Klik met de rechtermuisknop op de naam of het nummer van de voorwaarde waaronder u de gekopieerde voorwaarde wilt plaatsen en klik op **[!UICONTROL Paste]**.
