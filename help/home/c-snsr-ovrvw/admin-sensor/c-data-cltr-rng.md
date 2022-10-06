---
description: Controleer of de verzamelaar andere methoden gebruikt.
title: Bevestigend dat de Collector van Gegevens loopt
uuid: e5b9b12a-b8a5-4c00-abe5-e824516d46b7
exl-id: 1235d741-1ddf-4a65-8377-3d8a9b4ba0d3
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Bevestigend dat de Collector van Gegevens loopt{#confirming-that-the-data-collector-is-running}

{{eol}}

Controleer of de verzamelaar andere methoden gebruikt.

**Aanbevolen frequentie:** Elke 5-10 minuten

* [Gebruik de functie Site Test in de zender.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-a5a697c3252e40f184c0b662926170f2)
* [Controleren of [!DNL Sensor] stelt een cookie in.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-365a0182474c4dc9a5372d3e984f53de)

## Site testen {#section-a5a697c3252e40f184c0b662926170f2}

Één manier om te verifiëren dat de inzamelaar loopt is de functie van de Test van de Plaats in de zender toe te laten. Wanneer u de Test van de Plaats toelaat, verzendt de zender periodiek (om de 60 seconden) een verzoek van de GET naar de Webserver waarop de inzamelaar loopt. Als de Test van de Plaats geen reactie van de Webserver krijgt, schrijft het een foutenmelding aan syslog en verzendt een foutenmelding naar [!DNL data workbench server] (wordt geschreven naar het sensorlogbestand).

Als de Test van de Plaats een reactie van de Webserver ontvangt, zoekt het in het rijdossier voor een pakket van de Webserver. Als het pakket niet verschijnt (erop wijzend dat de inzamelaar niet liep om de gebeurtenis te vangen), schrijft de Test van de Plaats een foutenmelding aan syslog en verzendt een foutenmelding naar Adobe (die ook aan het sensor-logboek dossier wordt geschreven).

In de verzoeken die de Test van de Plaats naar de Webserver verzendt, plaatst de Test van de Plaats de gebruiker-Agent waarde aan &quot; [!DNL Sensor] Testen.&quot; Als u deze verzoeken niet in uw dataset wilt verschijnen, voeg &quot; [!DNL Sensor] Gebruiker-Agent van de test aan [!DNL Baseline Robots List.txt] of de [!DNL Extended Robots List.txt] in het [!DNL Lookups] map op de [!DNL data workbench server].

**Sitetest inschakelen in de zender**

1. Zoek de [!DNL txlogd.conf] bestand op de computer [!DNL Sensor] wordt uitgevoerd en geopend in een teksteditor.

1. In de [!DNL txlogd.conf] , zoekt u de regel SiteTest en configureert u deze zoals hieronder wordt weergegeven. Als uw [!DNL txlogd.conf] Het bestand bevat niet de regel SiteTest. Voeg de regel gewoon toe aan het einde van het configuratiebestand.

   SiteTest http, *serverAddress*, *poort*, *resource*

   waar *serverAddress* de naam of het IP-adres van de webserver; *poort* de HTTP-luisterpoort van de server is, en *resource* is de specifieke bron die u bij het testen van de server wilt laten opvragen bij Sitetest. Let op: *resource* kan een queryreeks bevatten.

   Voorbeeld: SiteTest http,localhost,80,/index.jsp

   Als u meerdere webservers wilt testen, geeft u gewoon meerdere SiteTest-regels op.

## Controleren op een cookie {#section-365a0182474c4dc9a5372d3e984f53de}

Een andere manier om te controleren of de verzamelaar op een webserver wordt uitgevoerd, is om te controleren of [!DNL Sensor] stelt een cookie in in de reacties die de webserver retourneert aan clients. Als de verzamelaar werkt, retourneert de webserver een &quot;v1st&quot;-cookie.

U kunt de naam van het cookie wijzigen. Als u dit hebt gedaan, moet u naar de opgegeven naam zoeken, niet naar v1st.

U kunt deze controle uitvoeren gebruikend een geautomatiseerd manuscript of controleagent. Neem contact op met de Adobe Consulting Services voor een voorbeeldscript of aanvullende hulp bij deze taak.
