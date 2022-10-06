---
description: Stappen om ervoor te zorgen dat het opnieuw verwerken of het opnieuw omzetten regelmatig gaat en in tijd voor de gebruikers van de gegevenswerkbank eindigt om terug aan het werk te worden
title: Voorbereiden op opwerking of hertransformatie
uuid: 69a5878e-707a-4100-89ba-bae0b8a16c84
exl-id: f3746edf-416e-45c2-896c-48a3c875318c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Voorbereiden op opwerking of hertransformatie{#preparing-for-reprocessing-or-retransformation}

{{eol}}

Stappen om ervoor te zorgen dat het opnieuw verwerken of het opnieuw omzetten regelmatig gaat en in tijd voor de gebruikers van de gegevenswerkbank eindigt om terug aan het werk te worden

1. Bepaal de verstreken tijd van vorige verwerking of transformatie door de profielen van de dataset te controleren [!DNL Processing Mode History] in de [!DNL Detailed Status] interface.

   1. Tijdens het werken in uw datasetprofiel, open [!DNL Detailed Status] interface.
   1. Klikken **[!UICONTROL Processing Status]** > *&lt;**[!UICONTROL dataset profile name]**>* > **[!UICONTROL Processing Mode History]** om de verstreken tijden van vorige verwerking of transformatie te bekijken.

      * De snelle Input is de totale tijd nodig voor logboekverwerking.
      * De snelle Fusie is de totale tijd nodig voor transformatie.
      * De som twee keer (Snelle Input + Snelle Fusie) is de totale tijd nodig voor de verwerking van de dataset.

      In het onderstaande voorbeeld wordt aangegeven dat de logverwerking ongeveer 43 seconden in beslag heeft genomen, terwijl de transformatie minder dan 2 minuten in beslag heeft genomen.

      ![](assets/vis_DetailedStatus_ProcessingModeHistory.png)

      Voor meer informatie over de [!DNL Detailed Status] interface, zie *Gebruikershandleiding voor Data Workbench*.


1. Plan en plant de opwerking. Omdat de gebruikers van de gegevenswerkbank geen toegang tot de gegevens tijdens de fase van de logboekverwerking hebben, zorg ervoor dat u herverwerking om tijdens een aangewezen tijd, zoals over het weekend plant voor te komen.
1. Controleer de voortgang van de opwerking en de hertransformatie met behulp van de velden in het dialoogvenster [!DNL Processing Legend.] Voor meer informatie over de [!DNL Processing Legend], zie de *Gebruikershandleiding voor Data Workbench*.
