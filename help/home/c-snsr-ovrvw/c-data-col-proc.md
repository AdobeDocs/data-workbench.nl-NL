---
description: Sensor automatiseert de aanschaf van gegevens van uw Internet-kanaal door het grootste deel van de menselijke arbeid weg te doen die traditioneel bij gegevensinzameling betrokken is.
title: Hoe werkt het gegevensverzamelingsproces?
uuid: d34e5938-217b-4a1e-b96e-55a02b1c3af0
exl-id: dd930739-ca24-4166-8ebd-84b65f6f3754
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Hoe werkt het proces van de Gegevensverzameling?{#how-does-the-data-collection-process-work}

Sensor automatiseert de aanschaf van gegevens van uw Internet-kanaal door het grootste deel van de menselijke arbeid weg te doen die traditioneel bij gegevensinzameling betrokken is.

In veel gevallen kan het gebruik van [!DNL Sensor] uw gegevensbeheerproces aanzienlijk vereenvoudigen.

De grote Internet van vandaag, Extranet, en Intranetplaatsen lopen vaak op een serie van Webservers. De geproduceerde logboeken en gegevens kunnen zeer groot en lastig zijn te beheren. Bijvoorbeeld, als uw plaats 30 Webservers in werking stelt, typisch zou één van uw werknemers (of de werknemers van de uitbestede dienstverlener) elk logboekdossier op elk van de 30 servers trekken en consolideren, dan looppas rapporten over hen. Als u [!DNL Sensor] op elk van uw webservers installeert, wordt dit hele proces geautomatiseerd, waardoor uw kosten worden verminderd en gegevens in real-time beschikbaar worden gesteld.

Om dit proces te automatiseren, verzamelt [!DNL Sensor] ruwe informatie over het verkeer op een website direct van elke Webserver. De onbewerkte gegevens die [!DNL Sensor] vastlegt, worden gebeurtenisgegevens genoemd en zijn vergelijkbaar met het type gegevens dat uw webserver opneemt in de logbestanden.

Om deze gegevens te vangen, registreert de instrumentatie binnen [!DNL Sensor] informatie over elk HTTP- verzoek dat uw Webserver verwerkt. [!DNL Sensor] buffert dan de informatie tegen netwerkmislukking te beschermen en verzendt veilig de informatie via HTTP/S aan  [!DNL data workbench server] die u specificeert.

Nadat [!DNL data workbench server] de gegevens ontvangt, verwerkt en slaat het uw logboekdossiers in hoogst-samengeperste [!DNL .vsl] formaatdossiers op, die u toestaan om zeer grote hoeveelheden gegevens op goedkope hardware gemakkelijk te handhaven.

Zie [Gebeurtenisgegevensvelden](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44) voor informatie over de gebeurtenisgegevensvelden die door [!DNL Sensor] in [!DNL .vsl]-bestanden worden verzameld.
