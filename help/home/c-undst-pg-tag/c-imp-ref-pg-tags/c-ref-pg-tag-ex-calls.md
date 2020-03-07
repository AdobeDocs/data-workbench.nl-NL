---
description: De vraag van de Uitvoering van de Markering van de Verwijzing wordt opgenomen in Web-pagina's waarvoor u meetgegevens wilt verzamelen.
solution: Analytics
title: Het toevoegen van de Vraag van de Markering van de Verwijzing de Uitvoering van de Vraag
topic: Data workbench
uuid: 8c682649-d1b1-40a6-a2b2-4ff5a92b732f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het toevoegen van de Vraag van de Markering van de Verwijzing de Uitvoering van de Vraag{#adding-reference-page-tag-execution-calls}

De vraag van de Uitvoering van de Markering van de Verwijzing wordt opgenomen in Web-pagina&#39;s waarvoor u meetgegevens wilt verzamelen.

Het zou in het lichaam van het HTML- document moeten worden omvat en kan binnen globaal worden geplaatst omvat footer indien van toepassing. Het [!DNL Reference Page Tag Execution Call] kan door uw team worden gewijzigd om extra informatie te verzamelen die tijdens vereisten zou kunnen worden geïdentificeerd die vergaderingen met het team van de Diensten van het Raadplegen van Adobe verzamelen.

Voer de volgende stappen uit om het verzamelen van gegevens door het gebruik van de [!DNL Reference Page Tag]gegevensbank te vergemakkelijken:

1. Kopieer de volgende code in uw het documentlichaam van HTML:

   ```
   <!--//BEGIN REFERENCE PAGE TAG--> 
   <script language="javascript"> 
   var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
   var v = {}; 
   </script> 
   
   <!--//MODIFIY PATH TO ZIG.JS--> 
   <script language="javascript" src="/path/to/zig.js" type="text/javascript"></script> 
   <!--//END REFERENCE PAGE TAG--> 
   
   <noscript> 
   <img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
   </noscript> 
   <!-- END REFERENCE PAGE TAG-->
   ```

1. Wijzig de weg aan de plaats van de [!DNL zig.js] en [!DNL zag.gif] dossiers. Bijvoorbeeld:

   ```
   //www.mysite.com/scripts/zig.js 
   //www.mysite.com/images/zag.gif 
   ```

Gelieve te zorgen ervoor dat de aangewezen HTTP caching-Controle kopballen op uw Webserver zijn geplaatst om ervoor te zorgen dat de [!DNL zig.js]en [!DNL zag.gif] - dossiers niet door browser in het voorgeheugen ondergebracht worden. U kunt de HTTP Cache-Controle kopbalinformatie plaatsen gebruikend één van twee methodes. De eerste methode is een HTTP- kopbal via de Webserver te plaatsen. De tweede methode moet een HTTP- kopbal voor elke specifieke pagina of ingebed voorwerp plaatsen gebruikend manuscript. Met de scripting methode, moet de Web-pagina gebruikend een programmeertaal zoals JSP of ASPIS gecreeerd zijn. De pagina wordt dan scripted zodat het de aangewezen kopbalinformatie verzendt. Deze methode gaat vergezeld van twee duidelijke nadelen: 1) alle pagina&#39;s moeten worden gecodeerd om de kopbal te verzenden, en 2) de pagina&#39;s kunnen geen statisch HTML zijn, dat één of ander effect op de prestaties van de Webserver heeft.

De websites die op Microsoft IIS lopen kunnen de aangewezen HTTP- kopbal door de Console van het Beheer van Microsoft toevoegen. De websites die van de Servers van het Web van Netscape worden gediend kunnen dit verwezenlijken door het [!DNL obj.conf] dossier binnen de de configuratiefolder van de plaats uit te geven. De Apache Server van het Web verstrekt webmasters de capaciteit om de kopballen van HTTP aan te passen gebruikend de inbegrepen mod_headers module waar AOLServer klantgericht door het gebruik van de modules van TCP wordt. Alvorens de de geheime voorgeheugen-Controle van HTTP- kopballen uit te voeren, zou u naar de documentatie specifiek voor uw platform van de Webserver moeten verwijzen.

In het algemeen, zou de HTTP- kopbal als volgt moeten worden gestructureerd:

```
Cache-Control: no-cache 
Pragma: no-cache 
Expires: -1
```

