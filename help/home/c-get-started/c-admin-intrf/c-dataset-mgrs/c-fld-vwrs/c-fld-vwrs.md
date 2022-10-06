---
description: Een veldviewer is een tabel met de waarden van een of meer gegevensvelden.
title: Veldviewer
uuid: 1227b0de-6ae8-4f97-ad3e-5c9ead818ba5
exl-id: 53ede4aa-4865-4e67-b3b1-e3e6287f29d7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Veldviewer{#field-viewer}

{{eol}}

Een veldviewer is een tabel met de waarden van een of meer gegevensvelden.

De gebieden de waarvan waarden tonen zijn input of output van de het logboekbronnen van een dataset, transformaties, of uitgebreide afmetingen. De naam van het veld wordt weergegeven in de kolomkop en elke rij bevat de waarde van het veld voor één rij brongegevens. Omdat veldviewers u in staat stellen de waarden van een veld weer te geven, zijn ze handig bij het schrijven en testen [reguliere expressies](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

U kunt een veldviewer openen als een bijschrift van een [!DNL Transformation Dependency] kaart of als standalone visualisatie van [!DNL Admin] menu:

* Een veldviewer maken op basis van een [!DNL Transformation Dependency] kaart. Wanneer u een veldviewer opent vanuit een [!DNL Transformation Dependency] kaart, wordt de kijker bevolkt automatisch gebaseerd op de logboekbron, de transformatie, of de afmeting die u met de rechtermuisknop aanklikt. Voor een logbron of transformatie zijn de velden in de viewer invoer of uitvoer van de logbron of transformatie. Voor een dimensie zijn de velden invoer van de dimensie. Desgewenst kunt u velden toevoegen en verwijderen.

* Een veldviewer maken als zelfstandige visualisatie. Wanneer u een veldviewer opent als een zelfstandige visualisatie, kunt u een [!DNL Log Processing Field Viewer] of [!DNL Transformation Field Viewer]. De viewer is leeg en u moet de gewenste velden toevoegen aan de viewer. Voor een [!DNL Log Processing Field Viewer], kunt u velden toevoegen uit de [!DNL Log Processing.cfg] bestand of [!DNL Log Processing Dataset Include] bestand. Voor een [!DNL Transformation Field Viewer], kunt u velden toevoegen uit de [!DNL Transformation.cfg] bestand of [!DNL Transformation Dataset Include] bestand.

![](assets/vis_FieldViewer_OneField.png)

>[!NOTE]
>
>De kijkers van het gebied zijn geen lijstvisualisaties; daarom hebben zij niet de eigenschappen verbonden aan lijsten.

Ga voor informatie over het toevoegen en verwijderen van velden en filteren in een veldviewer naar [Administratieve interfaces](../../../../../home/c-get-started/c-admin-intrf/c-admin-intrf.md#concept-855c1a91e1a948969fab592adca15f74).
