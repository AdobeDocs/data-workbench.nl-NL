---
description: U moet Sensor op elke Webserver installeren en in werking stellen die de inhoud voor uw plaats dient om alle verzoeken te verzamelen die door die servers worden gezien.
solution: Analytics
title: Hoe verkrijg ik deze Data_
topic: Data workbench
uuid: c0d8b01e-a135-4ef7-8159-811766929f62
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Hoe verkrijg ik deze Data_{#how-do-i-acquire-this-data}

U moet Sensor op elke Webserver installeren en in werking stellen die de inhoud voor uw plaats dient om alle verzoeken te verzamelen die door die servers worden gezien.

Deze verzoeken vormen 90% of meer van de verzoeken die aan uw plaats worden gedaan en 90% of meer van de gegevens die voor de volledige analyse van het verkeer van uw plaats nodig zijn. [!DNL Page Tags] zou dan moeten worden gebruikt om de resterende 10% of minder verkeersgegevens te verzamelen die niet aan uw Webservers bekend zijn. Het volgende, echter, zijn geldige configuraties voor de inzameling van de gegevens van het Webverzoek van uw plaats, in volgorde van voorkeur, die op onze operationele ervaring wordt gebaseerd:

1. [!DNL Sensor] is geïnstalleerd op elke Webserver die u controleert en die uw plaats steunt. De inhoud van derdeplaatsen, inhoud die van geheim voorgeheugen wordt gediend, en bepaalde types van dynamische inhoud zou moeten worden geëtiketteerd, en dergelijke paginarabels zouden de gegevens moeten verzenden die zij aan een Webserver bij uw plaats verzamelen die loopt [!DNL Sensor]. U kunt een extra Webserver toevoegen als het niveau van het verkeer van het de verzoekverkeer van de paginarag dergelijk rechtvaardigt, of in speciale gevallen, een Webserver wijdt om deze verzoeken van de paginarag te verzamelen.
1. [!DNL Sensor] is geïnstalleerd op twee Webservers, die ook als servers van de gegevensinzameling in deze gids worden bedoeld, bij uw plaats die aan het verzamelen van de gegevens van het de verzoekverzoek van de paginarag van geëtiketteerde pagina&#39;s gewijd zijn. Alle inhoud op uw plaats wordt geëtiketteerd en alle paginarabels worden geleid aan de twee servers van de gegevensinzameling.
1. [!DNL Sensor’s] de diensten van de gegevensinzameling worden verleend door een outsourcer die de servers van de gegevensinzameling in werking stelt om elk van uw gegevens van het Webverzoek te verzamelen. In dit geval, wordt al inhoud op uw plaats geëtiketteerd en de paginamarkeringen verzenden hun gegevens naar de outsourced servers van de gegevensinzameling.

   Voor meer informatie over [!DNL Sensor], zie de *Gids[!DNL Sensor]van de Werkbank van* Gegevens.

