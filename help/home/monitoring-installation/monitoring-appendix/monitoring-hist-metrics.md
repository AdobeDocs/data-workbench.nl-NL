---
description: In het volgende voorbeeld worden de metriek weergegeven die is opgenomen in het Historische controleprofiel van de gegevenswerkbank en hoe deze zijn afgeleid.
title: Metriek in het historisch controleprofiel van de Data Workbench
uuid: 47b874f7-8acb-4593-9ac9-5997d5279e52
exl-id: 65f0f605-f128-45bb-8f6c-95284b2da740
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Metriek in het Historische de Controleprofiel van de Data Workbench{#metrics-in-the-data-workbench-historical-monitoring-profile}

In het volgende voorbeeld worden de metriek weergegeven die is opgenomen in het Historische controleprofiel van de gegevenswerkbank en hoe deze zijn afgeleid.

| **Waarschuwingscritici** | De som van de waarschuwingsdimensie voor elke pingelt. |
|---|---|
| **Waarschuwingspunten** | De som van de Waarschuwing neer afmeting voor elke Ping. |
| **Waarschuwingen** | De som van de waarschuwingsafmetingen voor elke pingelt. |
| **Alle componenten** | De telling van Pings waar de Succes van de Controle van de Component &quot;1&quot;gedeeld door metrische pings vermenigvuldigd met 100 gelijk is. |
| **Vanaf vertragingsminuten** | Deze metrisch is de som van de notulen van de Vertraging van elke pingelt, dan die door metrisch pingelt wordt gedeeld. |
| **Blokken** | De som van één voor elk blok. |
| **Alles blokkeren** | Alle blokken. |
| **Totale capaciteit** | De metrische tijden 2 van de Grootte van de Capaciteit plus metrisch van de Rij van de Capaciteit, gedeeld door 3. |
| **Capaciteitsrij** | De som van de afmeting van het Percentage van de Rij van de Capaciteit voor elke pingelt die door metrisch pingelt wordt gedeeld. |
| **Capaciteitsgrootte** | De som van de afmeting van het Percentage van de Grootte van de Capaciteit voor elke pingelt, gedeeld door metrisch pingelt. |
| **Communicatie** | Het aantal pingelt waar het Snelle Succes van de Controle &quot;1&quot;aanpast, gedeeld door metrisch pingelt. |
| **Gedetailleerde controle seconden** | De som Gedetailleerde Controle Seconds afmeting voor elk pingelt waar pingelt type &quot;server&quot;is, die door metrisch pingelt wordt verdeeld. |
| **Dimension GigaBytes** | De som van Dimension gigabytes voor elke pingelt, gedeeld door metrische pingelen. |
| **Schijf &quot;x&quot;** | De metriek van de Schijf wordt berekend door de som van hun Schijf te nemen Gebruikte Percentage voor elk pingelt, die door metrisch pingelt wordt gedeeld. |
| **Geschatte zweepminuten** | Dit is de som van de geschatte schelpdierecondes van de kneep voor elke pingelt, gedeeld door de pingmeting waarbij de geschatte schelpdiereconds van de kneep groter is dan nul, gedeeld door 6. |
| **Snelle invoer MB per minuut** | De som snelle input MegaBytes per minuut voor elke pingelt die door het aantal pingelt wordt gedeeld wanneer de Snelle Input MegaBytes per Minuut groter is dan nul. |
| **Modus voor snelle invoer** | Pingelt waar de afmeting van de Wijze van de Verwerking aan &quot;Snelle input&quot;gelijk is gedeeld door Pings. |
| **Snel MegaBytes samenvoegen per minuut** | De som Snelle Megabytes van de Fusie per Minuut voor elke pingelt, die door metrische pingelt wordt gedeeld. |
| **Modus Snel samenvoegen** | Pingelt waar de Wijze van de Verwerking &quot;snelle fusie&quot;die door metrisch pingelt evenaart. |
| **Veld GigaBytes** | De som van de afmetingen van het Gebied in gigabytes voor elke Ping gedeeld door metrische Pingen. |
| **Laden** | De som van de Gemiddelde afmeting van de Lading voor elke Ping, gedeeld door metrisch pingelt. |
| **Log lezen** | De som de afmeting van de Verwerking van de Lezing van het Logboek voor elke pingelt, gedeeld door metrisch pingelt, allen gedeeld door 10. |
| **Geheugenpagina** | De som van het Percentage van het Dossier van de Pagina van het Geheugen voor elke pingelt, gedeeld door metrisch pingelt. |
| **Fysiek geheugen** | De som van de Fysieke dimensie van het Percentage van het Geheugen voor elke pingelt, gedeeld door metrisch pingelt. |
| **Geheugenquery** | De som van het Percentage van de Vraag van het Geheugen voor elke pingelt, die door metrisch pingelt wordt gedeeld. |
| **Geheugen in totaal GB** | De som Fysieke MegaBytes van het Geheugen Totale afmeting voor elke Ping, die door metrische pingelt wordt gedeeld. |
| **Netwerkverbindingen** | Dit is de som van de Verbindingen van het Netwerk voor elk pingelt die door metrisch pingelt wordt verdeeld. |
| **Totaal pings x capaciteit** | De pingelt metrisch vermenigvuldigd met de Totale metrisch van de Capaciteit. |
| **Milliseconden opiniepeilingen** | De som van de Centisecondedimensie van de Latentie van de Opiniepeiling voor elke Ping, die door metrische pingelt wordt gedeeld, allen vermenigvuldigd met 10. |
| **Query uitvoeren** | De som van één voor elke pingelt waar de Geschatte Dekaseconds van de Sneep groter is dan &quot;0&quot;, gedeeld door metrische pingelt waar het Pingstype &quot;server&quot;evenaart. |
| **Seconden snel controleren** | De som Seconden van de Snelle Controle voor elke Ping waar het Pingstype aan &quot;server&quot;gelijk is, gedeeld door metrisch Pingt. |
| **Rijen uitvoeren** | De som afmeting van de Rijen van de Output voor elk pingelt gedeeld door metrisch pingelt, vermenigvuldigd met 100000. |
| **Real-time modus** | Het aantal pingen waar de afmeting van de Wijze van de Verwerking &quot;real time&quot;gelijk is, gedeeld door metrisch pingelt, allen vermenigvuldigd met 100. |
| **Verwerkingsmodus** | 100 minus het aantal Pings waar de Wijze van de Verwerking &quot;real time&quot;gedeeld door metrische Pings, vermenigvuldigd met 100 gelijk is. |
| **Gestopt** | The sum of the Processing Stalled afmetingen in the Insight [Profile Status](../../../home/monitoring-installation/monitoring-appendix/monitoring-profile-status.md#concept-d4cd7da41c8a42bab4aea25418264e64) profile. |
| **Temp DB** | De som van het Ruimtepercentage van de Ruimte van TempDB voor elke pingelt, gedeeld door metrisch pingelt. |
| **Transformatie** | De som van het Percentage van de Transformatie voor elke pingelt die door metrische pingelt allen wordt gedeeld gedeeld door 10. |
