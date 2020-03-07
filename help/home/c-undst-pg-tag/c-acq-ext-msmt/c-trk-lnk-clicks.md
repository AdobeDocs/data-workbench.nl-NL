---
description: De stappen die worden gebruikt om de inzameling van de klikken van de Verbinding door het gebruik van de Markering van de Pagina van de Verwijzing te vergemakkelijken.
solution: Analytics
title: Het volgen van de klikken van de Verbinding
topic: Data workbench
uuid: e4c492d2-9c90-4ed7-b997-6c50bdf98f93
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het volgen van de klikken van de Verbinding{#tracking-link-clicks}

De stappen die worden gebruikt om de inzameling van de klikken van de Verbinding door het gebruik van de Markering van de Pagina van de Verwijzing te vergemakkelijken.

Door de plaatsing van [!DNL Reference Page Tag], is het mogelijk om meetgegevens te verzamelen die de verbindingen (of href waarden) aanduiden die de bezoekers terwijl het bezoeken van bepaalde pagina&#39;s klikken. Typisch, impliceert deze inzameling niet de implementatie van extra verbindingsherkenningstekens in uw HTML- pagina&#39;s.

Om inzameling van de Klikken van de Verbinding door het gebruik van te vergemakkelijken, voltooi de volgende stappen: [!DNL Reference Page Tag]

1. Kopieer de volgende code in het bestaande dossier genoemd [!DNL zig.js]:

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

1. Creeer of plaats 1 pixel door 1 pixelbeelddossier genoemd in een folder huidig op uw Webserver. [!DNL zag2.gif]
1. Wijzig de [!DNL lc.src] variabele om het aangewezen domein van uw website van verwijzingen te voorzien waarvan het [!DNL zag2.gif]dossier van verwijzingen wordt voorzien.

1. Verzeker aangewezen geheim voorgeheugen-controle de kopballen voor de [!DNL zag.gif] en [!DNL zig.js] dossiers worden gevestigd.

1. Binnen de HTML- dossiers u de waarden van de verbindingsklik van wilt verzamelen, [!DNL Reference Page Tag Execution Call] moet worden gewijzigd om de [!DNL Page Tag Execution Script] te informeren verbinding klikt voor die pagina te vangen. Om dit te doen, verander de vlc veranderlijke waarde in &quot;1&quot;zoals benadrukt in het volgende codevoorbeeld:

```
<!-- BEGIN REFERENCE PAGE TAG--> 
<script language="javascript"> 
var vlc = "1" //Capture Link Click  1=TRUE, 0=FALSE 
var vfc = "0"; //Capture Form Field Click  1=TRUE, 0=FALSE 
var v = {}; 
</script> 
 
<script language="javascript" src=”http://www.myserver.com/path/to/zig.js" type="text/javascript"></script> 
 
<noscript> 
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
</noscript> 
 
<!-- END REFERENCE PAGE TAG-->
```

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_ln= | Waarde die de Campagne van de Impressie aanduidt | v_ln=&quot;Ongeveer%20Us&quot; |

