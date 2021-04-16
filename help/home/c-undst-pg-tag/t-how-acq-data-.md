---
description: U moet Sensor installeren en uitvoeren op elke webserver die de inhoud voor uw site levert om alle aanvragen te verzamelen die door deze servers worden bekeken.
title: Hoe verkrijg ik deze Data_
uuid: c0d8b01e-a135-4ef7-8159-811766929f62
exl-id: 1c886f60-eae9-48c2-b641-396c622035d4
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Hoe verkrijg ik deze Data_{#how-do-i-acquire-this-data}

U moet Sensor installeren en uitvoeren op elke webserver die de inhoud voor uw site levert om alle aanvragen te verzamelen die door deze servers worden bekeken.

Deze verzoeken betreffen 90% of meer van de aanvragen die op uw site zijn ingediend en 90% of meer van de gegevens die nodig zijn voor de volledige analyse van het verkeer van uw site. [!DNL Page Tags] moet vervolgens worden gebruikt om de resterende 10% of minder van de verkeersgegevens te verzamelen die niet bekend zijn bij uw webservers. De volgende, echter, zijn geldige configuraties voor de inzameling van de gegevens van het Webverzoek van uw plaats, in volgorde van voorkeur, die op onze operationele ervaring wordt gebaseerd:

1. [!DNL Sensor] is geïnstalleerd op elke webserver die u beheert en die uw site ondersteunt. Inhoud van externe sites, inhoud die wordt aangeboden vanuit cache en bepaalde typen dynamische inhoud moeten worden gecodeerd. Dergelijke paginatags moeten de gegevens die ze verzamelen verzenden naar een webserver op uw locatie waarop [!DNL Sensor] wordt uitgevoerd. U kunt een extra webserver toevoegen als het niveau van het aanvraagverkeer voor paginatags dit rechtvaardigt, of in speciale gevallen een webserver toewijzen om deze aanvragen voor paginatags te verzamelen.
1. [!DNL Sensor] wordt geïnstalleerd op twee webservers, ook wel gegevensverzamelingsservers genoemd in deze handleiding, op uw locatie die zijn bestemd voor het verzamelen van aanvraaggegevens voor paginatags van gecodeerde pagina&#39;s. Alle inhoud op uw site is gelabeld en alle paginatags worden naar de twee servers voor gegevensverzameling geleid.
1. [!DNL Sensor’s] de diensten van de gegevensinzameling worden verleend door een outsourcer die de servers van de gegevensinzameling in werking stelt om al uw gegevens van het Webverzoek te verzamelen. In dit geval wordt alle inhoud op uw site gelabeld en verzenden de paginatags de gegevens naar de servers voor outsourced gegevensverzameling.

   Voor meer informatie over [!DNL Sensor], zie *Data Workbench [!DNL Sensor] Gids*.
