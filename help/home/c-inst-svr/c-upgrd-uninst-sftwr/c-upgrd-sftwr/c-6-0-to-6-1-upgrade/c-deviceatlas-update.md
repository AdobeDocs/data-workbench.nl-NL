---
description: Het dossier van DeviceAtlas JSON zal nu in een.bundle dossier (anders genoemd .tar.gz) samen met de dossiers van DeviceAtlas.dll en DeviceAtlas64.dll worden verdeeld.
solution: Analytics
title: DeviceAtlas-distributie
topic: Data workbench
uuid: 1eb76c61-6696-4e6c-a3fd-61c00cc17b0a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# DeviceAtlas-distributie{#deviceatlas-distribution}

Het dossier van DeviceAtlas JSON zal nu in een.bundle dossier (anders genoemd .tar.gz) samen met de dossiers van DeviceAtlas.dll en DeviceAtlas64.dll worden verdeeld.

Wanneer de beheerder de Server van het Inzicht aan versie 6.0 bevordert, is het dossier DeviceAtlas.bundle inbegrepen met het verbeteringspakket in het profiel van de Software en van Dos (softwareprofiel) dat bij wordt gevestigd:

[!DNL Server Packages > v6.00 > Server_6.00.zip]

Het bestand DeviceAtlas.bundle wordt geëxtraheerd naar [!DNL Server\Lookups\DeviceAtlas].

Het bestand DeviceAtlas.bundle moet in een directory worden geplaatst die gesynchroniseerd is met de DPU&#39;s en het bestand DeviceAtlas.cfg dat overeenkomt met het nieuwe bestand DeviceAtlasComponent moet worden geplaatst in de directory &quot;Componenten voor Verwerkingsservers&quot; van de synchronisatie-master. Wanneer het ApparaatAtlas.bundle- dossier wordt veranderd, zal de zeer volgende de raadplegingsvraag van DeviceAtlas resultaten krijgen die op het bijgewerkte API en/of JSON- dossier worden gebaseerd.

## Het bestand Transformation.cfg wijzigen {#section-394823348f5740028666e62e2bd42754}

De transformaties DeviceAtlas zullen niet meer te hoeven om de weg aan het JSON dossier te specificeren. Om het even welke vorige DeviceAtlasTransformation die in het transformation.cfg- dossier wordt bepaald zou niet meer de parameter van het Dossier moeten omvatten die aan het verduisterde JSON- dossier richt.

Dit voorbeeld Transformation.cfg- dossier toont het argument van het Dossier dat zou moeten worden geschrapt om verwarring te vermijden. (Als u het daar laat, zal dat geen schade veroorzaken, maar alleen verwarring omdat het genegeerd zal worden.)

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

Dit is een voorbeeld van het [!DNL component] argument dat in het ApparaatAtlas.cfg- dossier wordt vereist.

```
component = DeviceAtlasComponent: 
  DeviceAtlas Bundle File = string:Lookups\\DeviceAtlas\\DeviceAtlas.bundle 
  Unsynchronized Bundle Extraction Path = string: Temp\\DeviceAtlas\\
```

Dit dossier DeviceAtlas.bundle zal enkel als een configuratiedossier vanuit het perspectief van de eigenschap van de Synchronisatie van het Profiel worden behandeld. Bovendien zullen de JSON- gegevens en DLL op het niveau van de Component eerder dan op het individuele niveau van de Transformatie worden gebruikt.

Een nieuwe DeviceAtlasComponent, op opstarten, vindt de .bundle configuratie, de-verduistert het JSON- dossier in geheugen, haalt de dossiers in een tijdelijke folder, en laadt aangewezen DLL voor het lopende platform. Deze component controleert ook veranderingen in het bundeldossier, en herlaadt automatisch het DLL en .cfg dossier als het verandert.

## Apparaat uitvoerenAtlas {#section-6ed37b39199d4ffd95d30b49a7ee9666}

De juiste configuratie maakt een groot verschil in de tijd die voor transformatie wordt vereist. De transformatie kan worden gevormd om slechts één keer per bezoeker per zitting te lopen om DeviceAtlas toe te staan om het proces te versnellen.

**Indien geïmplementeerd met behulp van Log Processing.cfg**:

Voer de transformaties tweemaal uit.

1. Kijk alleen op het [!DNL mobile id] veld, dan
1. Creeer voorwaarden om het te negeren [!DNL mobile id] en dan de rest gebieden op te zoeken.

**Indien geïmplementeerd met Transformation.cfg**:

Stel zoals in Stap 1 in de Verwerking van het Logboek hierboven op, of gebruik dwars-rijen om het voorwaardelijke plaatsen te steunen.

* Kruis-Rijen-greep de vorige zittingssleutel. Dan identificeer als de huidige zittingssleutel van gevonden met dwars-rijen verschillend is. Als zo, dan zal de transformatie DeviceAtlas slechts op één verslag per zitting lopen.

