---
description: Wanneer het vormen van uw dataset, kunt u variabelen, die als parameters worden bedoeld, bepalen om zinvolle waarden te vertegenwoordigen.
solution: Analytics
title: Het bepalen van Parameters in Dataset omvat Dossiers
topic: Data workbench
uuid: 1eb7d48c-a107-4b32-abca-55d30586813f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het bepalen van Parameters in Dataset omvat Dossiers{#defining-parameters-in-dataset-include-files}

Wanneer het vormen van uw dataset, kunt u variabelen, die als parameters worden bedoeld, bepalen om zinvolle waarden te vertegenwoordigen.

Om een waarde aan een parameter (namelijk om de parameter te bepalen) toe te wijzen, voegt u de naam en de waarde van de parameter aan de vector van Parameters in een logboekverwerking of [!DNL Transformation Dataset Include] dossier toe. Nadat u parameters bepaalt, kunt u hen in de configuratiedossiers van uw datasetprofiel van verwijzingen voorzien. Het bepalen van en het van verwijzingen voorzien van dergelijke parameters wordt bedoeld als parametersubstitutie. Het gebruiken van parametersubstitutie wanneer het vormen van uw dataset laat u toe om een gecentraliseerde plaats voor uw parameterdefinities tot stand te brengen. Wanneer u een parameter moet bijwerken die veelvoudige tijden of in veelvoudige dossiers van verwijzingen wordt voorzien, moet u de verandering slechts eenmaal aanbrengen.

>[!NOTE]
>
>In deze gids, is de term parameter gebruikt om naar de naam van om het even welke het plaatsen in een configuratiedossier (zoals de Voorwaarde van de Ingang van het Logboek, het Herproces, of Transformaties) te verwijzen. Nochtans, zoals gebruikt in deze sectie, verwijst de parameter specifiek naar een lid van de vector van Parameters in een dataset omvat dossier en niet aan de naam van het plaatsen in een configuratiedossier.

U zou de volgende punten moeten overwegen wanneer het bepalen van een parameter:

* Een parameter moet precies één keer worden bepaald. Daarom kunt u niet de zelfde variabele in veelvoudige dataset bepalen omvat dossiers.
* Om het even welke parameter die u bepaalt is lokaal aan of de logboekverwerking of de transformatiefasen, maar het is globaal over de veelvoudige dossiers van de datasetconfiguratie voor die fase. Bijvoorbeeld, als u een parameter in een [!DNL Transformation Dataset Include] dossier bepaalt, wordt de parameter bepaald voor de volledige transformatiefase, en u kunt het in het [!DNL Transformation.cfg] dossier en alle andere [!DNL Transformation Dataset Include] dossiers voor de geërfte profielen van verwijzingen voorzien. De parameter zou niet worden bepaald voor de verwerking van stamhout; daarom zouden om het even welke verwijzingen naar de parameter in het [!DNL Log Processing.cfg] dossier of een [!DNL Log Processing Dataset Include] dossier een verwerkingsfout produceren.

**Om een parameter te definiëren**

U kunt koord, numerieke, en vectorparameters in [!DNL Log Processing] en [!DNL Transformation Include] dossiers bepalen.

1. In het venster van de gegevenswerkbank voor het [!DNL Log Processing] of [!DNL Transformation Dataset Include] dossier, klik met de rechtermuisknop aan **[!UICONTROL Parameters]**, dan klik **[!UICONTROL Add new]** > **[!UICONTROL Parameter]**.

1. Selecteer **[!UICONTROL String Parameter]**, **[!UICONTROL Numeric Parameter]** of **[!UICONTROL Vector Parameter]**, en voltooi de parameters van de Naam en van de Waarde zoals die in de volgende secties worden beschreven.

1. Om de dataset te bewaren omvat dossier waarin u de parameter hebt bepaald, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

>[!NOTE]
>
>Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

**Om een parameter van verwijzingen te voorzien**

* Wanneer u een bepaalde parameter in een ander dossier van de datasetconfiguratie van verwijzingen voorziet, moet u zijn naam typen zoals [!DNL $(parameter name)].

De volgende secties beschrijven de types van parameters die u kunt bepalen.

* [Koord en Numerieke Parameters](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-string-num-param.md#concept-14f391ce107c4a3dad827ec7967f1080)
* [Vectorparameters](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-vector-param.md#concept-adb42a5474e245a9996d0aa8d5d522d0)

