---
description: Wanneer het vormen van uw dataset, kunt u variabelen, die als parameters worden bedoeld, bepalen om betekenisvolle waarden te vertegenwoordigen.
title: Parameters definiëren in gegevensset met include-bestanden
uuid: 1eb7d48c-a107-4b32-abca-55d30586813f
exl-id: 80bb77e1-a157-4e16-9519-6d0e2ce17fe1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Parameters definiëren in gegevensset met include-bestanden{#defining-parameters-in-dataset-include-files}

{{eol}}

Wanneer het vormen van uw dataset, kunt u variabelen, die als parameters worden bedoeld, bepalen om betekenisvolle waarden te vertegenwoordigen.

Als u een waarde wilt toewijzen aan een parameter (de parameter definiëren), voegt u de naam en de waarde van de parameter toe aan de vector Parameters in een logverwerking of [!DNL Transformation Dataset Include] bestand. Nadat u parameters bepaalt, kunt u hen in de configuratiedossiers van het profiel van uw dataset van verwijzingen voorzien. Het definiëren van en verwijzen naar dergelijke parameters wordt parametervervanging genoemd. Het gebruiken van parametervervanging wanneer het vormen van uw dataset laat u toe om een gecentraliseerde plaats voor uw parameterdefinities tot stand te brengen. Wanneer u een parameter moet bijwerken waarnaar meerdere keren of in meerdere bestanden wordt verwezen, hoeft u de wijziging slechts één keer aan te brengen.

>[!NOTE]
>
>In deze gids, is de term parameter gebruikt om naar de naam van om het even welk die plaatsen in een configuratiedossier (zoals de Voorwaarde van de Ingang van het Logboek, Herbewerking, of Transformaties) te verwijzen. Nochtans, zoals gebruikt in deze sectie, verwijst de parameter specifiek naar een lid van de vector van Parameters in een dataset omvat dossier en niet naar de naam van het plaatsen in een configuratiedossier.

Bij het definiëren van een parameter moet u rekening houden met de volgende punten:

* Een parameter moet precies één keer worden gedefinieerd. Daarom kunt u niet de zelfde variabele in veelvoudige dataset bepalen omvat dossiers.
* Om het even welke parameter die u bepaalt is lokaal aan of de logboekverwerking of de transformatiefasen, maar het is globaal over veelvoudige dossiers van de datasetconfiguratie voor die fase. Als u bijvoorbeeld een parameter in een [!DNL Transformation Dataset Include] bestand, wordt de parameter gedefinieerd voor de gehele transformatiefase en kunt u ernaar verwijzen in het dialoogvenster [!DNL Transformation.cfg] bestand en alle andere [!DNL Transformation Dataset Include] bestanden voor de overgeërfde profielen. De parameter wordt niet gedefinieerd voor de verwerking van stamhout; verwijzingen naar de parameter in de [!DNL Log Processing.cfg] of een [!DNL Log Processing Dataset Include] zou een verwerkingsfout veroorzaken.

**Een parameter definiëren**

U kunt tekenreeks-, numerieke en vectorparameters definiëren in [!DNL Log Processing] en [!DNL Transformation Include] bestanden.

1. In het venster van de gegevenswerkbank voor [!DNL Log Processing] of [!DNL Transformation Dataset Include] bestand, klik met de rechtermuisknop **[!UICONTROL Parameters]** en klik vervolgens op **[!UICONTROL Add new]** > **[!UICONTROL Parameter]**.

1. Selecteren **[!UICONTROL String Parameter]**, **[!UICONTROL Numeric Parameter]**, of **[!UICONTROL Vector Parameter]** en vul de parameters Naam en Waarde in zoals beschreven in de volgende secties.

1. Als u het gegevensbestand wilt opslaan, bevat het bestand waarin u de parameter hebt gedefinieerd, klikt u met de rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

>[!NOTE]
>
>Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

**Naar een parameter verwijzen**

* Wanneer u naar een bepaalde parameter in een ander gegevensbestand van de datasetconfiguratie verwijst, moet u zijn naam als typen [!DNL $(parameter name)].

In de volgende secties worden de typen parameters beschreven die u kunt definiëren.

* [Tekenreeks en numerieke parameters](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-string-num-param.md#concept-14f391ce107c4a3dad827ec7967f1080)
* [Vectorparameters](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-vector-param.md#concept-adb42a5474e245a9996d0aa8d5d522d0)
