---
description: Het DeviceAtlas JSON-bestand wordt nu samen met de bestanden DeviceAtlas.dll en DeviceAtlas64.dll gedistribueerd in een .bundle-bestand (de naam .tar.gz).
title: DeviceAtlas-distributie
uuid: 1eb76c61-6696-4e6c-a3fd-61c00cc17b0a
exl-id: e9671810-d32c-4ec4-a1cb-54b71c6f101c,333507bb-3e8b-4da1-8218-b35fcf8d5f80,aa811c7b-ef80-4f23-b395-0cbb7d2677a9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# DeviceAtlas-distributie{#deviceatlas-distribution}

{{eol}}

Het DeviceAtlas JSON-bestand wordt nu samen met de bestanden DeviceAtlas.dll en DeviceAtlas64.dll gedistribueerd in een .bundle-bestand (de naam .tar.gz).

Wanneer de beheerder de Server van het Inzicht aan versie 6.0 bevordert, is het bestand DeviceAtlas.bundle inbegrepen met het verbeteringspakket in het profiel van de Software en van Docs (softdocs profiel) dat bij:

[!DNL Server Packages > v6.00 > Server_6.00.zip]

Het bestand DeviceAtlas.bundle wordt geëxtraheerd naar [!DNL Server\Lookups\DeviceAtlas].

Het bestand DeviceAtlas.bundle moet worden geplaatst in een map die is gesynchroniseerd met de DPU&#39;s en het bestand DeviceAtlas.cfg dat overeenkomt met de nieuwe DeviceAtlasComponent moet in de map &quot;Components for Processing Servers&quot; op de master synchronisatie worden geplaatst. Wanneer het bestand DeviceAtlas.bundle wordt gewijzigd, krijgt de volgende opzoekvraag van DeviceAtlas resultaten op basis van de bijgewerkte API- en/of JSON-bestanden.

## Het bestand Transformation.cfg wijzigen {#section-394823348f5740028666e62e2bd42754}

De transformaties DeviceAtlas hoeven niet langer het pad naar het JSON-bestand op te geven. Eerdere DeviceAtlasTransformation die in het bestand transformation.cfg is gedefinieerd, mag niet langer de parameter File bevatten die naar het verduisterde JSON-bestand wijst.

In dit voorbeeld wordt in het bestand Transformation.cfg het argument File weergegeven dat moet worden verwijderd om verwarring te voorkomen. (Als u het weglaat, veroorzaakt dit geen schade, maar alleen potentiële verwarring omdat het genegeerd wordt.)

```
6 = DeviceAtlasTransformation:  
  Comments = Comment: 0 items  
  Condition = AndCondition: 0 items

<b></b> 
<filepath>
  File = string: Lookups\\DeviceAtlas\\20110106_private.json.obfuscated 
</filepath> 
  ^^ DELETE THE ABOVE LINE FROM ALL PREVIOUS TRANSFORMATIONS ^^  
 
  Name = string: DeviceAtlas Lookup  
  Outputs = vector: 4 items  
    0 = Column:  
      Column Name = string: vendor  
      Field Name = string: x-vendor  
    1 = Column:  
      Column Name = string: model  
      Field Name = string: x-model  
    2 = Column:  
      Column Name = string: isBrowser  
      Field Name = string: x-isbrowser  
    3 = Column:  
      Column Name = string:usableDisplayHeight  
      Field Name = string: x-usable-display-height 
User Agent = string: x-ua  
```

## Het bestand DeviceAtlas.cfg wijzigen {#section-10b43705a6c846fd9ec54ea6be249f88}

Dit is een voorbeeld van het [!DNL component] in het bestand DeviceAtlas.cfg is vereist.

```
component = DeviceAtlasComponent: 
  DeviceAtlas Bundle File = string:Lookups\\DeviceAtlas\\DeviceAtlas.bundle 
  Unsynchronized Bundle Extraction Path = string: Temp\\DeviceAtlas\\
```

Dit bestand DeviceAtlas.bundle wordt vanuit het perspectief van de functie voor profielsynchronisatie op dezelfde manier behandeld als een configuratiebestand. Bovendien worden de JSON-gegevens en het DLL-bestand gebruikt op componentniveau in plaats van op individueel transformatieniveau.

Een nieuwe DeviceAtlasComponent, bij opstarten, vindt de .bundle samenklontering, de-obfuscates het JSON- dossier in geheugen, haalt de dossiers in een tijdelijke folder uit, en laadt aangewezen DLL voor het lopende platform. Deze component controleert ook de wijzigingen in het bundelbestand en laadt het DLL- en Cfg-bestand automatisch opnieuw als het wordt gewijzigd.

## DeviceAtlas uitvoeren {#section-6ed37b39199d4ffd95d30b49a7ee9666}

De correcte configuratie maakt een groot verschil in de tijd die voor transformatie wordt vereist. De transformatie kan worden geconfigureerd om slechts eenmaal per bezoeker per sessie te worden uitgevoerd, zodat DeviceAtlas het proces kan versnellen.

**Indien geïmplementeerd met behulp van Log Processing.cfg**:

Voer de transformaties tweemaal uit.

1. Alleen de knop Opzoeken [!DNL mobile id] veld, dan
1. Voorwaarden maken om de [!DNL mobile id] en dan de rest van de velden opzoeken.

**Indien geïmplementeerd met Transformation.cfg**:

Implementeer zoals in Stap 1 in de logverwerking hierboven, of gebruik kruisrijen ter ondersteuning van een voorwaardelijke instelling.

* Cross-Rows - Pak de vorige zittingssleutel. Geef vervolgens aan of de huidige sessiesleutel afwijkt van de sleutel die met kruisrijen wordt gevonden. Als dat het geval is, wordt de transformatie DeviceAtlas slechts op één record per sessie uitgevoerd.
