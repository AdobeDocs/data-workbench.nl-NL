---
description: Informatie over de algemene configuratie van de Sensor met één instantie van de Webserver die op een Webserver loopt.
title: Werken met meerdere instanties van een webserver
uuid: 778ea95f-e0f2-4c2a-b7ed-7e323fea1e48
exl-id: a371f9ed-6c27-4b3d-843f-ae5621013410
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Werken met meerdere instanties van een webserver{#working-with-multiple-instances-of-a-web-server}

{{eol}}

Informatie over de algemene configuratie van de Sensor met één instantie van de Webserver die op een Webserver loopt.

![](assets/web_inst.png)

In dit scenario schrijft één enkele instantie van de Webserver gegevens aan het geheugen in kaart gebrachte rijdossier, dat door de zender wordt gelezen en naar het verzonden [!DNL data workbench server].

Wanneer [!DNL Sensor] is geïnstalleerd op een webserver waarop meerdere verzamelaarinstanties worden uitgevoerd, kunt u deze op twee manieren configureren:

* U kunt alle inzamelaarmodules hebben één rijdossier delen.

   Wanneer het gebruiken van één enkel rijdossier, wordt het beheer, de configuratie, en het beleid enigszins vereenvoudigd omdat de architectuur zelf minder complex is. Nochtans, met één enkel rijdossier, wordt de volledige Webserver, ongeacht het aantal instanties, geïdentificeerd als WEB1.

* U kunt de bovenstaande architectuur meerdere keren repliceren en elke instantie van de webserver een afzonderlijk rijdossier hebben.

   Hierdoor kunt u elk exemplaar van de webserver afzonderlijk identificeren. Met andere woorden, de identificatie van de webserver (en de bijbehorende SensorID in de [!DNL Sensor] configuratie) is een functie van deze configuratie.

In elk geval, hebben de gegevens nog alle informatie van de gastheernaam zodat u tussen kunt onderscheiden [!DNL www.client.com], [!DNL www2.client.com], enzovoort. De correcte configuratie wordt bepaald door de analysedoelstellingen en of de analisten de gegevens moeten segmenteren die op een specifieke instantie worden gebaseerd die op een Webserver loopt.

>[!NOTE]
>
>Dit soort segmentatie wordt doorgaans alleen gebruikt voor operationele analyse en wordt buiten dat gebied niet veel praktisch gebruikt.
