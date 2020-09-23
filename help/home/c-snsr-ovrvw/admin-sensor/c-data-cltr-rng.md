---
description: Controleer of de verzamelaar andere methoden gebruikt.
solution: Analytics
title: Bevestigend dat de Collector van Gegevens loopt
uuid: e5b9b12a-b8a5-4c00-abe5-e824516d46b7
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Bevestigend dat de Collector van Gegevens loopt{#confirming-that-the-data-collector-is-running}

Controleer of de verzamelaar andere methoden gebruikt.

**Aanbevolen frequentie:** Elke 5-10 minuten

* [Gebruik de functie Site Test in de zender.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-a5a697c3252e40f184c0b662926170f2)
* [Controleer [!DNL Sensor] of een cookie is ingesteld.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-365a0182474c4dc9a5372d3e984f53de)

## Site testen {#section-a5a697c3252e40f184c0b662926170f2}

Één manier om te verifiëren dat de inzamelaar loopt is de functie van de Test van de Plaats in de zender toe te laten. Wanneer u de Test van de Plaats toelaat, verzendt de zender periodiek (om de 60 seconden) een verzoek van de GET naar de Webserver waarop de inzamelaar loopt. Als de Test van de Plaats geen reactie van de Webserver krijgt, schrijft het een foutenmelding aan syslog en verzendt een foutenmelding naar [!DNL data workbench server] (die aan het sensor-logboek dossier wordt geschreven).

Als de Test van de Plaats een reactie van de Webserver ontvangt, zoekt het in het rijdossier voor een pakket van de Webserver. Als het pakket niet verschijnt (erop wijzend dat de inzamelaar niet liep om de gebeurtenis te vangen), schrijft de Test van de Plaats een foutenmelding aan syslog en verzendt een foutenmelding naar Adobe (die ook aan het sensor-logboek dossier wordt geschreven).

In de verzoeken die de Test van de Plaats naar de Webserver verzendt, plaatst de Test van de Plaats de gebruiker-Agent waarde aan &quot; [!DNL Sensor] Test.&quot; Als u deze verzoeken niet in uw dataset wilt verschijnen, voeg &quot; [!DNL Sensor] Test&quot;gebruiker-Agent aan het [!DNL Baseline Robots List.txt] dossier of het [!DNL Extended Robots List.txt] dossier in de [!DNL Lookups] omslag op [!DNL data workbench server].

**Sitetest inschakelen in de zender**

1. Zoek het [!DNL txlogd.conf] bestand op de computer waarop het [!DNL Sensor] wordt uitgevoerd en open het in een teksteditor.

1. Zoek in het [!DNL txlogd.conf] bestand de regel SiteTest en configureer deze zoals hieronder wordt weergegeven. Als uw [!DNL txlogd.conf] bestand de regel SiteTest niet bevat, voegt u gewoon de regel toe aan het einde van het configuratiebestand.

   SiteTest http, *serverAddress*, *port*, *resource*

   waarbij *serverAddress* de naam of het IP-adres van de webserver is, is de *poort* de HTTP-luisterpoort van de server en is de *bron* de specifieke bron die de Site Test moet aanvragen bij het testen van de server. Merk op dat de *bron* een vraagkoord kan omvatten.

   Voorbeeld: SiteTest http,localhost,80,/index.jsp

   Als u meerdere webservers wilt testen, geeft u gewoon meerdere SiteTest-regels op.

## Controleren op een cookie {#section-365a0182474c4dc9a5372d3e984f53de}

Een andere manier om te controleren of de verzamelaar op een webserver wordt uitgevoerd, is te controleren of een cookie [!DNL Sensor] wordt ingesteld in de reacties die de webserver naar clients retourneert. Als de verzamelaar werkt, retourneert de webserver een &quot;v1st&quot;-cookie.

U kunt de naam van het cookie wijzigen. Als u dit hebt gedaan, moet u naar de opgegeven naam zoeken, niet naar v1st.

U kunt deze controle uitvoeren gebruikend een geautomatiseerd manuscript of controleagent. Neem contact op met de Adobe Consulting Services voor een voorbeeldscript of aanvullende hulp bij deze taak.
