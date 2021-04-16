---
description: Informatie over de algemene configuratie van de Sensor met één instantie van de Webserver die op een Webserver loopt.
title: Werken met meerdere instanties van een webserver
uuid: 778ea95f-e0f2-4c2a-b7ed-7e323fea1e48
exl-id: a371f9ed-6c27-4b3d-843f-ae5621013410
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Werken met meerdere instanties van een webserver{#working-with-multiple-instances-of-a-web-server}

Informatie over de algemene configuratie van de Sensor met één instantie van de Webserver die op een Webserver loopt.

![](assets/web_inst.png)

In dit scenario schrijft één webserverinstantie gegevens naar het in geheugen toegewezen rijbestand, dat door de zender wordt gelezen en naar [!DNL data workbench server] wordt verzonden.

Wanneer [!DNL Sensor] op een Webserver wordt geïnstalleerd die veelvoudige inzamelaarinstanties in werking stelt, kunt u het op één van twee manieren vormen:

* U kunt alle inzamelaarmodules hebben één rijdossier delen.

   Wanneer het gebruiken van één enkel rijdossier, wordt het beheer, de configuratie, en het beleid enigszins vereenvoudigd omdat de architectuur zelf minder complex is. Nochtans, met één enkel rijdossier, wordt de volledige Webserver, ongeacht het aantal instanties, geïdentificeerd als WEB1.

* U kunt de bovenstaande architectuur meerdere keren repliceren en elke instantie van de webserver een afzonderlijk rijdossier hebben.

   Hierdoor kunt u elk exemplaar van de webserver afzonderlijk identificeren. Met andere woorden, de identificatie van de webserver (en de bijbehorende SensorID in de configuratie [!DNL Sensor]) is een functie van deze configuratie.

In elk geval, hebben de gegevens nog alle informatie van de gastheernaam zodat u tussen [!DNL www.client.com], [!DNL www2.client.com] kunt onderscheiden, etc. De correcte configuratie wordt bepaald door de analysedoelstellingen en of de analisten de gegevens moeten segmenteren die op een specifieke instantie worden gebaseerd die op een Webserver loopt.

>[!NOTE]
>
>Dit soort segmentatie wordt doorgaans alleen gebruikt voor operationele analyse en wordt buiten dat gebied niet veel praktisch gebruikt.
