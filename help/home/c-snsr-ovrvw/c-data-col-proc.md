---
description: Sensor automatiseert de aanschaf van gegevens van uw Internet-kanaal door het grootste deel van de menselijke arbeid weg te doen die traditioneel bij gegevensinzameling betrokken is.
title: Hoe werkt het gegevensverzamelingsproces?
uuid: d34e5938-217b-4a1e-b96e-55a02b1c3af0
exl-id: dd930739-ca24-4166-8ebd-84b65f6f3754
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Hoe werkt het gegevensverzamelingsproces?{#how-does-the-data-collection-process-work}

{{eol}}

Sensor automatiseert de aanschaf van gegevens van uw Internet-kanaal door het grootste deel van de menselijke arbeid weg te doen die traditioneel bij gegevensinzameling betrokken is.

In veel gevallen kunt u [!DNL Sensor] kan uw gegevensbeheerproces aanzienlijk vereenvoudigen.

De grote Internet van vandaag, Extranet, en Intranetplaatsen lopen vaak op een serie van Webservers. De geproduceerde logboeken en gegevens kunnen zeer groot en lastig zijn te beheren. Bijvoorbeeld, als uw plaats 30 Webservers in werking stelt, typisch zou één van uw werknemers (of de werknemers van de uitbestede dienstverlener) elk logboekdossier op elk van de 30 servers trekken en consolideren, dan looppas rapporten over hen. Installeren [!DNL Sensor] op elk van uw webservers automatiseert u dit hele proces, waardoor uw kosten worden verminderd en gegevens in real-time beschikbaar worden gesteld.

Om dit proces te automatiseren, [!DNL Sensor] verzamelt ruwe informatie over het verkeer op een website direct bij elke Webserver. De onbewerkte gegevens die [!DNL Sensor] vangt wordt genoemd gebeurtenisgegevens en is gelijkaardig aan het type van gegevens dat uw Webserver in zijn logboekdossiers registreert.

Om deze gegevens te vangen, instrumentatie binnen [!DNL Sensor] registreert informatie over elke HTTP- verzoek dat uw Webserver verwerkt. [!DNL Sensor] buffert dan de informatie tegen netwerkmislukking te beschermen en verzendt veilig de informatie via HTTP/S aan [!DNL data workbench server] die u opgeeft.

Na de [!DNL data workbench server] ontvangt de gegevens, verwerkt het en slaat uw logboekdossiers in hoogst samengeperst op [!DNL .vsl] bestandsindelingen maken, zodat u eenvoudig zeer grote hoeveelheden gegevens op goedkope hardware kunt bijhouden.

Voor informatie over de velden met gebeurtenisgegevens die worden verzameld door [!DNL Sensor] in [!DNL .vsl] bestanden, zie [Gebeurtenisgegevensrecordvelden](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44).
