---
description: Het vertrouwen legends helpt u om de waarschijnlijkheid te bepalen dat de aantallen u zien toe te schrijven aan toeval zijn en om de mogelijke afwijkingen in de gegevens te begrijpen.
title: Vertrouwelijke legenda
uuid: 2559ff7c-6060-4fee-b509-9ae0c3912016
exl-id: 9aab169a-98b8-4e71-b74d-28e385c5c424
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Vertrouwelijke legenda{#confidence-legends}

{{eol}}

Het vertrouwen legends helpt u om de waarschijnlijkheid te bepalen dat de aantallen u zien toe te schrijven aan toeval zijn en om de mogelijke afwijkingen in de gegevens te begrijpen.

Zelfs als u geen monsters neemt, kunt u de aantallen van een specifieke tijdspanne of een ondergroep aan andere tijdsperioden of ondergroepen niet met volledig vertrouwen extrapoleren. Met de vertrouwenslegenda kunt u nagaan hoe waarschijnlijk het is dat de getallen binnen een bepaald bereik vallen.

Als je echte data ziet als een groot experiment, dan impliceert de echte wereld nog steeds toeval, zelfs wanneer je met exacte getallen werkt. Als u bijvoorbeeld het aantal personen kent dat een transactie tussen 8.00 uur en 12.00 uur op een dinsdag heeft voltooid, betekent dat niet dat precies hetzelfde aantal dat op de volgende dinsdag zal doen.

De volgende vertrouwenslegenda toont vertrouwensdetails over metrisch Conversie, terwijl de volgende lijst meer informatie over wat elk gegevenspunt betekent.

![](assets/lgd_ConfidenceLegend.png)

<table id="table_387F22C7EF4E4DE9AD810D3D9204676F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Metrisch of Formule </p> </td> 
   <td colname="col2"> <p>De metrische naam of metrische uitdrukking waarvoor u vertrouwensinformatie wilt bekijken. Alle selecties die u in de werkruimte maakt, worden weerspiegeld in de legenda. In dit voorbeeld worden details over de metrische conversie weergegeven. </p> <p>Voor informatie over syntaxisregels voor het invoeren van een expressie raadpleegt u <a href="../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f"> Syntaxis zoektaal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gemeten waarde </p> </td> 
   <td colname="col2"> <p>De waarde van de werkelijk verzamelde gegevens. In dit voorbeeld is de conversiesnelheid voor de huidige selectie 2,3%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardafwijking </p> </td> 
   <td colname="col2"> <p>De standaardafwijking van de gemeten waarde. In dit voorbeeld is de standaardafwijking van de conversiesnelheid voor de huidige selectie 0,1%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De waarde "true" </p> </td> 
   <td colname="col2"> <p>De waarschijnlijkheid dat de gemeten waarde binnen het bereik valt dat voor elke waarschijnlijkheid wordt vermeld. In dit voorbeeld, als dit "real-world experiment"opnieuw en opnieuw worden herhaald, zou u 90% zeker kunnen zijn dat de Gemeten Waarde tussen 2.1% en 2.4% zou zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Bij het analyseren van de resultaten van berekeningen moet u rekening houden met de volgende punten:
>* De getallen zijn schattingen. Als u de zelfde berekeningen met een verschillende dataset herhaalde zou u een verschillend resultaat krijgen. Dit wordt willekeurige variatie genoemd.
>* Extrapolaties naar hogere waarschijnlijkheid hangen af van een veronderstelling van normaliteit die niet correct voor alle metriek is. Daarom zijn de waarden voor 99% waarschijnlijkheid minder betrouwbaar dan de waarden voor 90% waarschijnlijkheid.
>
>Als u meer nauwkeurige aantallen nodig hebt, zou u een deskundige in statistieken moeten raadplegen.

## Metriek of formules wijzigen {#section-7f09ff84c3514f26b78d29294e1f03d9}

* Klik in de vertrouwenslegenda op de knop **[!UICONTROL Metric or Formula]** veld en typ de gewenste metrische waarde of expressie. Zie voor syntaxisregels voor expressies [Syntaxis zoektaal](../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f).

## Exporteren naar Microsoft Excel {#section-f36e2db7273740b7af278f8a2b79d564}

Voor informatie over het exporteren van vensters raadpleegt u [Venstergegevens exporteren](../../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349).
