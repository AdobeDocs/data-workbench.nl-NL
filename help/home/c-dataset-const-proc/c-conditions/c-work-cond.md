---
description: Informatie over het toevoegen van, het verwijderen van, of het kopiëren van een voorwaarde.
solution: Analytics
title: Werken onder omstandigheden
topic: Data workbench
uuid: b6f52b40-26aa-429b-9ff5-3f3b9c9d57a9
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Werken onder omstandigheden{#working-with-conditions}

Informatie over het toevoegen van, het verwijderen van, of het kopiëren van een voorwaarde.

* [Om een voorwaarde aan een Dossier van de Configuratie van de Dataset toe te voegen](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-3e2a34db047b462585502f69722f6511)
* [Om een Voorwaarde uit een Dossier van de Configuratie van de Dataset te verwijderen](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-677270f93f1648c3a268ca2aea7d4540)
* [Om een voorwaarde te kopiëren](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-00617bcf2c274f428686b2ec7f2d1db8)

## Om een voorwaarde aan een Dossier van de Configuratie van de Dataset toe te voegen {#section-3e2a34db047b462585502f69722f6511}

1. Terwijl het werken in uw datasetprofiel, gebruik [!DNL Profile Manager] om het dossier van de datasetconfiguratie te openen dat u wilt uitgeven.

   * Om het [!DNL Log Processing.cfg] dossier te openen, zie het [Uitgeven van het Dossier](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5)van de Configuratie van de Verwerking van het Logboek.

   * Om het [!DNL Transformation.cfg] dossier te openen, zie het [Uitgeven van het Dossier](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc)van de Configuratie van de Transformatie.

   * Een [!DNL Dataset Include] dossier openen, zie [Dataset omvat Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. Binnen het dossier van de datasetconfiguratie, bepaal de plaats van de de Voorwaarde of parameter van de Voorwaarde van de Ingang van het Logboek die u zou willen bepalen.
1. Klik met de rechtermuisknop op de parameter en klik op **[!UICONTROL Add new]**. Kies één van de volgende voorwaardentypes:

   * [!DNL Not Empty]
   * [!DNL String Match]
   * [!DNL Regular Expression]
   * [!DNL Range]
   * [!DNL And]
   * [!DNL Or]
   * [!DNL Neither]
   * [!DNL Compare]

1. Geef de parameters van de voorwaarde uit zoals gewenst. Zie voor beschrijvingen van de parameters van elke toestand het desbetreffende punt van dit aanhangsel.
1. Om uw veranderingen te bewaren, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

1. Als u de lokaal aangebrachte wijzigingen wilt doorvoeren, klikt u met de [!DNL Profile Manager,] rechtermuisknop op het vinkje voor het bestand in de [!DNL User] kolom en klikt u op **[!UICONTROL Save to]** > &lt;* **[!UICONTROL profile name]***>, waarbij de profielnaam de naam is van het gegevenssetprofiel of het geërfte profiel waartoe het bestand behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## Om een Voorwaarde uit een Dossier van de Configuratie van de Dataset te verwijderen {#section-677270f93f1648c3a268ca2aea7d4540}

1. Klik de naam van de voorwaarde of het aantal met de rechtermuisknop aan die aan de voorwaarde beantwoorden dat u wilt verwijderen.
1. Klik op **[!UICONTROL Remove]** &lt;* **[!UICONTROL #number]***>, waarbij het nummer overeenkomt met de voorwaarde die u wilt verwijderen.

## Om een voorwaarde te kopiëren {#section-00617bcf2c274f428686b2ec7f2d1db8}

U kunt een voorwaarde van één plaats aan een andere plaats in het zelfde dossier kopiëren, of u kunt een voorwaarde van één dossier van de datasetconfiguratie aan een andere kopiëren.

1. Klik de naam van de voorwaarde of het aantal met de rechtermuisknop aan die aan de voorwaarde beantwoorden dat u wilt kopiëren en klikken **[!UICONTROL Copy]**.
1. Klik de naam of het aantal van de voorwaarde met de rechtermuisknop aan waaronder u de gekopieerde voorwaarde wilt plaatsen en klikken **[!UICONTROL Paste]**.

