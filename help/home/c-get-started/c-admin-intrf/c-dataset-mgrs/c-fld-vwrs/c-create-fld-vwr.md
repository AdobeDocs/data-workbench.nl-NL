---
description: U kunt een veldviewer openen als een bijschrift van een afhankelijkheidskaart of als een zelfstandige visualisatie in het menu Beheer.
title: Een veldviewer maken
uuid: df48e728-96f9-4432-82c8-f8047840ffb9
exl-id: a2563dbb-1d1f-4ed8-b73b-6ac7a2687405
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Een veldviewer maken{#create-a-field-viewer}

U kunt een veldviewer openen als een bijschrift van een afhankelijkheidskaart of als een zelfstandige visualisatie in het menu Beheer.

## Een veldviewer maken op basis van een afhankelijkheidskaart {#section-040cb83c902b49c48b841d35abc127e5}

Wanneer u een veldviewer opent vanuit een afhankelijkheidskaart (zoals wordt weergegeven in [Veldviewers openen](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-opn-field-vwrs.md#concept-0f0738ac50804a33818487222c337c27)), wordt de viewer automatisch gevuld op basis van de logbron, transformatie of dimensie waarop u met de rechtermuisknop klikt. Voor een logbron of transformatie zijn de velden in de viewer invoer of uitvoer van de logbron of transformatie. Voor een dimensie zijn de velden invoer van de dimensie. Desgewenst kunt u velden toevoegen en verwijderen.

## Een veldviewer maken als zelfstandige visualisatie {#section-11d10e46631d4fdca45d7534336e1e80}

Wanneer u een veldviewer opent als een zelfstandige visualisatie, kunt u een [!DNL Log Processing Field Viewer] of [!DNL Transformation Field Viewer] maken. De viewer is leeg en u moet de gewenste velden toevoegen aan de viewer. Voor een [!DNL Log Processing Field Viewer], kunt u gebieden van [!DNL Log Processing.cfg] dossier of om het even welk [!DNL Log Processing dataset include] dossier toevoegen. Voor een [!DNL Transformation Field Viewer], kunt u gebieden van [!DNL Transformation.cfg] dossier of om het even welk [!DNL Transformation dataset include] dossier toevoegen.

Voor meer informatie over configuratie en omvat dossiers, zie *de Gids van de Configuratie van de Dataset*.

## Veld {#section-9c0d4f5735a044a8b21dc7a99c63a59a} toevoegen en verwijderen

**Een veld toevoegen aan een veldviewer**

* Klik met de rechtermuisknop in de veldviewer en klik op **[!UICONTROL Fields]** > *&lt;**[!UICONTROL field name]**>* > *&lt;**[!UICONTROL instance]**>*.

   -of-

* Klik met de rechtermuisknop in een bestaande kolom in de veldviewer en klik **[!UICONTROL Fields]** > *&lt;**[!UICONTROL field name]**>* > *&lt;**[!UICONTROL instance]***.

De veldnaam verwijst naar de naam van het veld en de instantie verwijst naar de plaats in de configuratie van de gegevensset waar het veld wordt gebruikt, zoals een gegevenssetverwerkingsfase of een transformatie. Sommige velden worden op meerdere plaatsen in de configuratie van de gegevensset gebruikt (een veld kan bijvoorbeeld door meerdere transformaties worden gewijzigd). U moet dus selecteren welke instantie van het veld u aan de veldviewer wilt toevoegen.

In de lijst met beschikbare velden wordt een X links weergegeven van velden die al in de viewer worden weergegeven.

**Een veld verwijderen uit een veldviewer**

* Klik met de rechtermuisknop in de kolom voor het veld dat u wilt verwijderen en klik op **[!UICONTROL Remove Field]**.
