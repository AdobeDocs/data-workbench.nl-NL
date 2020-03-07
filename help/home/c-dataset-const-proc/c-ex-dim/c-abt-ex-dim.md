---
description: De server van het Inzicht (InsightServer64.exe) laat u toe om douanedimensies van gebeurtenisgegevens of raadplegingsgegevens te bepalen.
solution: Analytics
title: Over uitgebreide afmetingen
topic: Data workbench
uuid: ae014a26-5286-4e36-9098-aaa463d9fe05
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Over uitgebreide afmetingen{#about-extended-dimensions}

De server van het Inzicht (InsightServer64.exe) laat u toe om douanedimensies van gebeurtenisgegevens of raadplegingsgegevens te bepalen.

Om het even welke douaneafmetingen die u bepaalt worden bedoeld als uitgebreide afmetingen. U kunt hen gebruiken om visualisaties tot stand te brengen, uitgebreide metriek te bouwen, of analyse uit te voeren om de verrichtingen en de kwesties te begrijpen verbonden aan uw bedrijfskanaal. U kunt verscheidene types van uitgebreide afmetingen in het [!DNL Transformation.cfg] dossier of in [!DNL Transformation Dataset Include] dossiers bepalen.

Een uitgebreide dimensie vertegenwoordigt een verband tussen de waarden van het logboekgebied en een ouderdimensie. Een ouderafmeting kan om het even welke user-defined telbare afmeting zijn. Zie [Afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-count-dim.md#concept-f28b633419494e7bbc510012dbfcc6f8). U specificeert de ouder wanneer het bepalen van de afmeting in het [!DNL Transformation.cfg] dossier of een [!DNL Transformation Dataset Include] dossier. De ouder van een dimensie is het zelfde als zijn niveau. Bijvoorbeeld, als u een afmeting met een ouder van Zitting bepaalt, dan is die afmeting een zitting-vlakke afmeting.

>[!NOTE]
>
>De waarden van het logboekgebied kunnen uit de inherente waarden komen beschikbaar in de logboek ( [!DNL .vsl]) dossiers of andere bronnen van gebeurtenisgegevens of uit uitgebreide logboekgebieden die door het gebruik van transformaties worden gecreeerd.

Om een uitgebreide afmeting aan een visualisatie toe te voegen, hebt toegang u tot het van de Uitgebreide lijst binnen het [!DNL Select Dimension] menu. Bijvoorbeeld, om een uitgebreide afmeting aan een grafiekvisualisatie toe te voegen, zou u binnen de werkruimte met de rechtermuisknop klikken en **[!UICONTROL Add Visualization]** > **[!UICONTROL Graph]** > **[!UICONTROL Extended]** > *&lt;**[!UICONTROL dimension name]**>* klikken. Als u de lijst van uw uitgebreide afmetingen binnen de interface van de gegevenswerkbank zou willen organiseren, kunt u de uitgebreide afmetingen in subfolders bewegen die u creeert. Zie het Administratieve hoofdstuk van Interfaces van de Gids *van de Gebruiker van de Werkbank van* Gegevens. Als u dit doet, verschijnen de namen van subfolders ook in het menu, zoals in Add Visualisatie > Grafiek > Uitgebreid > &lt;*subfolder naam*> > &lt;*afmetingsnaam*>.

Om alle afmetingen te zien die voor uw datasetprofiel en de buffergrootte voor elk zijn bepaald, open de [!DNL Detailed Status] interface in gegevenswerkbank en klik **[!UICONTROL Performance]**, dan **[!UICONTROL Dimensions]** om de knopen uit te breiden. De buffergrootte, die vraagtijden controleert, wordt uitgedrukt in MB. Voor meer informatie over de [!DNL Detailed Status] interface, zie de gids van het Beleid en van de Installatie van de Server.
