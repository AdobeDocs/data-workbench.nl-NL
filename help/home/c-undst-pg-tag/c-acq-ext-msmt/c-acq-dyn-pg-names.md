---
description: Voor sommige sites is het nodig om ingesloten objectverzoeken te gebruiken om informatie door te geven aan de webserver, zodat Sensor details kan verkrijgen over de pagina die daadwerkelijk is bediend en deze kan gebruiken voor rapportage en analyse.
title: Dynamische paginanamen ophalen
uuid: eaa35023-bbfa-4eb9-9ab7-3986187e5537
exl-id: cd94caf0-b0dc-46c1-8f59-3ebb2f703286
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Dynamische paginanamen ophalen{#acquiring-dynamic-page-names}

{{eol}}

Voor sommige sites is het nodig om ingesloten objectverzoeken te gebruiken om informatie door te geven aan de webserver, zodat Sensor details kan verkrijgen over de pagina die daadwerkelijk is bediend en deze kan gebruiken voor rapportage en analyse.

Dit kan nodig zijn als de URL van de pagina, zoals deze door de webserver wordt gezien, niet indicatief is voor de pagina-inhoud die aan de browser wordt weergegeven. Dit geval is vaak het gevolg van het gebruik van personalisatie- of dynamische contentbeheersystemen waarbij de werkelijke inhoud op een pagina direct wordt bepaald door de URL, het cookie, de gerelateerde gegevens en toepassingslogica.

De implementatie van een ingesloten object om aanvullende metingen te verzamelen, heeft minimale invloed op de algehele prestaties van de site. Adobe stelt voor dat u een JavaScript-bestand insluit als het object dat wordt gebruikt om de uitgebreide kenmerken te verzamelen. (Een JavaScript-bestand kan worden ingesloten zonder dat dit invloed kan hebben op de lay-out en presentatie van uw webpagina. Dit kan gebeuren als een ingesloten afbeelding wordt gebruikt.) Om de informatie nauwkeurig te vangen die binnen het ingebedde voorwerp wordt overgegaan, stelt Adobe ook voor dat een gemeenschappelijke naam wordt gebruikt. Voor naamgevingsdoeleinden verwijst Adobe naar dit object als [!DNL zig.js]. De [!DNL zig.js] bestand moet worden gemaakt in de juiste map op een webserver waarop [!DNL Sensor] is geïnstalleerd. Dit bestand moet bestaan, zodat het verzoek geen 404-foutcode retourneert. De inhoud van het bestand zelf is niet belangrijk. U moet een leeg bestand gebruiken met de naam [!DNL zig.js] om de hoeveelheid netwerkverkeer die als gevolg van het verzoek wordt veroorzaakt tot een minimum te beperken.

Voor [!DNL Sensor] om een bruikbare naam te verzamelen voor de pagina die eigenlijk werd gediend, moeten een paar lijnen code JavaScript aan de dynamische pagina&#39;s worden toegevoegd die u wilt volgen of waaraan u een unieke paginanaam wilt toevoegen. Deze code sluit een JavaScript-fragment in de pagina in. Hierdoor wordt een tertiair verzoek om een ingesloten object naar de webserver verzonden terwijl de pagina wordt geladen. Dat verzoek verzendt details over de specifieke pagina die aan de Webserver werd gediend. De naam van de pagina die daadwerkelijk is aangeboden, wordt als een variabele in de queryreeks van het ingesloten objectverzoek (in dit geval JavaScript) naar de webserver geretourneerd.

Over het algemeen zou de objecten aanvraag ingebed in elk dergelijk HTML pagina als het volgende moeten kijken:

```
<!-- BEGIN REFERENCE PAGE TAG-->
<script language="javascript">
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE
var v = {};
v["_pn"] = "Application Form";
</script>

<script language="javascript" src=”https://www.myserver.com/path/to/zig.js" type="text/javascript"></script>

<noscript>
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/>
</noscript>

<!-- END REFERENCE PAGE TAG-->
```

[!DNL Log=1] ervoor zorgt dat [!DNL Sensor] het verzoek ondanks [!DNL Sensor] filterregels voor inhoudstypen daarentegen, zoals het filteren uit JavaScript en afbeeldingsaanvragen voordat deze worden opgeslagen. De gedeclareerde v_pn-variabele geeft de naam aan van de pagina-inhoud die daadwerkelijk wordt aangeboden, zodat [!DNL Site] Hiermee kent u de naam van de pagina die de bezoeker daadwerkelijk heeft weergegeven. De waarde v_pn kan handmatig of met andere script- of toepassingscode worden ingesteld.

Nadat de waarde wordt verzameld, kunt u de server van de gegevenswerkbank vormen om de inhoud van de veranderlijke vraagkoord (name=value paar, bijvoorbeeld, v_pn=Application Vorm) te gebruiken die aan wordt toegevoegd [!DNL zag.gif] URI (bijvoorbeeld [!DNL https://www.mysite.com/pageserved.asp?v_pn=Application%20Form]), als een aanvulling op de [!DNL zag.gif] URI. Naast de basislijnmetingen die bij elke HTTP-aanvraag zijn verkregen, zou met deze aanvraag een uitgebreide meting worden verkregen.

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_pn= | Waarde gekoppeld aan de variabele v_pn-queryreeks | v_pn=Toepassingsformulier |
