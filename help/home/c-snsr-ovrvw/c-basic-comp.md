---
description: De sensor bestaat uit drie belangrijkste componentenGegevens Collector, de Rij van de Schijf, en de Transmitter van Gegevens.
title: Wat zijn basiscomponenten
uuid: 32e6e8d9-90ee-4db1-8883-dbdf245df26f
exl-id: aee6a601-590a-43e0-aeeb-42a4522e55c8
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Wat zijn basiscomponenten{#what-are-basic-components}

{{eol}}

Sensor bestaat uit drie hoofdcomponenten: Gegevensverzamelaar, Schijfwachtrij en Gegevenszender.

![](assets/Visual-Sensor.png)

## Gegevensverzameling {#section-f970eaff30364a3c8106d5ec9c1b5caa}

De gegevensverzamelaar (verzamelaar) is een NSAPI-, ISAPI-, J2EE-filterservlet- of Apache-module die wordt uitgevoerd in het webserverproces.

De onbewerkte gebeurtenisgegevens worden vastgelegd voor elke HTTP-aanvraag die de webserver verwerkt en opslaat in de schijfwachtrij. Als u meerdere instanties van een webserver op dezelfde computer uitvoert, laadt elke instantie de eigen instantie van de verzamelaarmodule. nochtans, schrijven alle instanties van de inzamelaar hun gebeurtenisgegevens aan de zelfde schijfrij.

## Schijfwachtrij {#section-41aac77ab30e48478d1b31eac288df05}

De schijfrij (rij) is fout-verdraagzaam, FIFO (eerst binnen, eerst uit) geheugen-in kaart gebrachte rijdossier dat buffert de ruwe gebeurtenisgegevens die Sensor verzamelt, die tijdelijke opslag voor verzamelde gebeurtenisgegevens op de Webserver verstrekken waar het geïnstalleerd is.

Om te voorkomen dat de wachtrij zonder beperkingen wordt uitgebreid (en daardoor alle beschikbare schijfruimte verbruikt), wordt de wachtrij in een bestand met een vaste grootte onderhouden. Dit houdt in dat de wachtrij alleen zoveel gebeurtenisgegevens bevat als er capaciteit voor is. De grootte van het rijdossier wordt gevormd in de parameter QueueSize van het de configuratiedossier van de Sensor, txlogd.conf, wanneer de Sensor wordt geïnstalleerd. Voor informatie over de parameters txlogd.conf, zie de Parameters van het Dossier van Txlogd.conf.

Zodra gevestigd, groeit de fysieke lengte van het dossier niet of krimpt. De inzamelaar zet eenvoudig nieuwe gebeurtenisgegevens in de rij en de zender trekt gebeurtenissen van het. Als de verzamelaar het einde van het bestand bereikt, wordt het schrijven naar het rijbestand gestopt.

Over het algemeen, trekt de zender gebeurtenissen van de rij zo snel aangezien de inzamelaar hen bewaart. Nochtans, als de verbinding tussen de zender en de Server van het Inzicht langzaam of niet beschikbaar is, kan de rij met niet-verzonden gebeurtenissen vullen. In deze gebeurtenis stopt de verzamelaar met het verzamelen van gegevens totdat de zender de wachtrij tekent. Informatie over verzoeken dat de Webserver tijdens dit tijd verwerkt permanent wordt verloren.

**De grootte van de wachtrij bepalen**

Voordat u Sensor installeert, moet u bepalen hoe groot de wachtrij moet zijn. Om permanent gegevensverlies te verhinderen, is het belangrijk om een rij tot stand te brengen die groot genoeg is om het aantal gebeurtenissen aan te passen die tijdens langste waarschijnlijke stroomonderbreking van de verbinding aan de Server van het Inzicht (namelijk voldoende opslag voor verscheidene dagen van piekactiviteit) zouden kunnen accumuleren. De rij moet worden gevormd om genoeg gebeurtenisgegevens te houden zodat de systeembeheerders tijd hebben om netwerktoegankelijkheid aan de server van het doelInzicht te herstellen, of de Server van het Inzicht te herstellen of te vervangen zonder om het even welke gegevens te verliezen. Als de sensor is mislukt en een geldig en toegankelijk rijbestand niet beschikbaar is om de gebeurtenisgegevens te bevatten, gaan de volgende gegevens verloren.

>[!NOTE]
>
>Het is belangrijk dat de beheerders van elke machine waarop de Sensor in werking stelt de unieke aard van het lokale rijdossier begrijpen om ervoor te zorgen dat zij het niet behandelen als een gewoon logboekdossier dat kan worden geschrapt, worden gearchiveerd, of worden samengeperst.

Adobe raadt aan dat de wachtrij wordt geconfigureerd om minstens tien (10) piekdagen gebeurtenisgegevens te bevatten die worden geproduceerd door de server waarop de sensor is geïnstalleerd. Dat wil zeggen, neem de hoeveelheid gebeurtenisgegevens van een piekdag in het laatste jaar en vermenigvuldig deze met tien.

Deze aanbeveling gaat uit van het volgende:

* Het team van de Technologie van uw bedrijf controleert elke Sensor op de wijze die in Administering Sensor, van deze gids wordt beschreven en doet dit minstens eenmaal per dag. Indien dit niet het geval is, moet deze termijn op passende wijze worden verlengd.
* Het IT-team van uw bedrijf kan de netwerktoegankelijkheid herstellen of geïnstalleerde Insight Servers binnen 72 uur vervangen of repareren. Indien dit niet het geval is, moet deze termijn op passende wijze worden verlengd.
* De configuratie van Sensor blijft ongewijzigd.
* Geen externe gebeurtenissen (bijvoorbeeld een grote marketingcampagne) zorgen ervoor dat de hoeveelheid gebeurtenisgegevens die door de webservers worden gegenereerd, aanzienlijk toeneemt.

Uw keuze van rijgrootte hangt grotendeels van het gewenste niveau van systeemcontrole in het licht van de praktijken en het beleid van uw bedrijf betreffende reactietijden en weekend/vakantie systeembeleid af. Aangezien de grotere rijgrootte beter is, adviseert Adobe dat uw bedrijf de rij zo groot mogelijk maakt.

>[!NOTE]
>
>Grotere bestandsgrootten in de wachtrij zijn niet van invloed op de prestaties.

Voor verdere aanbevelingen over het rangschikken van de rij, contacteer de Raadplegende Diensten van de Adobe.

## Gegevensverzending {#section-2dc03d37d73b4cc6bdd5af6b346350d4}

De zender is een onafhankelijk proces (bijvoorbeeld, een daemon op een op UNIX-Gebaseerde computer of de dienst op een computer van Vensters) dat op de zelfde machine zoals de Webserver uitvoert.

De zender leest de gebeurtenisgegevens van de schijfrij, comprimeert het, en verzendt het via HTTP/S naar de Server van het Inzicht die u hebt gespecificeerd, waar het wordt verwerkt en opgeslagen in **.vsl** bestanden.
