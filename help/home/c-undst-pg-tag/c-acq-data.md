---
description: Met Sensor kunt u aanvraaggegevens voor het web (gebeurtenis- of loggegevens) en uitgebreide meetgegevens ophalen.
title: Wat voor soort gegevens kan ik ophalen?
uuid: 5ac864b8-4017-4d80-b491-7a5976225eb2
exl-id: 97d87084-cac3-4a94-89e0-f01a66e20324
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Welk soort gegevens kan ik verkrijgen?{#what-kind-of-data-can-i-acquire}

Met Sensor kunt u aanvraaggegevens voor het web (gebeurtenis- of loggegevens) en uitgebreide meetgegevens ophalen.

Uitgebreide meetgegevens zijn niet beschikbaar op uw webservers als onderdeel van de normale werking.

De volgende onderwerpen worden beschreven:

## Webaanvraaggegevens {#section-a28217e8a8c047eb9b1c0ca1f67c832f}

[!DNL Sensor] kunnen gegevens over webverzoeken (gebeurtenis- of loggegevens) automatisch worden opgehaald en naar een centrale locatie worden vervoerd voor opslag en verwerking voor analyse. Tenzij u specifiek verkiest om bepaalde soorten verzoeken uit te filteren en geen gegevens over die verzoektypes te verzamelen, [!DNL Sensor] vangt gegevens over alle GET verzoeken die van de Webservers worden gemaakt waarop het geïnstalleerd is.

[!DNL Sensor] automatiseert dit proces voor het verkrijgen van gegevens voor alle verzoeken van GET die op uw servers worden gedaan en heeft significante zakelijke en technische voordelen in vergelijking met alternatieve methoden om gegevens van websiteverzoeken te verkrijgen. Deze voordelen zijn onder meer:

* Verzoeken die niet nodig zijn voor analyse en rapportage kunnen worden uitgefilterd voordat u kosten maakt voor de aanschaf, het transport, de opslag en de verwerking ervan.
* Sitebeheerders hoeven logbestanden niet handmatig of via een script in batch te roteren.
* [!DNL Sensor] Hiermee voegt u logbestanden samen op een centrale locatie, zodat u ze gemakkelijk kunt verwerken.
* [!DNL Sensor] organiseert en slaat logboekdossiers in een gemeenschappelijke gegevens-bewaart formaat op, die de behoefte om hen te preprocess alvorens zij voor analyse en rapporteringsdoeleinden kunnen worden gebruikt verwijderen.
* Instanties van bepaalde inhoudstypen kunnen in de logbestanden worden opgenomen, ook al worden de meeste aanvragen voor een bepaald inhoudstype automatisch uitgefilterd.
* [!DNL Sensor] Hiermee comprimeert u vermeldingen in logbestanden, waarvoor aanzienlijk minder opslagruimte nodig is, waardoor de kosten worden verminderd en de gegevens langer beschikbaar blijven voor analyse.
* [!DNL Sensor’s] de fout verdraagzame eigenschappen staan systeem en netwerkgebreken toe terwijl nog het verzekeren van de levering van de logboekgegevens aan een centrale bewaarplaats.
* [!DNL Sensor] maakt het mogelijk om gecontroleerde experimenten met webinhoud, processen en marketingcampagnes uit te voeren.
* [!DNL Sensor] tijdstempels registreren vermeldingen in eenheden van 100 ns, die nieuwe types van analytische functionaliteit toestaan.
* [!DNL Sensor] stelt de eigenaars van sites in staat om na de eerste implementatie gegevens (metingen) aan de logbestandvermeldingen toe te voegen, zodat ze deze kunnen analyseren en rapporteren.

Zie [Basislijnmetingen ophalen](../../home/c-undst-pg-tag/c-acq-bsln-msmts/c-acq-bsln-msmts.md#concept-ed9b4b21693a4bafac75d60708b9b6fe) voor meer informatie over het verkrijgen van uitgebreide meetgegevens.

## Uitgebreide meetgegevens {#section-b7f0285de49e432b9db8fda85fa735ba}

[!DNL Sensor] biedt ook ondersteuning voor het gebruik van paginatags (of aanvragen voor ingesloten objecten) voor het ophalen van meetgegevens die niet beschikbaar zijn op uw webservers als onderdeel van hun normale werking. Paginalabels worden doorgaans gebruikt om te meten:

* De weergave van een logische pagina in een dynamische website.
* De weergave van inhoud of advertenties op een door derden beheerde website.
* De weergave van inhoud die wordt aangeboden via een browsercache of CDN.
* Gedetailleerde informatie over de browser van een bezoeker, zoals metingen zoals laadtijd van de pagina, schermresolutie, de formuliervelden die de bezoeker heeft ingevuld, enzovoort.
* Andere gegevens die niet anderszins door browsers naar uw webservers worden verzonden.

[!DNL Sensor] verzamelt alle informatie die in een aanvraag van een GET is geplaatst die naar een webserver wordt verzonden die wordt uitgevoerd  [!DNL Sensor]. Dergelijke verzoeken kunnen afkomstig zijn van alle soorten verzoeken om ingesloten objecten, hetzij om te meten of het verzoek op een bepaald tijdstip door een bepaalde browser is gedaan, hetzij om andere meetgegevens in de gegevensverzamelingsstroom door te geven zodat ze voor analyse- en rapportagedoeleinden kunnen worden verwerkt.

[!DNL Sensor] biedt het beste van aanschafweringswerelden voor zowel client-side als server-side gegevens; het verkrijgt uw webloggegevens aan serverzijde en verzamelt metingen voor client-side, externe sites of cache-busting die door ingesloten objectaanvragen zijn uitgevoerd. Met andere woorden, [!DNL Sensor] verkrijgt zowel de aanvraaggegevens die normaal bekend zijn bij uw webservers (metingen aan de serverzijde) als alle aanvullende meetgegevens die u verzamelt via het gebruik van paginatags (metingen aan de clientzijde) die de gegevens verzenden naar webservers waarop [!DNL Sensor] wordt uitgevoerd. Dergelijke webservers kunnen worden ingezet voor het verzamelen van metingen aan de clientzijde, maar dit hoeft niet zo te zijn.

Zie [Uitgebreide metingen ophalen](../../home/c-undst-pg-tag/c-acq-ext-msmt/c-acq-ext-msmt.md#concept-d171a6d2bde843cdb65bcfe69c6a4944) voor meer informatie over het verkrijgen van uitgebreide meetgegevens.
