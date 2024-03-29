---
description: Stappen die worden gebruikt om het verzamelen van Klik van de Verbinding door het gebruik van de Markering van de Pagina van de Verwijzing te vergemakkelijken.
title: Koppelingsklikken bijhouden
uuid: e4c492d2-9c90-4ed7-b997-6c50bdf98f93
exl-id: 0cb743e6-5c6e-4f80-bc77-83d1e706c92b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Koppelingsklikken bijhouden{#tracking-link-clicks}

{{eol}}

Stappen die worden gebruikt om het verzamelen van Klik van de Verbinding door het gebruik van de Markering van de Pagina van de Verwijzing te vergemakkelijken.

Door de inzet van de [!DNL Reference Page Tag], is het mogelijk om meetgegevens te verzamelen die de koppelingen (of href-waarden) aangeven waarop bezoekers tijdens het bezoeken van bepaalde pagina&#39;s klikken. Typisch, impliceert deze inzameling niet de implementatie van extra verbindingsherkenningstekens in uw HTML pagina&#39;s.

Om inzameling van de klik van de Verbinding door het gebruik van te vergemakkelijken [!DNL Reference Page Tag]Voer de volgende stappen uit:

1. Kopieer de volgende code naar het bestaande bestand genaamd [!DNL zig.js]:

   ```
   //REFERENCE LINK AND FORM CLICK PAGE TAG
   //INITIATE FUNCTIONS ONLOAD
   function addEvent(obj, evType, fn){
    if (obj.addEventListener){
      obj.addEventListener(evType, fn, false);
      return true;
    } else if (obj.attachEvent){
      var r = obj.attachEvent("on"+evType, fn);
      return r;
    } else {
      return false;
    }
   }
   addEvent(window, 'load', startCapture);
   addEvent(window, 'load', startCapture);
   function startCapture(){
   //TO CAPTURE LINK CLICKS
     if (vlc == "1"){captureLink();}
     //TO CAPTURE FORM FIELD CLICKS
     if (vfc == "1"){captureForm();}
   }
   //BEGIN LINK CAPTURE PAGE TAG
   function captureLink(){
     if (document.links[0]){
       if (document.links){
         var links = document.links, link, k=0;
         while(link=links[k++]) {
           link.onclick = captureLinkName;
    }
       }
     }
   }
   function captureLinkName() {
     var lc=new Image();
     this.parent = this.parentNode;
     lc.src='zag2.gif?linkname=' + escape(this.name) + "&cd=" + new Date().getTime();
   }
   //END LINK CAPTURE PAGE TAG
   //BEGIN FORM CLICK CAPTURE PAGE TAG
   function captureForm(){
     if (document.forms[0]) {
       if(document.forms){
    for(i=0; i<document.forms[0].elements.length; i++){
           var forms = document.forms[0].elements[i];
           forms.onfocus = captureFormName;
         }
       }
     }
   }
   function captureFormName() {
     var fc=new Image();
     fc.src='zag3.gif?fieldname=' + escape(this.name) + "&cd=" + new Date().getTime();
   }
   //END FORM CLICK CAPTURE PAGE TAG
   ```

1. Een afbeeldingsbestand van 1 pixel bij 1 pixel maken of plaatsen met de naam [!DNL zag2.gif] in een map op uw webserver.
1. De [!DNL lc.src] variabele die verwijst naar het juiste domein van uw website waaruit de [!DNL zag2.gif]Er wordt naar het bestand verwezen.

1. Zorg ervoor dat de juiste cachebeheerkoppen zijn ingesteld voor de [!DNL zag.gif] en [!DNL zig.js] bestanden.

1. In de HTML-bestanden waarvan u de koppelingsklikwaarden wilt verzamelen, kiest u [!DNL Reference Page Tag Execution Call] moet worden gewijzigd om de [!DNL Page Tag Execution Script] om verbinding te vangen klikt voor die pagina. Hiervoor wijzigt u de waarde van de variabele vlc in &quot;1&quot;, zoals in het volgende codevoorbeeld wordt gemarkeerd:

```
<!-- BEGIN REFERENCE PAGE TAG-->
<script language="javascript">
var vlc = "1" //Capture Link Click  1=TRUE, 0=FALSE
var vfc = "0"; //Capture Form Field Click  1=TRUE, 0=FALSE
var v = {};
</script>

<script language="javascript" src=”https://www.myserver.com/path/to/zig.js" type="text/javascript"></script>

<noscript>
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/>
</noscript>

<!-- END REFERENCE PAGE TAG-->
```

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_ln= | Waarde die de campagne voor onderdrukking aanduidt | v_ln=&quot;About%20Us&quot; |
