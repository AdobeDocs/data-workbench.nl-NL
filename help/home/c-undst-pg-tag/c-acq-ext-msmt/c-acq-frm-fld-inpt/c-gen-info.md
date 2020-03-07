---
description: De waarden ingegaan in een vorm in een Web-pagina kunnen in het vraagkoord van de later gevraagde pagina (op vormvoorlegging) door het gebruik van JavaScript worden verzameld en worden toegevoegd.
solution: Analytics
title: Algemene informatie
topic: Data workbench
uuid: 401816a5-1d95-48e6-bedf-ee2a5dbd2d50
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Algemene informatie{#general-information}

De waarden ingegaan in een vorm in een Web-pagina kunnen in het vraagkoord van de later gevraagde pagina (op vormvoorlegging) door het gebruik van JavaScript worden verzameld en worden toegevoegd.

Dit wordt getoond in het volgende voorbeeld. Omvat dit JavaScript na om het even welke manuscripten van de vormbevestiging die in uw HTML- pagina&#39;s worden gebruikt.

```
<html> 
<head> 
</head> 
<script language="JavaScript"> 
 
function AppendFormValues() 
{ 
 
for(var i = 0; i < document.formname.length; i++) 
{ 
var item = document.formname.elements[i]; 
var formitem = “v_”+i; 
var formvalue = item.value; 
formvalues += formitem + '=' + formvalue + '&'; 
} 
document.formname.action = document.formname.action + '?' + formvalues; 
 
} 
</script> 
<body> 
<form name="formname" action="thankyou.asp" method="POST" onSubmit="AppendFormValues();"> 
<input name="NAME" size="50" value=""></input>name<br/> 
<input name="CITY" size="50" value=""></input>city<br/> 
<input name="STATE" size="50" value=""></input>state<br/> 
<input name="ZIP" size="10" value=""></input>zip<br /> 
<input type="submit" name="submit" value="submit"/> 
</body> 
</html> 
```

Dit voorbeeld voegt de waarden ingegaan in de vorm door de browser gebruiker aan de verdere &quot;thankyou.asp&quot;pagina toe die in de waarde van de Actie van de VORM als volgt wordt vermeld:

```
http://www.myserver.com/thankyou.asp?v_1=John Smith&v_2=Los Angeles&v_3=California&v_4=90210
```

De volgende uitgebreide metingen zouden met dit verzoek worden verkregen naast de basismetingen die worden verzameld door [!DNL Sensor]:

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_1 | Waarde verbonden aan het de vormgebied van de NAAM | v_1=John Smith |
| v_2 | Waarde verbonden aan het de vormgebied van de CITY | v_2=Los Angeles |
| v_3 | Waarde verbonden aan het de vormgebied van de STAAT | v_3=Californië |
| v_4 | Waarde verbonden aan het de vormgebied van het PIT | v_4=90210 |

