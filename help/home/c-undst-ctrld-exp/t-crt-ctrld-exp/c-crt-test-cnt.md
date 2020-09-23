---
description: Voordat u het experiment configureert, moet u de alternatieve inhoud maken die u in het experiment wilt gebruiken.
solution: Analytics,Analytics
title: De testinhoud maken
topic: Data workbench
uuid: d7996522-38a6-4bb8-9736-d71157c17b45
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# De testinhoud maken{#creating-the-test-content}

Voordat u het experiment configureert, moet u de alternatieve inhoud maken die u in het experiment wilt gebruiken.

De controlegroep wordt verzonden naar originele URI, terwijl de testgroep wordt verzonden naar nieuwe, afwisselende URI.

U voorkomt verwarring door de bestandsnamen van testgroepen niet opnieuw te gebruiken. Als u bijvoorbeeld een experiment uitvoert met een bestand voor een testgroep met de naam [!DNL test2.asp], gebruikt u niet [!DNL test2.asp] als naam voor het testbestand in het volgende experiment.

Voor de veronderstelling dat het bewegen van de grafische verbinding &quot;Verzoek om een Demo&quot;op uw homepage de Omzetting van de Bezoeker beïnvloedt, creëren wij de afwisselende homepage die de &quot;Verzoek om een Demo&quot;grafische verbinding in de nieuwe positie bevat. De volgende sectie beschrijft hoe u dan specificeert dat de controlegroep URI met de testgroep URI [!DNL index.asp] voor een bepaald percentage bezoekers [!DNL index2.asp] wordt vervangen.
