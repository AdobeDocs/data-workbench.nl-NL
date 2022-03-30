---
description: De parameter ExpCookieURL kan worden gebruikt om te testen dat uw gecontroleerd experiment behoorlijk werkt.
solution: Analytics
title: Het parameter ExpCookieURL wijzigen (optioneel)
uuid: 0c160c26-f9de-4e41-a05d-bf7bb32395bb
exl-id: fe3dadab-890d-4426-b6f5-8ffd1cd38c69
source-git-commit: 31f775478b0f0d968310ed10a43ad46791319ee9
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Het parameter ExpCookieURL wijzigen (optioneel){#modifying-the-expcookieurl-paramter-optional}

De parameter ExpCookieURL kan worden gebruikt om te testen dat uw gecontroleerd experiment behoorlijk werkt.

Deze parameter definieert de URL van een virtuele pagina die u op verzoek plaatst in een opgegeven experiment en groep en u vervolgens doorstuurt naar de hoofdmap van uw website. Vanaf dat punt tot het einde van het experiment maakt u deel uit van het opgegeven experiment en de opgegeven groep.

De standaardpagina voor deze parameter is [!DNL setcookie.htm], maar u kunt elke geldige virtuele URL gebruiken.

>[!NOTE]
>
>Dit moet een virtuele URL zijn en mag geen echte pagina of deel van bestaande inhoud zijn. Er mag geen bestand met de opgegeven naam voorkomen op de webserver op het opgegeven pad.

Hieronder ziet u een voorbeeld van de parameter ExpCookieURL:

[!DNL ExpCookieURL /setcookie.htm]
