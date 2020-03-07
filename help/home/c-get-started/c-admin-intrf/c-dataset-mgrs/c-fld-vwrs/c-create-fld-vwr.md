---
description: U kunt een gebiedsviewer als callout van een gebiedsdeelkaart of als standalone visualisatie van het menu van Admin openen.
solution: Analytics
title: Creeer een gebiedskijker
topic: Data workbench
uuid: df48e728-96f9-4432-82c8-f8047840ffb9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Creeer een gebiedskijker{#create-a-field-viewer}

U kunt een gebiedsviewer als callout van een gebiedsdeelkaart of als standalone visualisatie van het menu van Admin openen.

## Creeer een gebiedsviewer van een gebiedsdeelkaart {#section-040cb83c902b49c48b841d35abc127e5}

Wanneer u een gebiedsviewer van een gebiedsdeelkaart (zoals aangetoond in de [Openende Kijkers](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-opn-field-vwrs.md#concept-0f0738ac50804a33818487222c337c27)van het Gebied) opent, is de kijker bevolkt automatisch gebaseerd op de logboekbron, de transformatie, of de afmeting die u met de rechtermuisknop aanklikt. Voor een logboekbron of een transformatie, zijn de gebieden in de kijker input of output van de logboekbron of transformatie. Voor een afmeting, zijn de gebieden input van de afmeting. U kunt gebieden toevoegen en verwijderen zoals gewenst.

## Creeer een gebiedskijkers als standalone visualisatie {#section-11d10e46631d4fdca45d7534336e1e80}

Wanneer u een gebiedskijker als standalone visualisatie opent, kunt u een [!DNL Log Processing Field Viewer] of een [!DNL Transformation Field Viewer]creëren. De kijker is leeg, en u moet de gewenste gebieden aan de kijker toevoegen. Voor een [!DNL Log Processing Field Viewer], kunt u gebieden van het [!DNL Log Processing.cfg] dossier of om het even welk [!DNL Log Processing dataset include] dossier toevoegen. Voor een [!DNL Transformation Field Viewer], kunt u gebieden van het [!DNL Transformation.cfg] dossier of om het even welk [!DNL Transformation dataset include] dossier toevoegen.

Voor meer informatie over configuratie en omvat dossiers, zie de Gids *van de Configuratie van de* Dataset.

## Een veld toevoegen en verwijderen {#section-9c0d4f5735a044a8b21dc7a99c63a59a}

**Om een gebied aan een gebiedskijker toe te voegen**

* Klik binnen de gebiedskijker met de rechtermuisknop aan en klik **[!UICONTROL Fields]** > *&lt;**[!UICONTROL field name]**>* > *&lt;**[!UICONTROL instance]**>*.

   -of-

* Klik in een bestaande kolom in de veldviewer met de rechtermuisknop en klik **[!UICONTROL Fields]** > *&lt;**[!UICONTROL field name]**>* > *&lt;**[!UICONTROL instance]**>*.

De naam van het gebied verwijst naar de naam van het gebied, en de instantie verwijst naar waar in de datasetconfiguratie het gebied wordt gebruikt, zoals een gegevenssetverwerkingsstadium of een transformatie. Sommige gebieden worden gebruikt in veelvoudige plaatsen binnen de datasetconfiguratie (bijvoorbeeld, kan een gebied door veelvoudige transformaties) worden gewijzigd, zodat moet u selecteren welke instantie van het gebied om aan uw gebiedskijker toe te voegen.

In de lijst van beschikbare gebieden, verschijnt X links van om het even welk gebied dat reeds in de kijker wordt getoond.

**Om een gebied uit een gebiedskijker te verwijderen**

* Klik binnen de kolom voor het gebied met de rechtermuisknop aan dat u wilt verwijderen en klikken **[!UICONTROL Remove Field]**.

