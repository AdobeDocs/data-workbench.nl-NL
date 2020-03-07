---
description: Het vraagkoord (cs-uri-vraag) wordt vaak gebruikt door Webtoepassingen en plaatsontwikkelaars om informatie van pagina tot pagina wegens de statenloze aard van HTTP over te gaan.
solution: Analytics
title: Het begrip van het Koord van de Vraag
topic: Data workbench
uuid: 7403277d-fbce-4e98-bd42-894142e38d0d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het begrip van het Koord van de Vraag{#understanding-the-query-string}

Het vraagkoord (cs-uri-vraag) wordt vaak gebruikt door Webtoepassingen en plaatsontwikkelaars om informatie van pagina tot pagina wegens de statenloze aard van HTTP over te gaan.

In veel gevallen, kan de informatie in het vraagkoord worden overgegaan wanneer het door [!DNL Sensor] bij de Webserver wordt verworven. Dergelijke informatie kan worden gebruikt door de ware structuur van de site en het pad van de bezoekers erdoorheen te belichten, evenals andere informatie. [!DNL Site]

In sommige dynamische websites, zijn de naam=value paren (variabelen) in het vraagkoord belangrijk voor het bepalen van de daadwerkelijke pagina die door een bezoeker wordt gevraagd. In dergelijke gevallen kunnen URL&#39;s op de volgende of soortgelijke wijze worden gestructureerd:

```
http://www.myserver.com/pageserved.asp?PAGENAME=HOME
```

In dit voorbeeld, is PAGENAME eigenlijk de indicator van welke pagina aan de aanvrager van dit URL zal worden gediend. Vele hulpmiddelen en de diensten van de de analyse van het Weblogboek beperken de capaciteit van een plaatsexploitant om te bepalen wat een pagina in hun plaats gebaseerd is op welke variabelen van het vraagkoord in de vraagkoorden van URLs van de plaats voorkomen. De server van de gegevenswerkbank en de gegevenswerkbank kunnen worden gevormd om dergelijke vraagnamen te gebruiken om unieke pagina&#39;s te bepalen. Dit is belangrijk omdat vele systemen volgende URLs als de zelfde pagina zouden interpreteren, maar [!DNL Site] niet.

```
http://www.myserver.com/pageserved.asp?PAGENAME=HOME
http://www.myserver.com/pageserved.asp?PAGENAME=HOME2
```

Op dezelfde manier voegen de plaatsontwikkelaars en de toepassingen vaak vele variabelen van het vraagkoord in URLs van een plaats toe die niets met het identificeren van de daadwerkelijke pagina te doen hebben die wordt gevraagd. De voorbeelden worden hieronder getoond:

```
http://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10001
http://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10002
http://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10003
```

In dit voorbeeld, is de variabele CAMPAIGN= van het vraagkoord toegevoegd aan URL. Deze variabele CAMPAIGN wordt gebruikt om erop te wijzen welke marketing campagne een bezoeker veroorzaakte om dit URL te selecteren. [!DNL Site] kan worden gevormd om deze CAMPAIGN informatie te gebruiken, nog los het van de definitie van welke pagina een bezoeker bekeken zodat in uw lijst van pagina&#39;s voor rapportering en analysedoeleinden u eenvoudig het volgende zou zien:

```
http://www.myserver.com/pageserved.asp?PAGENAME=HOME
```

