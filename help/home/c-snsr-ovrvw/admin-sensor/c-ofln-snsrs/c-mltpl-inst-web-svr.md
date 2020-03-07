---
description: Informatie over de algemene configuratie van de Sensor met één instantie die van de Webserver op een Webserver loopt.
solution: Insight
title: Het werken met Veelvoudige Instanties van een Server van het Web
uuid: 778ea95f-e0f2-4c2a-b7ed-7e323fea1e48
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het werken met Veelvoudige Instanties van een Server van het Web{#working-with-multiple-instances-of-a-web-server}

Informatie over de algemene configuratie van de Sensor met één instantie die van de Webserver op een Webserver loopt.

![](assets/web_inst.png)

In dit scenario, schrijft één enkele instantie van de Webserver gegevens aan het geheugen in kaart gebrachte rijdossier, dat door de zender wordt gelezen en naar [!DNL data workbench server]wordt verzonden.

Wanneer [!DNL Sensor] is geïnstalleerd op een Webserver die veelvoudige inzamelaarinstanties in werking stelt, kunt u het één van twee manieren vormen:

* U kunt alle inzamelaarmodules hebben één rijdossier delen.

   Wanneer het gebruiken van één enkel rijdossier, worden het beheer, de configuratie, en het beleid enigszins vereenvoudigd omdat de architectuur zelf minder complex is. Nochtans, met één enkel rijdossier, wordt de volledige Webserver, ongeacht het aantal instanties, geïdentificeerd als WEB1.

* U kunt de bovengenoemde architectuur veelvoudige tijden herhalen en elke instantie van de Webserver hebben een afzonderlijk rijdossier hebben.

   Dit laat u toe om elk van de instanties van de Webserver uniek te identificeren. Met andere woorden, is de identificatie van de Webserver (en overeenkomstige SensorID in de [!DNL Sensor] configuratie) een functie van deze configuratie.

In elk geval, heeft het gegeven nog alle informatie van de gastheernaam zodat u tussen kunt onderscheiden [!DNL www.client.com], [!DNL www2.client.com]enzovoort. De correcte configuratie wordt bepaald door de analysedoelstellingen en of de analisten de gegevens moeten segmenteren die op een specifieke instantie worden gebaseerd die op een Webserver loopt.

>[!NOTE]
>
>Dit type van segmentatie wordt typisch gebruikt slechts in operationele analyse en verstrekt niet veel praktisch gebruik buiten dat gebied.

