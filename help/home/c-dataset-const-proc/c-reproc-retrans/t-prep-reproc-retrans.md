---
description: Stappen om ervoor te zorgen dat de opwerking of de retransformatie regelmatig gaan en op tijd voor de gebruikers van de gegevenswerkbank eindigt om terug aan het werk te krijgen
solution: Analytics
title: Voorbereiding voor opwerking of herbewerking
topic: Data workbench
uuid: 69a5878e-707a-4100-89ba-bae0b8a16c84
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Voorbereiding voor opwerking of herbewerking{#preparing-for-reprocessing-or-retransformation}

Stappen om ervoor te zorgen dat de opwerking of de retransformatie regelmatig gaan en op tijd voor de gebruikers van de gegevenswerkbank eindigt om terug aan het werk te krijgen

1. Bepaal de verstreken tijd van vorige verwerking of transformatie door de datasetprofiel [!DNL Processing Mode History] in de [!DNL Detailed Status] interface te controleren.

   1. Terwijl het werken in uw datasetprofiel, open de [!DNL Detailed Status] interface.
   1. Klik **[!UICONTROL Processing Status]** > *&lt;**[!UICONTROL dataset profile name]**>* > **[!UICONTROL Processing Mode History]** om de verstreken tijd van vorige verwerking of transformatie te bekijken.

      * De snelle Input is de totale tijd nodig voor logboekverwerking.
      * De snelle Fusie is de totale tijd nodig voor transformatie.
      * De som twee keer (Snelle Input + Snelle Fusie) is de totale tijd nodig voor de verwerking van de dataset.
      Het voorbeeld hieronder wijst erop dat de logboekverwerking ongeveer 43 seconden kostte, terwijl de transformatie minder dan 2 minuten kostte.

      ![](assets/vis_DetailedStatus_ProcessingModeHistory.png)

      Voor meer informatie over de [!DNL Detailed Status] interface, zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.


1. De opwerking plannen en plannen. Omdat de gebruikers van de gegevenswerkbank geen toegang tot de gegevens tijdens de fase van de logboekverwerking hebben, zorg ervoor dat u opwerking plant om tijdens een aangewezen tijd, zoals over het weekend voor te komen.
1. Controleer de voortgang van de opwerking en de hertransformatie met behulp van de velden in [!DNL Processing Legend.] Voor meer informatie over de [!DNL Processing Legend], raadpleegt u de gebruikershandleiding voor de *gegevenswerkbank*.
