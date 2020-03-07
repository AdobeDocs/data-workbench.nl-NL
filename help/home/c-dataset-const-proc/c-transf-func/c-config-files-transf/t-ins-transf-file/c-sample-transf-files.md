---
description: Informatie over hoe te om parameters in het dossier te specificeren Transform.cfg dat op de verscheidene scenario's wordt gebaseerd.
solution: Analytics
title: Voorbeeld van gegevenswerkbankbestanden Transform.cfg
topic: Data workbench
uuid: cb473a5a-54e2-4bf7-84fb-c9c27910ef64
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Voorbeeld van gegevenswerkbankbestanden Transform.cfg{#sample-data-workbench-transform-cfg-files}

Informatie over hoe te om parameters in het dossier te specificeren Transform.cfg dat op de verscheidene scenario&#39;s wordt gebaseerd.

* [Een eenvoudig dossier van Transform.cfg van het Inzicht](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-b7e83cafa3a947c597bd09d316930190)
* [Uitvoer met komma-gescheiden Waarden](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-03916934ad574efc8695abbae54a1816)
* [Bemonsterde logboekdossiers](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-113b3b0c0c7547ea9536bb2f465c0875)
* [Het verdelen van de Dossiers van het Logboek door de Sectie van de Website](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-2cac205cd3934d31abb6c6ed8780196d)

In elke steekproef, wordt het dossier getoond als [!DNL Transform.cfg] venster in gegevenswerkbank.

## Een eenvoudig dossier van Transform.cfg van de Werkbank van Gegevens {#section-b7e83cafa3a947c597bd09d316930190}

Het volgende [!DNL Transform.cfg] venster verstrekt instructies om [!DNL .vsl] dossiers van de [!DNL Logs] folder te lezen en de x-timestring en x-trackingid gebieden naar een tekstdossier uit te voeren dat in de folder van Logs \ VT wordt opgeslagen. Omdat geen de periode van de dossieromwenteling of formaat van het outputdossier - noem wordt gespecificeerd, bevat elk dossier gegevens voor één kalenderdag en heeft een naam in het standaardformaat [!DNL %yyyy%%mm%%dd%-%x-mask%.txt].

![](assets/cfg_VisualTransform_SimpleExample.png)

## Uitvoer met komma-gescheiden Waarden {#section-03916934ad574efc8695abbae54a1816}

Het volgende [!DNL Transform.cfg] venster verstrekt instructies om [!DNL .vsl] [!DNL .csv]dossiers van de folder van Logs en de uitvoergebieden 0 door 13 te lezen aan een komma-afgebakend () dossier dat in Logs\VT\CSV directory wordt opgeslagen. Omdat geen periode van de dossieromwenteling wordt gespecificeerd, bevat elk dossier gegevens voor één kalenderdag. De outputdossiers zijn [!DNL .csv] dossiers die in het formaat worden genoemd [!DNL %yyyy%%mm%%dd%-%x-mask%.csv].

![](assets/cfg_VisualTransform_CSVExample.png)

## Voorbeeldlogbestanden {#section-113b3b0c0c7547ea9536bb2f465c0875}

U kunt transformatiefunctionaliteit vormen om een bijgewerkte, compacte versie van uw volledige logboekdossiers tot stand te brengen en te handhaven. Het doen laat u toe om uw datasetconfiguraties snel, met opwerkingstijden van seconden of notulen in plaats van uren te testen nodig om de volledige dataset opnieuw te verwerken. Het volgende voorbeeld verstrekt een voorbeeld van hoe te om transformatiefunctionaliteit te vormen om dit te doen.

Het volgende [!DNL Transform.cfg] venster verstrekt instructies om [!DNL .vsl] dossiers van de folder van Logs te lezen en de x-timestring en x-trackingid gebieden naar een tekstdossier uit te voeren dat in de folder van Logs \ VT wordt opgeslagen. De gespecificeerde filters van de Drempel van de Hash bepaalde het volgen IDs van de dataset, daardoor creërend een dataset die door een factor 100 wordt bemonsterd. Omdat geen periode van de dossieromwenteling wordt gespecificeerd, bevat elk dossier gegevens voor één kalenderdag. De namen van de outputdossiers zijn in het standaardformaat [!DNL %yyyy%%mm%%dd%-%x-mask%.txt].

![](assets/cfg_VisualTransform_SampledExample.png)

## Het verdelen van de Dossiers van het Logboek door de Sectie van de Website {#section-2cac205cd3934d31abb6c6ed8780196d}

Het volgende [!DNL Transform.cfg] venster verstrekt instructies om [!DNL .vsl]dossiers van de folder van Logs te lezen en de x-timestring en x-trackingid gebieden naar een tekstdossier uit te voeren dat in de folder van Logs \ VT wordt opgeslagen. De normale uitdrukkingstransformatie ( [!DNL RETransform]) neemt als input het cs-uri-stengebied en leidt tot een nieuw gebied (x-plaats) dat een sectie van de plaats bepaalt. Het x-plaatsgebied is inbegrepen in de naam van de dossiers van de outputtekst, elk waarvan gegevens voor één kalenderdag bevatten.

![](assets/cfg_VisualTransform_SplittingExample.png)

