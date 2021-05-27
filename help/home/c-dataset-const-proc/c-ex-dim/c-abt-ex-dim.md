---
description: De Server van het Inzicht (InsightServer64.exe) laat u toe om douanedimensies van gebeurtenisgegevens of raadplegingsgegevens te bepalen.
title: Uitgebreide Dimension
uuid: ae014a26-5286-4e36-9098-aaa463d9fe05
exl-id: f74aa85e-f880-4ab5-a8fb-128862aa808f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Informatie over uitgebreide Dimension{#about-extended-dimensions}

De Server van het Inzicht (InsightServer64.exe) laat u toe om douanedimensies van gebeurtenisgegevens of raadplegingsgegevens te bepalen.

Aangepaste afmetingen die u definieert, worden uitgebreide afmetingen genoemd. U kunt hen gebruiken om visualisaties tot stand te brengen, uitgebreide metriek te bouwen, of analyse uit te voeren om de verrichtingen en de kwesties te begrijpen verbonden aan uw bedrijfskanaal. U kunt verschillende soorten uitgebreide afmetingen definiëren in het [!DNL Transformation.cfg]-bestand of in [!DNL Transformation Dataset Include]-bestanden.

Een uitgebreide dimensie vertegenwoordigt een relatie tussen de waarden van het logboekgebied en een ouderafmeting. Een ouderafmeting kan om het even welke user-defined telbare afmeting zijn. Zie [Telbare Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-count-dim.md#concept-f28b633419494e7bbc510012dbfcc6f8). U geeft het bovenliggende element op bij het definiëren van de dimensie in het [!DNL Transformation.cfg]-bestand of een [!DNL Transformation Dataset Include]-bestand. Het bovenliggende element van een dimensie is hetzelfde als het niveau ervan. Bijvoorbeeld, als u een afmeting met een ouder van Zitting bepaalt, dan is die afmeting een zitting-vlakke afmeting.

>[!NOTE]
>
>De waarden van de logvelden kunnen afkomstig zijn van de inherente waarden die beschikbaar zijn in de logbestanden ( [!DNL .vsl]) of andere bronnen van gebeurtenisgegevens, of van uitgebreide logvelden die zijn gemaakt met behulp van transformaties.

Als u een uitgebreide dimensie aan een visualisatie wilt toevoegen, opent u deze vanuit de lijst Uitgebreide in het menu [!DNL Select Dimension]. Als u bijvoorbeeld een uitgebreide dimensie wilt toevoegen aan een grafiekvisualisatie, klikt u met de rechtermuisknop in de werkruimte en klikt u op **[!UICONTROL Add Visualization]** > **[!UICONTROL Graph]** > **[!UICONTROL Extended]** > *&lt;**[!UICONTROL dimension name]**>*. Als u de lijst met uitgebreide afmetingen wilt ordenen in de interface van de gegevenswerkbank, kunt u de uitgebreide afmetingen verplaatsen naar submappen die u maakt. Zie het Administratieve hoofdstuk van Interfaces van *de Gids van de Gebruiker van de Data Workbench*. Als u dit doet, verschijnen de namen van de submappen ook in het menu, zoals in Add Visualization > Graph > Extended > &lt;*subfolder name*> > &lt;*dimensienaam*>.

Als u alle dimensies wilt zien die zijn gedefinieerd voor uw gegevenssetprofiel en de buffergrootte voor elke component, opent u de [!DNL Detailed Status]-interface in de gegevenswerkbank en klikt u op **[!UICONTROL Performance]** en **[!UICONTROL Dimensions]** om de knooppunten uit te vouwen. De buffergrootte, die vraagtijden controleert, wordt uitgedrukt in MB. Voor meer informatie over de [!DNL Detailed Status] interface, zie de gids van het Beleid van de Server en van de Installatie.
