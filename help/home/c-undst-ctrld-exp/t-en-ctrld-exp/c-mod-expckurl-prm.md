---
description: De parameter ExpCookieURL kan worden gebruikt om te testen dat uw gecontroleerd experiment behoorlijk werkt.
solution: Insight,Analytics
title: Het wijzigen van de Paramter ExpCookieURL (Facultatief)
topic: Data workbench
uuid: 0c160c26-f9de-4e41-a05d-bf7bb32395bb
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het wijzigen van de Paramter ExpCookieURL (Facultatief){#modifying-the-expcookieurl-paramter-optional}

De parameter ExpCookieURL kan worden gebruikt om te testen dat uw gecontroleerd experiment behoorlijk werkt.

Deze parameter bepaalt URL van een virtuele pagina die wanneer gevraagd u in een gespecificeerd experiment en een groep plaatst en dan u aan de wortel van uw website opnieuw richt. Vanaf dat punt tot het einde van het experiment, maak je deel uit van het gespecificeerde experiment en de groep.

De standaardpagina voor deze parameter is [!DNL setcookie.htm], maar u kunt om het even welke geldige virtuele URL gebruiken.

>[!NOTE]
>
>Dit moet een virtuele URL zijn en mag geen echte pagina of stuk bestaande inhoud zijn. Er zou geen dossier op de Webserver bij de gespecificeerde weg met de gespecificeerde naam moeten zijn.

Na is een voorbeeld van de parameter ExpCookieURL:

[!DNL ExpCookieURL /setcookie.htm]
