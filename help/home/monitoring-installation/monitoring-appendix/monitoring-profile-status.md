---
description: De volgende afmetingen zijn beschikbaar voor gebruik in het statusprofiel van het gegevenswerkbankprofiel.
title: Dimension in het statusprofiel van het profiel Data Workbench
uuid: bd84a3e5-d1ea-4768-9dac-62f5dfbad49a
exl-id: 57b3ff16-26db-4292-819b-f6cd8e024c2a
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# Dimension in het statusprofiel van het Profiel van de Data Workbench{#dimensions-in-the-data-workbench-profile-status-profile}

De volgende afmetingen zijn beschikbaar voor gebruik in het statusprofiel van het gegevenswerkbankprofiel.

<table id="table_DD143B4F15FF446DAD24BD2473B485B9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Blok</b> </td> 
   <td colname="col2"> Dit is het enige telbare in deze configuratie en bestaat als wortel voor alle dimensies. Een blok kan als een server worden beschouwd. Het veld x-trackingid wordt gebruikt. De blok-id is een hash van de servernaam plus de hostnaam. Er zal dus ongeveer één blok per server per profiel zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Vertraging minuten</b> </td> 
   <td colname="col2"> cs-uri-query(bi) wordt in het veld x-as-of-delay-minutes geplaatst en afgerond naar de dichtstbijzijnde minuut. Vanaf Vertragingsminuten is een numerieke dimensie die de laatste rij neemt van x-as-of-delay-minuten voor een blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Omgeving</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(c) wordt gebruikt voor de milieu-id. De laatste rij voor een blok wordt gebruikt als waarde voor de dimensie. Deze Eenvoudige Dimension zal het Milieu tonen waarin uw Servers lopen (op voorwaarde dat het behoorlijk wordt gevormd). <p>Dit kan in het insight_monitor_agent.cfg- dossier worden geplaatst </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle invoer MegaBytes per minuut</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(bj) wordt gebruikt voor deze dimensie. De laatste rij voor een blok wordt gebruikt als waarde voor de dimensie. Als de dataset Snelle Input deze Numerieke minieme waarde in zal tonen MB per waarbij het systeem gegevens invoert. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel MegaBytes samenvoegen per minuut</b> </td> 
   <td colname="col2">De waarde cs-uri-query(bk) wordt gebruikt voor deze dimensie. De laatste rij voor een blok wordt gebruikt als waarde voor de dimensie. Als de dataset Deze Numerieke waarde van de Fusie in Snelle is zal de MB per minuut tonen waarbij het systeem samenvoegt. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Veld GigaBytes</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(bg) wordt gebruikt voor deze dimensie. De waarde wordt gedeeld door 1000 en afgerond naar het dichtstbijzijnde gehele getal. Deze numerieke Dimension zal de hoeveelheid ruimte tonen de Gebieden in de dataset gebruiken. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Host</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(b) wordt gebruikt voor deze dimensie. De waarde van de eenvoudige dimensie is de Laatste Rij voor een Blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingel</b> </td> 
   <td colname="col2">x-last-pingel is x-unixtime verdelen door 10 (om numerieke groottebeperkingen aan te passen). Laatste pingelt is de Laatste Rij voor een bepaald Blok, en het vertegenwoordigt de laatste tijd de controleagent het programma opende de systeemgezondheid. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage voor logarittering</b> </td> 
   <td colname="col2">De waarde cs-uri-query(be) wordt gebruikt voor deze numerieke dimensie. Het is de Laatste Rij voor een bepaald Blok. Deze afmeting wordt gebruikt om het percentage logboeken te berekenen die worden gelezen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verwerkingsmodus-id</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(bb) wordt gebruikt voor deze eenvoudige Dimension. Het is de laatste rij voor een bepaald blok. De identiteitskaart van de Wijze van de verwerking staat één toe om te zien welke wijze van verwerking het systeem is (Snelle Input, Snelle Fusie, Echte Tijd). <p>Opmerking:  Deze dimensie wordt verborgen en vervolgens opnieuw blootgesteld aan vriendelijke waarden in de verwerkingsmodus voor afmetingen aan de clientzijde. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verwerking gestapeld</b> </td> 
   <td colname="col2"> Het veld met de opmaakfunctie voor x-verwerking wordt onder verschillende omstandigheden gemaakt om aan te geven of het profiel al dan niet wordt uitgevoerd. Het is een eenvoudige dimensie. <p>Opmerking:  Deze dimensie werkt het best wanneer er een groot aantal inputlogboeken zijn om onder DPUs eerlijk te verdelen. Als er bijvoorbeeld slechts één groot bestand per dag wordt geladen, kan de werkbank voor gegevens een uur of langer 'vastlopen', wat resulteert in een fout positief lezen van deze dimensie. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Profiel</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(ba) wordt gebruikt voor deze eenvoudige Dimension. Deze dimensie geeft de naam of namen weer van de profielen die momenteel worden gecontroleerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Bron verder achter</b> </td> 
   <td colname="col2"> De laatste rij van cs-uri-query(bl) wordt gekopieerd in het x-bron-verst-achter gebied. De eenvoudige Dimension gebruikt de Laatste Rij voor een bepaald Blok. Deze afmeting toont wanneer het laatste contact met een gegevensbron voorkwam. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Transformatiepercentage</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(bf) wordt gebruikt voor deze numerieke dimensie. Het is de Laatste Rij voor een bepaald Blok. Deze dimensie wordt gebruikt om het percentage van volledige gegevenstransformatie te berekenen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Dimension tijd</b> </td> 
   <td colname="col2"> Uur, Dag, Week, Maand, Uur van Dag, en Dag van Week zijn allen afgeleid uit het x-timestamp gebied. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Groep</b> </td> 
   <td colname="col2"> Het groeperen van woord dat u een andere manier geeft om de resulterende dataset te filtreren. In het bestand insight_monitor_agent.cfg instellen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Cijfers</b> </td> 
   <td colname="col2"> Hieronder ziet u een overzicht van de meetgegevens die zijn opgenomen in het controleprofiel van de gegevenswerkbank en de manier waarop deze zijn afgeleid. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Vanaf vertragingsminuten</b> </td> 
   <td colname="col2"> Deze metrische waarde is de som van de notulen van de Vertraging voor elk Blok, dan verdeeld door metrische Blokken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Vanaf vertragingsseconden</b> </td> 
   <td colname="col2"> Deze metrische waarde is de som van de seconden vanaf de vertraging voor elk blok, gedeeld door het totale aantal blokken. (Vanaf vertragingsseconden Dimension is niet buiten het vak geconfigureerd) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Blokken</b> </td> 
   <td colname="col2"> Som één voor elk Blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle invoer MB per minuut</b> </td> 
   <td colname="col2"> De som van Fast Input MegaBytes per minuut voor elk blok gedeeld door het aantal blokken wanneer Fast Input MegaBytes per minuut groter is dan nul. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel MB samenvoegen per minuut</b> </td> 
   <td colname="col2"> De som van Fast Merge MegaBytes per Minuut voor elk Blok gedeeld door het aantal Blokken wanneer Snelle Fusie MegaBytes per Minuut groter is dan nul. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Veld GigaBytes</b> </td> 
   <td colname="col2"> De som van velgigabytes voor elk blok gedeeld door de metrische waarde van Blokken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pagina</b> </td> 
   <td colname="col2"> Het tijdstip min de laatste pingstijd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingstijd</b> </td> 
   <td colname="col2"> De som van Laatste pingelt voor elk Blok gedeeld door Blokken, dan vermenigvuldigd met 10. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Log lezen</b> </td> 
   <td colname="col2"> Wanneer het percentage voor het lezen van het logbestand groter is dan nul, is het lezen van het logbestand de som van het percentage voor het lezen van het logbestand voor elk blok, gedeeld door de metrische waarde van de blokken, die allemaal wordt gedeeld door 10. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verwerking gestapeld</b> </td> 
   <td colname="col2"> De som van de Verwerking Geroepen Dimension voor elk Blok, die door metrische Blokken wordt gedeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Transformatie</b> </td> 
   <td colname="col2"> De som van het Transformatiepercentage voor elk blok gedeeld door de metrische Blokken, wanneer het Transformatiepercentage groter is dan nul, allen gedeeld door 10. </td> 
  </tr> 
 </tbody> 
</table>
