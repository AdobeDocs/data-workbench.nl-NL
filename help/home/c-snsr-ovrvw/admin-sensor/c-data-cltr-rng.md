---
description: Controleer of de verzamelaar andere methoden gebruikt.
title: Bevestigend dat de Collector van Gegevens loopt
uuid: e5b9b12a-b8a5-4c00-abe5-e824516d46b7
exl-id: 1235d741-1ddf-4a65-8377-3d8a9b4ba0d3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Bevestigend dat de Collector van Gegevens{#confirming-that-the-data-collector-is-running} loopt

Controleer of de verzamelaar andere methoden gebruikt.

**Aanbevolen frequentie:** elke 5-10 minuten

* [Gebruik de functie Site Test in de zender.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-a5a697c3252e40f184c0b662926170f2)
* [Controleer  [!DNL Sensor] of een cookie is ingesteld.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-365a0182474c4dc9a5372d3e984f53de)

## Sitetest gebruiken {#section-a5a697c3252e40f184c0b662926170f2}

Één manier om te verifiëren dat de inzamelaar loopt is de functie van de Test van de Plaats in de zender toe te laten. Wanneer u de Test van de Plaats toelaat, verzendt de zender periodiek (om de 60 seconden) een verzoek van de GET naar de Webserver waarop de inzamelaar loopt. Als de Test van de Plaats geen reactie van de Webserver krijgt, schrijft het een foutenmelding aan syslog en verzendt een foutenmelding naar [!DNL data workbench server] (die aan het sensor-logboek dossier wordt geschreven).

Als de Test van de Plaats een reactie van de Webserver ontvangt, zoekt het in het rijdossier voor een pakket van de Webserver. Als het pakket niet verschijnt (erop wijzend dat de inzamelaar niet liep om de gebeurtenis te vangen), schrijft de Test van de Plaats een foutenmelding aan syslog en verzendt een foutenmelding naar Adobe (die ook aan het sensor-logboek dossier wordt geschreven).

In de verzoeken die de Test van de Plaats naar de Webserver verzendt, plaatst de Test van de Plaats de gebruiker-Agent waarde aan &quot;[!DNL Sensor] Test.&quot; Als u niet deze verzoeken om in uw dataset wilt verschijnen, voeg &quot;[!DNL Sensor] Test&quot;Gebruiker-Agent aan [!DNL Baseline Robots List.txt] dossier of [!DNL Extended Robots List.txt] dossier in [!DNL Lookups] omslag op [!DNL data workbench server] toe.

**Sitetest inschakelen in de zender**

1. Zoek het [!DNL txlogd.conf]-bestand op de computer waarop [!DNL Sensor] wordt uitgevoerd en open het in een teksteditor.

1. Zoek in het [!DNL txlogd.conf]-bestand de regel SiteTest en configureer deze zoals hieronder wordt weergegeven. Als uw [!DNL txlogd.conf] dossier niet de lijn &quot;SiteTest&quot;omvat, voeg eenvoudig de lijn aan het eind van het configuratiedossier toe.

   SiteTest http, *serverAddress*, *port*, *resource*

   waarbij *serverAddress* de naam of het IP-adres van de webserver is, *port* de HTTP-luisterpoort van de server is en *resource* de specifieke bron die u bij het testen van de server wilt laten opvragen bij Site Test. Merk op dat *resource* een vraagkoord kan omvatten.

   Voorbeeld: SiteTest http,localhost,80,/index.jsp

   Als u meerdere webservers wilt testen, geeft u gewoon meerdere SiteTest-regels op.

## Controleren op een cookie {#section-365a0182474c4dc9a5372d3e984f53de}

Een andere manier om te controleren of de verzamelaar op een webserver wordt uitgevoerd, is te controleren of [!DNL Sensor] een cookie instelt in de reacties die de webserver retourneert aan clients. Als de verzamelaar werkt, retourneert de webserver een &quot;v1st&quot;-cookie.

U kunt de naam van het cookie wijzigen. Als u dit hebt gedaan, moet u naar de opgegeven naam zoeken, niet naar v1st.

U kunt deze controle uitvoeren gebruikend een geautomatiseerd manuscript of controleagent. Neem contact op met de Adobe Consulting Services voor een voorbeeldscript of aanvullende hulp bij deze taak.
