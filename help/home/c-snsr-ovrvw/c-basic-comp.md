---
description: De sensor bestaat uit drie belangrijke componentenGegevensverzamelaar, de Rij van de Schijf, en de Overdracht van Gegevens.
title: Wat zijn basiscomponenten
uuid: 32e6e8d9-90ee-4db1-8883-dbdf245df26f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Wat zijn basiscomponenten{#what-are-basic-components}

Sensor bestaat uit drie hoofdcomponenten: De Collector van gegevens, de Rij van de Schijf, en de Transmitter van Gegevens.

![](assets/Visual-Sensor.png)

## Gegevensverzamelaar {#section-f970eaff30364a3c8106d5ec9c1b5caa}

De gegevensverzamelaar (inzamelaar) is een NSAPI, ISAPI, J2EE filterservlet, of module Apache die binnen het proces van de Webserver uitvoert.

Het vangt de ruwe gebeurtenisgegevens over elk HTTP- verzoek dat de Webserver verwerkt en die informatie in de schijfrij opslaat. Als u veelvoudige instanties van een Webserver op de zelfde machine in werking stelt, laadt elke instantie zijn eigen instantie van de collectormodule; nochtans, schrijven alle instanties van de inzamelaar hun gebeurtenisgegevens aan de zelfde schijfrij.

## Schijfwachtrij {#section-41aac77ab30e48478d1b31eac288df05}

De schijfrij (rij) is een fout-verdraagzaam, FIFO (eerst in, eerst uit) geheugen-in kaart gebrachte rijdossier dat als buffer optreedt voor de ruwe gebeurtenisgegevens die Sensor verzamelt, die tijdelijke opslag verstrekken voor verzamelde gebeurtenisgegevens over de Webserver waar het wordt geïnstalleerd.

Om de rij te verhinderen zonder beperking (en daardoor verbruikend al beschikbare schijfruimte) uit te breiden, wordt de rij gehandhaafd in een be*vestigen-groottedossier, betekenend dat het slechts zo veel gebeurtenisgegevens houdt aangezien het capaciteit om is gegeven te houden. De grootte van het rijdossier wordt gevormd in de parameter QueueSize van het de configuratiedossier van de Sensor, txlogd.conf, wanneer de Sensor geïnstalleerd is. Voor informatie over de parameters txlogd.conf, zie de Parameters van het Dossier van de Sensor Txlogd.conf.

Zodra gevestigd, groeit de fysieke lengte van het dossier niet of krimpt. De inzamelaar zet eenvoudig nieuwe gebeurtenisgegevens in de rij op en de zender trekt gebeurtenissen van het. Als de inzamelaar het eind van het dossier bereikt, houdt het op schrijvend aan het rijdossier.

Over het algemeen, trekt de zender gebeurtenissen van de rij zo snel zoals de inzamelaar hen opslaat. Nochtans, als de verbinding tussen de zender en de Server van het Inzicht langzaam of niet beschikbaar is, kan de rij met niet overgebrachte gebeurtenissen vullen. In deze gebeurtenis, houdt de inzamelaar op verzamelend gegevens tot de zender onderaan de rij trekt. De informatie over verzoeken dat de processen van de Webserver tijdens deze tijd permanent wordt verloren.

**Het bepalen van de Grootte van de Rij**

Alvorens u Sensor installeert, moet u bepalen hoe groot de rij moet zijn. Om blijvend gegevensverlies te verhinderen, is het belangrijk om een rij te creëren die groot genoeg is om het aantal gebeurtenissen aan te passen die zich tijdens langste waarschijnlijke stroomonderbreking van de verbinding aan de Server van het Inzicht konden ophopen (namelijk voldoende opslag voor verscheidene dagen van piekactiviteit). De rij moet worden gevormd om genoeg gebeurtenisgegevens te houden zodat de systeembeheerders tijd hebben om netwerktoegankelijkheid aan de Server van het doelInzicht te herstellen, of de Server van het Inzicht te herstellen of te vervangen zonder enige gegevens te verliezen. Als de sensor heeft ontbroken en een geldig en toegankelijk rijdossier niet beschikbaar is om de gebeurtenisgegevens te houden, worden de verdere gegevens verloren.

>[!NOTE]
>
>Het is belangrijk dat de beheerders van elke machine waarop de looppas van de Sensor de unieke aard van het lokale rijdossier begrijpen om ervoor te zorgen dat zij het niet behandelen als gewoon logboekdossier dat kan worden geschrapt, worden gearchiveerd of worden samengeperst.

Adobe adviseert dat de rij wordt gevormd om minstens tien (10) piekdagen van gebeurtenisgegevens te houden die door de server worden geproduceerd waar de Sensor geïnstalleerd is. Dat wil zeggen, neem de hoeveelheid gebeurtenisgegevens van om het even welke piekdag in het afgelopen jaar en vermenigvuldig het met tien.

Deze aanbeveling gaat uit van het volgende:

* Het team van de Technologie van uw bedrijf van de Informatie van uw bedrijf controleert elke Sensor op de manier die in de Zensor van het Beheer, van deze gids wordt gedetailleerd en doet dit minstens eens per dag. Indien dit niet het geval is, moet deze termijn op passende wijze worden verlengd.
* Het team van de Technologie van de Informatie van uw bedrijf kan netwerktoegankelijkheid herstellen of om het even welke geïnstalleerde Servers van het Inzicht vervangen of herstellen binnen 72 uren. Indien dit niet het geval is, moet deze termijn op passende wijze worden verlengd.
* De configuratie van Sensor blijft het zelfde.
* Geen externe gebeurtenissen (bijvoorbeeld, zal een grote marketing campagne) de hoeveelheid gebeurtenisgegevens veroorzaken die door de Webservers worden geproduceerd om beduidend te stijgen.

Uw keus van rijgrootte hangt grotendeels van het gewenste niveau van systeem controle in het licht van de praktijken en het beleid van uw bedrijf betreffende reactietijden en weekend/vakantie systeembeleid af. Aangezien de grotere rijgrootte beter is, adviseert Adobe dat uw bedrijf de rij zo groot mogelijk maakt.

>[!NOTE]
>
>De grotere grootte van het rijdossier heeft geen invloed op prestaties.

Voor verdere aanbevelingen over het rangschikken van de rij, contacteer de Raadplegende Diensten van Adobe.

## Gegevensverzending {#section-2dc03d37d73b4cc6bdd5af6b346350d4}

De zender is een onafhankelijk proces (bijvoorbeeld, een daemon op een op UNIX-Gebaseerde computer of de dienst op een computer van Vensters) dat op de zelfde machine zoals de Webserver uitvoert.

De zender leest de gebeurtenisgegevens van de schijfrij, perst het samen, en verzendt het via HTTP/S naar de Server van het Inzicht die u hebt gespecificeerd, waar het wordt verwerkt en in **.vsl** dossiers opgeslagen.
