---
description: Informatie over hoe te om parameters in het Transform.cfg- dossier te specificeren dat op de verscheidene scenario's wordt gebaseerd.
title: Voorbeeld van Data Workbench Transform.cfg-bestanden
uuid: cb473a5a-54e2-4bf7-84fb-c9c27910ef64
exl-id: f7aadde4-6d89-4bd4-b34b-192a81a71dc3
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Voorbeeld van Data Workbench Transform.cfg-bestanden{#sample-data-workbench-transform-cfg-files}

{{eol}}

Informatie over hoe te om parameters in het Transform.cfg- dossier te specificeren dat op de verscheidene scenario&#39;s wordt gebaseerd.

* [Een eenvoudig Insight Transform.cfg-bestand](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-b7e83cafa3a947c597bd09d316930190)
* [Uitvoer met door komma&#39;s gescheiden waarden](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-03916934ad574efc8695abbae54a1816)
* [Voorbeeldlogbestanden](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-113b3b0c0c7547ea9536bb2f465c0875)
* [Logbestanden splitsen op websitesectie](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-2cac205cd3934d31abb6c6ed8780196d)

In elk voorbeeld wordt het bestand weergegeven als een [!DNL Transform.cfg] venster in de werkbank voor gegevens.

## Een eenvoudig Data Workbench Transform.cfg-bestand {#section-b7e83cafa3a947c597bd09d316930190}

Het volgende [!DNL Transform.cfg] venster bevat instructies voor het lezen van [!DNL .vsl] bestanden van de [!DNL Logs] en exporteer de velden x-timestring en x-trackingid naar een tekstbestand dat is opgeslagen in de map Logs\VT. Omdat er geen periode voor het roteren van het bestand of de indeling van de naam van het uitvoerbestand is opgegeven, bevat elk bestand gegevens voor één kalenderdag en heeft het een naam in de standaardindeling [!DNL %yyyy%%mm%%dd%-%x-mask%.txt].

![](assets/cfg_VisualTransform_SimpleExample.png)

## Uitvoer met door komma&#39;s gescheiden waarden {#section-03916934ad574efc8695abbae54a1816}

Het volgende [!DNL Transform.cfg] venster bevat instructies voor het lezen van [!DNL .vsl] bestanden in de map Logs en exporteer de velden 0 tot en met 13 naar een komma als scheidingsteken ( [!DNL .csv]) opgeslagen in de map Logs\VT\CSV. Omdat er geen periode voor het roteren van bestanden is opgegeven, bevat elk bestand gegevens voor één kalenderdag. De uitvoerbestanden zijn [!DNL .csv] bestanden met een naam in de indeling [!DNL %yyyy%%mm%%dd%-%x-mask%.csv].

![](assets/cfg_VisualTransform_CSVExample.png)

## Voorbeeldlogbestanden {#section-113b3b0c0c7547ea9536bb2f465c0875}

U kunt transformatiefunctionaliteit configureren om een bijgewerkte, compacte versie van uw volledige logbestanden te maken en te onderhouden. Dit laat u toe om uw datasetconfiguraties, met herverwerkingstijden van seconden of notulen in plaats van uren snel te testen nodig om de volledige dataset opnieuw te verwerken. In het volgende voorbeeld ziet u hoe u de transformatiefunctionaliteit kunt configureren om dit te doen.

Het volgende [!DNL Transform.cfg] venster bevat instructies voor het lezen van [!DNL .vsl] bestanden uit de map Logs en exporteer de velden x-timestring en x-trackingid naar een tekstbestand dat is opgeslagen in de map Logs\VT. De gespecificeerde Drempel van de Hash filters bepaalde het volgen IDs van de dataset, daardoor creërend een dataset die door een factor van 100 wordt bemonsterd. Omdat er geen periode voor het roteren van bestanden is opgegeven, bevat elk bestand gegevens voor één kalenderdag. De namen van de uitvoerbestanden hebben de standaardindeling [!DNL %yyyy%%mm%%dd%-%x-mask%.txt].

![](assets/cfg_VisualTransform_SampledExample.png)

## Logbestanden splitsen op websitesectie {#section-2cac205cd3934d31abb6c6ed8780196d}

Het volgende [!DNL Transform.cfg] venster bevat instructies voor het lezen van [!DNL .vsl]bestanden uit de map Logs en exporteer de velden x-timestring en x-trackingid naar een tekstbestand dat is opgeslagen in de map Logs\VT. De transformatie van de reguliere expressie ( [!DNL RETransform]) neemt als invoer het cs-uri-stentelveld en maakt een nieuw veld (x-site) dat een sectie van de site definieert. Het veld x-site wordt opgenomen in de naam van uitvoertekstbestanden, die elk gegevens voor één kalenderdag bevatten.

![](assets/cfg_VisualTransform_SplittingExample.png)
