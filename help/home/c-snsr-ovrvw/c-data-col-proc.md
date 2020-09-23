---
description: Sensor automatiseert de aanschaf van gegevens van uw Internet-kanaal door het grootste deel van de menselijke arbeid weg te doen die traditioneel bij gegevensinzameling betrokken is.
solution: Analytics
title: Hoe werkt het gegevensverzamelingsproces?
uuid: d34e5938-217b-4a1e-b96e-55a02b1c3af0
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# Hoe werkt het gegevensverzamelingsproces?{#how-does-the-data-collection-process-work}

Sensor automatiseert de aanschaf van gegevens van uw Internet-kanaal door het grootste deel van de menselijke arbeid weg te doen die traditioneel bij gegevensinzameling betrokken is.

In veel gevallen [!DNL Sensor] kan het gebruik van gegevensbeheer het gegevensbeheerproces aanzienlijk vereenvoudigen.

De grote Internet van vandaag, Extranet, en Intranetplaatsen lopen vaak op een serie van Webservers. De geproduceerde logboeken en gegevens kunnen zeer groot en lastig zijn te beheren. Bijvoorbeeld, als uw plaats 30 Webservers in werking stelt, typisch zou één van uw werknemers (of de werknemers van de uitbestede dienstverlener) elk logboekdossier op elk van de 30 servers trekken en consolideren, dan looppas rapporten over hen. Wanneer u [!DNL Sensor] op elk van uw webservers installeert, wordt dit hele proces geautomatiseerd, waardoor uw kosten worden verminderd en gegevens in real-time beschikbaar worden gesteld.

Om dit proces te automatiseren, [!DNL Sensor] verzamelt ruwe informatie over het verkeer op een website direct van elke Webserver. De onbewerkte gegevens die [!DNL Sensor] worden vastgelegd, worden gebeurtenisgegevens genoemd en zijn vergelijkbaar met het type gegevens dat de webserver in de logbestanden opneemt.

Om deze gegevens te vangen, instrumentatie binnen [!DNL Sensor] verslaginformatie over elke HTTP- verzoek dat uw Webserver verwerkt. [!DNL Sensor] buffert dan de informatie tegen netwerkmislukking te beschermen en verzendt veilig de informatie via HTTP/S aan [!DNL data workbench server] die u specificeert.

Nadat de gegevens zijn [!DNL data workbench server] ontvangen, worden uw logbestanden verwerkt en opgeslagen in bestanden met sterk gecomprimeerde [!DNL .vsl] indelingen, zodat u eenvoudig zeer grote hoeveelheden gegevens op goedkope hardware kunt onderhouden.

Voor informatie over de gebieden van gebeurtenisgegevens die door [!DNL Sensor] in [!DNL .vsl] dossiers worden verzameld, zie de Gebieden [van het Verslag van](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44)Gebeurtenisgegevens.
