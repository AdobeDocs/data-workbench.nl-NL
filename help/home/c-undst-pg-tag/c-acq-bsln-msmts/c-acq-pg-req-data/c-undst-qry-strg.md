---
description: De querytekenreeks (cs-uri-query) wordt vaak gebruikt door webtoepassingen en siteontwikkelaars om informatie van pagina naar pagina door te geven vanwege de stateless aard van HTTP.
title: De queryreeks begrijpen
uuid: 7403277d-fbce-4e98-bd42-894142e38d0d
exl-id: b5281e5f-3eb7-4d6a-a7b3-9958cb430621
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# De queryreeks begrijpen{#understanding-the-query-string}

{{eol}}

De querytekenreeks (cs-uri-query) wordt vaak gebruikt door webtoepassingen en siteontwikkelaars om informatie van pagina naar pagina door te geven vanwege de stateless aard van HTTP.

In veel gevallen kan informatie in het vraagkoord worden overgegaan wanneer het door wordt verworven [!DNL Sensor] op de webserver. Dergelijke informatie kan worden gebruikt door [!DNL Site] om de ware structuur van de site en het pad van de bezoekers erdoorheen te belichten, alsmede andere informatie.

In sommige dynamische websites zijn naam=waarde paren (variabelen) in de queryreeks belangrijk om te bepalen welke pagina daadwerkelijk wordt aangevraagd door een bezoeker. In dergelijke gevallen kunnen URL&#39;s op de volgende of soortgelijke wijze worden gestructureerd:

```
https://www.myserver.com/pageserved.asp?PAGENAME=HOME
```

In dit voorbeeld is PAGENAME in feite de indicator van welke pagina aan de aanvrager van deze URL zal worden betekend. Veel hulpprogramma&#39;s en services voor webloganalyse beperken de mogelijkheid van een siteoperator om te definiëren wat een pagina in hun site is, op basis van de variabelen voor queryreeksen die voorkomen in de queryreeksen van de URL&#39;s van de site. De server van de gegevenswerkbank en gegevenswerkbank kunnen worden gevormd om dergelijke vraagnamen te gebruiken om unieke pagina&#39;s te bepalen. Dit is belangrijk omdat veel systemen de volgende URL&#39;s als dezelfde pagina zouden interpreteren, maar [!DNL Site] niet.

```
https://www.myserver.com/pageserved.asp?PAGENAME=HOME
https://www.myserver.com/pageserved.asp?PAGENAME=HOME2
```

Siteontwikkelaars en -toepassingen voegen vaak veel queryreeksvariabelen toe aan de URL&#39;s van een site die niets te maken hebben met het identificeren van de pagina die wordt opgevraagd. Hieronder vindt u voorbeelden:

```
https://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10001
https://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10002
https://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10003
```

In dit voorbeeld is de variabele CAMPAIGN= van de querytekenreeks toegevoegd aan de URL. Deze CAMPAIGN-variabele wordt gebruikt om aan te geven welke marketingcampagne ertoe heeft geleid dat een bezoeker deze URL heeft geselecteerd. [!DNL Site] kan worden gevormd om deze informatie te gebruiken CAMPAIGN, maar het van de definitie van te scheiden welke pagina een bezoeker bekeken zodat in uw lijst van pagina&#39;s voor rapportering en analysedoeleinden u eenvoudig het volgende zou zien:

```
https://www.myserver.com/pageserved.asp?PAGENAME=HOME
```
