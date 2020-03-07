---
description: Voor sommige plaatsen, is het noodzakelijk om ingebedde objecten verzoeken te gebruiken om informatie tot de Webserver over te gaan zodat de details over welke pagina eigenlijk werd gediend door Sensor kunnen worden verworven en voor rapportering en analyse worden gebruikt.
solution: Analytics
title: Dynamische paginanamen ophalen
topic: Data workbench
uuid: eaa35023-bbfa-4eb9-9ab7-3986187e5537
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Dynamische paginanamen ophalen{#acquiring-dynamic-page-names}

Voor sommige plaatsen, is het noodzakelijk om ingebedde objecten verzoeken te gebruiken om informatie tot de Webserver over te gaan zodat de details over welke pagina eigenlijk werd gediend door Sensor kunnen worden verworven en voor rapportering en analyse worden gebruikt.

Dit zou kunnen worden vereist als URL van de pagina, zoals die door de Webserver wordt gezien, niet indicatief van de paginainhoud is die aan browser wordt getoond. Deze kwestie vloeit vaak voort uit het gebruik van verpersoonlijking of dynamische systemen van het inhoudsbeheer waarin de daadwerkelijke inhoud die in een pagina wordt gediend bij de vlucht door URL, het koekje, de verwante gegevens en toepassingslogica wordt bepaald.

De implementatie van een ingebed voorwerp om extra metingen te verzamelen zou minimale invloed op uw algemene plaatsprestaties moeten hebben. Adobe stelt voor dat u een dossier JavaScript als voorwerp inbedt dat wordt gebruikt om de uitgebreide attributen te verzamelen. (Merk op dat een dossier JavaScript zonder enige potentiële invloed op de lay-out en de presentatie van uw Web-pagina kan worden ingebed aangezien het met het gebruik van een ingebed beeld kan resulteren.) Om de informatie nauwkeurig te vangen die binnen het ingebedde voorwerp wordt overgegaan, stelt Adobe ook voor dat een gemeenschappelijke naam wordt gebruikt. Voor noemende doeleinden, verwijst Adobe naar dit voorwerp zoals [!DNL zig.js]. Het [!DNL zig.js] dossier zou binnen de aangewezen folder op een Webserver moeten worden gecreeerd waarop geïnstalleerd [!DNL Sensor] is. Dit dossier moet bestaan zodat het verzoek geen 404 foutencode terugkeert. De inhoud van het dossier zelf is niet belangrijk. U zou een leeg dossier moeten gebruiken genoemd [!DNL zig.js] om de hoeveelheid netwerkverkeer te minimaliseren dat als gevolg van het verzoek wordt opgelopen.

Om een bruikbare naam voor de pagina [!DNL Sensor] te verzamelen die eigenlijk werd gediend, moeten een paar lijnen van code JavaScript aan de dynamische pagina&#39;s worden toegevoegd die u wilt volgen of waaraan u een unieke paginanaam wilt toevoegen. Deze code bedt een fragment van JavaScript in de pagina in, die veroorzaakt dat een tertiair ingebed objecten verzoek om aan de Webserver wordt gemaakt aangezien de pagina laadt. Dat verzoek verzendt details over de specifieke pagina die terug naar de Webserver werd gediend. De naam van de pagina die eigenlijk werd gediend wordt gedragen terug naar de Webserver als variabele in het vraagkoord van het ingebedde objecten (in dit geval JavaScript) verzoek.

In het algemeen, zou het objecten verzoek ingebed in elke dergelijke HTML- pagina als het volgende moeten kijken:

```
<!-- BEGIN REFERENCE PAGE TAG--> 
<script language="javascript"> 
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
var v = {}; 
v["_pn"] = "Application Form"; 
</script> 
 
<script language="javascript" src=”http://www.myserver.com/path/to/zig.js" type="text/javascript"></script> 
 
<noscript> 
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
</noscript> 
 
<!-- END REFERENCE PAGE TAG-->
```

[!DNL Log=1] zorgt ervoor dat [!DNL Sensor] het verzoek ondanks de [!DNL Sensor] inhoudstype het filtreren regels aan het tegenovergestelde, zoals het filtreren uit JavaScript en beeldverzoeken registreert alvorens zij worden opgeslagen. De opgegeven v_pn variabele identificeert de naam van de werkelijke pagina-inhoud die wordt gediend, zodat de naam van de pagina die de bezoeker daadwerkelijk heeft bekeken, [!DNL Site] bekend is. De v_pn waarde zou manueel of door andere manuscript of toepassingscode kunnen worden gevestigd.

Nadat de waarde wordt verzameld, kunt u de server van de gegevenswerkbank vormen om de inhoud van de variabele van het vraagkoord (name=value paar, bijvoorbeeld, v_pn=Application Vorm) te gebruiken die aan [!DNL zag.gif] URI (bijvoorbeeld, [!DNL http://www.mysite.com/pageserved.asp?v_pn=Application%20Form]) wordt toegevoegd, als verhoging van [!DNL zag.gif] URI. Naast de basislijnmetingen die met elk HTTP- verzoek worden verworven, zou een uitgebreide meting met dit verzoek worden verworven.

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_pn= | Waarde verbonden aan de v_pn variabele van het vraagkoord | v_pn=Application Form |

