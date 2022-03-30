---
description: Voordat u het experiment configureert, moet u de alternatieve inhoud maken die u in het experiment wilt gebruiken.
solution: Analytics
title: De testinhoud maken
uuid: d7996522-38a6-4bb8-9736-d71157c17b45
exl-id: fd46c6af-37e8-452a-880d-147b7d0cfe21
source-git-commit: 31f775478b0f0d968310ed10a43ad46791319ee9
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# De testinhoud maken{#creating-the-test-content}

Voordat u het experiment configureert, moet u de alternatieve inhoud maken die u in het experiment wilt gebruiken.

De controlegroep wordt verzonden naar originele URI, terwijl de testgroep wordt verzonden naar nieuwe, afwisselende URI.

U voorkomt verwarring door de bestandsnamen van testgroepen niet opnieuw te gebruiken. Bijvoorbeeld, als u een experiment in werking stelt gebruikend een dossier van de testgroep genoemd [!DNL test2.asp], niet gebruiken [!DNL test2.asp] als de naam voor het testbestand in het volgende experiment.

Voor de veronderstelling dat het bewegen van de grafische verbinding &quot;Verzoek om een Demo&quot;op uw homepage de Omzetting van de Bezoeker beïnvloedt, creëren wij de afwisselende homepage die de &quot;Verzoek om een Demo&quot;grafische verbinding in de nieuwe positie bevat. De volgende sectie beschrijft hoe u dan specificeert dat de controlegroep URI [!DNL index.asp] worden vervangen door de testgroep URI [!DNL index2.asp] voor een bepaald percentage bezoekers.
