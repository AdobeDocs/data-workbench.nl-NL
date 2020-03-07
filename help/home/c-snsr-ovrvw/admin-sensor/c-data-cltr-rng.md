---
description: Controle of de inzamelaar gebruikend verschillende methodes in werking stelt.
solution: Insight
title: Bevestigend dat de Collector van Gegevens loopt
uuid: e5b9b12a-b8a5-4c00-abe5-e824516d46b7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bevestigend dat de Collector van Gegevens loopt{#confirming-that-the-data-collector-is-running}

Controle of de inzamelaar gebruikend verschillende methodes in werking stelt.

**Aanbevolen frequentie:** Om de 5-10 minuten

* [Gebruik de Functionaliteit van de Test van de Plaats in de zender.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-a5a697c3252e40f184c0b662926170f2)
* [Controleer of [!DNL Sensor] een cookie instelt.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-365a0182474c4dc9a5372d3e984f53de)

## Werken met sitetest {#section-a5a697c3252e40f184c0b662926170f2}

Één manier om te verifiëren dat de inzamelaar loopt is de functie van de Test van de Plaats in de zender toe te laten. Wanneer u de Test van de Plaats toelaat, verzendt de zender periodiek (om de 60 seconden) een GET verzoek naar de Webserver waarop de inzamelaar loopt. Als de Test van de Plaats geen reactie van de Webserver krijgt, schrijft het een foutenmelding aan syslog en verzendt een foutenmelding naar [!DNL data workbench server] (die aan het sensor-logboek dossier wordt geschreven).

Als de Test van de Plaats een reactie van de Webserver ontvangt, kijkt het in het rijdossier voor een pakket van de Webserver. Als het pakket niet verschijnt (erop wijzend dat de inzamelaar niet liep om de gebeurtenis te vangen), schrijft de Test van de Plaats een foutenmelding aan syslog en verzendt een foutenmelding naar Adobe (die ook aan het sensor-logboek dossier wordt geschreven).

In de verzoeken dat de Test van de Plaats naar de Webserver verzendt, plaatst de Test van de Plaats de gebruiker-agent waarde aan &quot; [!DNL Sensor] Test.&quot; Als u deze verzoeken niet in uw dataset wilt verschijnen, voeg de &quot; [!DNL Sensor] Test&quot;gebruiker-Agent aan het [!DNL Baseline Robots List.txt] dossier of het [!DNL Extended Robots List.txt] dossier in de [!DNL Lookups] omslag op toe [!DNL data workbench server].

**Om de Test van de Plaats in de zender toe te laten**

1. Bepaal de plaats van het [!DNL txlogd.conf] dossier op de machine waar [!DNL Sensor] loopt en open het in een tekstredacteur.

1. In het [!DNL txlogd.conf] dossier, bepaal de plaats van de lijn &quot;SiteTest&quot;en vorm het zoals hieronder getoond. Als uw [!DNL txlogd.conf] dossier niet de lijn &quot;SiteTest&quot;omvat, voeg eenvoudig de lijn aan het eind van het configuratiedossier toe.

   SiteTest http, *serverAddress*, *poort*, *resource*

   waar *serverAddress* de naam van de Webserver of IP adres is, is de *haven* de het luisteren haven van HTTP van de server, en het *middel* is het specifieke middel dat u de Test van de Plaats wilt verzoeken wanneer het testen van de server. Merk op dat het *middel* een vraagkoord kan omvatten.

   Voorbeeld: SiteTest http,localhost,80,/index.jsp

   Om veelvoudige Webservers te testen, specificeert u eenvoudig veelvoudige lijnen SiteTest.

## Een cookie controleren {#section-365a0182474c4dc9a5372d3e984f53de}

Een andere manier om te verifiëren dat de inzamelaar op een Webserver loopt is te controleren of [!DNL Sensor] plaatst een koekje in de reacties die de Webserver aan cliënten terugkeert. Als de collector werkt, geeft de webserver een &#39;v1st&#39; cookie terug.

Het is mogelijk om het koekje anders te noemen. Als u dit hebt gedaan, moet u de gespecificeerde naam zoeken, niet v1st.

U kunt deze controle uitvoeren gebruikend een geautomatiseerd manuscript of controleagent. Voor een steekproefmanuscript of extra hulp met deze taak, te contacteren gelieve de Raadplegende Diensten van Adobe.
