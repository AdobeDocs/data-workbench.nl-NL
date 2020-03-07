---
description: Dit dossier functioneert niet alleen als aantekenvel maar ook als verslag van uw besluiten over het experiment.
solution: Insight,Analytics
title: Experimentele ontwerpspreadsheet
topic: Data workbench
uuid: bcb11e39-9cbd-400c-af30-4b1c85e7f218
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Experimentele ontwerpspreadsheet{#experiment-design-spreadsheet}

Dit dossier functioneert niet alleen als aantekenvel maar ook als verslag van uw besluiten over het experiment.

Als u hulp nodig hebt die uw experiment ontwerpt, kunt u de spreadsheet van het experimentele ontwerp (genoemd VS Controlled Experiment Design.xls door gebrek) gebruiken die door Adobe wordt verstrekt.

De spreadsheet van het experimentele ontwerp kan slechts nuttige statistische gevolgtrekkingen opleveren wanneer de metrische in kwestie wordt gedefinieerd als een percentage bezoekers dat aan bepaalde criteria voldoet. Dat wil zeggen, het is pas nuttig wanneer een op bezoekers gebaseerde metrische hypothese wordt getest.

**Om uw experiment te ontwerpen met behulp van het ontwerpdossier van het experiment**

1. Als u beheerderstoegang tot uw Web of toepassingsservers hebt, navigeer aan de [!DNL Sensor] installatiemap op om het even welke [!DNL Sensor] machine in uw Webcluster. Als u geen beheerderstoegang hebt, contacteer uw de rekeningsmanager van Adobe om het dossier te verzoeken.
1. Open het VS Gecontroleerde Experiment Design.xls- dossier. (U kunt dit dossier anders noemen indien gewenst.)

   De spreadsheet op de volgende pagina is een voorbeeld van hoe u de spreadsheet zou voltooien wanneer het voorbereidingen treffen om de voorbeeldhypothese te testen die door deze gids wordt gebruikt.

   ![](assets/experimentdesigntop.png)

   ![](assets/experimentdesignmiddle.png)

   ![](assets/experimentdesignbottom.png)

1. Ga tekst of waarden voor alle gebieden in blauw in dit dossier in, die in de volgende lijst worden beschreven. De berekende gebieden worden bepaald in de tweede lijst.

<table id="table_C343F7A4BF3D4E0E9A5E9739EC7C2E10"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Op dit gebied... </th> 
   <th colname="col2" class="entry"> Specificeren </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Titel experiment </td> 
   <td colname="col2"> Een beschrijvende naam voor je experiment. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beschrijving van het experiment </td> 
   <td colname="col2"> Een tekstuele beschrijving van het experiment. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrisch onderzoek </td> 
   <td colname="col2"> <p>De naam van metrisch waarop het experiment wordt gebaseerd. </p> <p>Voorbeeld: Bezoekersconversie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrische definitie </td> 
   <td colname="col2"> <p>De definitie van metrisch waarop het experiment is gebaseerd. </p> <p>Formaat: Bezoekers[X]/Bezoekers </p> <p>Voorbeeld: <span class="filepath"> Bezoekers[URI='conversionpage.asp']/Bezoekers</span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beoogde begintijd </td> 
   <td colname="col2"> De datum en het tijdstip waarop u het experiment wilt starten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geplande eindtijd </td> 
   <td colname="col2"> De datum en het tijdstip waarop je het experiment wilt beëindigen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toepasselijke selecties </td> 
   <td colname="col2"> (Facultatief) de de afmetingsnaam en elementenreeks of waaier waardoor u de dataset verder wilt segmenteren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Experimentele URIs </td> 
   <td colname="col2"> De URIs betrokken bij uw hypothese. U bepaalt de huidige URIs voor de controlegroep en de afwisselende URIs die u hebt gecreeerd of voor de testgroep(en) zult creëren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verwachte Metriek voor de Selecties van de Toepassing </td> 
   <td colname="col2"> Rubriek voor de metrische waarden die u voor uw website verwacht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gemiddelde bezoekers per dag </td> 
   <td colname="col2"> Het gemiddelde aantal bezoekers aan uw website per dag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekersconversie </td> 
   <td colname="col2"> De gemiddelde omrekeningskoers voor bezoekers voor uw website. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Het experiment zal bepalen als de metrische naam voor de Groepen van de Test... is </td> 
   <td colname="col2"> Rubriek voor hoe de metrische waarden zouden moeten worden vergeleken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Groter dan de waarde voor de controlegroep? </td> 
   <td colname="col2"> Plaats dit gebied aan Waar als u de capaciteit wilt om te concluderen dat metrisch van de testgroep tijdens het experiment steeg. Plaats dit gebied aan Vals om het aantal bezoekers te verminderen nodig om conclusies te trekken. Adobe adviseert dat u het aan Waar plaatst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Minder dan de waarde voor de controlegroep? </td> 
   <td colname="col2"> Plaats dit gebied aan Waar als u de capaciteit wilt om te concluderen dat metrisch van de testgroep tijdens het experiment daalde. Adobe adviseert dat u het aan Waar plaatst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ten minste (detectieniveau) </td> 
   <td colname="col2"> Het percentage waardoor u metrisch voor de testgroep hoger of lager wilt zijn dan dat voor de controlegroep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Met een betrouwbaarheidsniveau van ten minste </td> 
   <td colname="col2"> Het gewenste betrouwbaarheidsniveau voor de waarden van de testgroep. Het vertrouwensniveau bepaalt het aantal valse positieven om de waarschijnlijkheid te meten dat de verklaarde verwachting waar is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> en een energieniveau van </td> 
   <td colname="col2"> Het gewenste vermogensniveau voor de waarden van de testgroep. Het machtsniveau bepaalt het aantal valse negatieven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> % bezoekers </td> 
   <td colname="col2"> Rubriek voor de percenten bezoekerswaarden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Testgroep </td> 
   <td colname="col2"> Percentage bezoekers die je wilt opnemen in de testgroep. U kunt met dit aantal spelen tot de waarde in het Totale (gewoonlijk 100%) gebied in de sectie van Bezoekers aan of groter is dan de waarde op het MinimumVereiste gebied van Bezoekers (Test+Control Groepen), allebei die in de volgende lijst worden beschreven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Controlegroep </td> 
   <td colname="col2"> Percentage bezoekers u in de controlegroep wilt omvatten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Andere ontwerpnotities </td> 
   <td colname="col2"> Om het even welke nota's die u voor toekomstige verwijzing wilt bewaren. </td> 
  </tr> 
 </tbody> 
</table>

De resterende gebieden worden berekend gebaseerd op de waarden die u inging en in de volgende lijst beschreven.

| Veld | Beschrijving |
|---|---|
| Verwachte Metriek voor de Selecties van de Toepassing | Rubriek voor de metrische waarden die u voor uw website verwacht. |
| Verwachte bezoekers per periode | Dit veld wordt normaal gesproken automatisch berekend aan de hand van de spreadsheet. Het baseert zich op de veronderstelling dat de website op de meeste dagen veel meer nieuwe bezoekers ontvangt dan bezoekers teruggeeft. Als dit niet het geval is, moet de berekening van deze cel worden overschreven met het werkelijke aantal bezoekers dat tijdens het experiment wordt verwacht. |
| Berekende Z-score voor type I-fout | De score van Z voor een vals positief resultaat. Dit is een tussentijdse statistische berekening. |
| Berekende Z-score voor type II-fout | De score van Z voor een vals negatief resultaat. Dit is een tussentijdse statistische berekening. |
| Minimale bezoekers vereist (test+controlegroepen) | Minimumaantal bezoekers nodig in uw experiment om uw gespecificeerd betrouwbaarheidsniveau, machtsniveau, en de score van Z te ontmoeten, die als percentage van de waarde in de Verwachte Bezoekers per gebied van de Periode wordt uitgedrukt. |
| Minimale bezoekers vereist (test+controlegroepen) | Minimumaantal bezoekers nodig in uw experiment om uw gespecificeerd betrouwbaarheidsniveau, machtsniveau, en de score van Z te ontmoeten. Deze waarde moet minder dan of gelijk aan de waarde in het Totale (gewoonlijk 100%) gebied in de sectie van Bezoekers zijn. |
| Minimale experimenteertijd (dagen) | Het minimum aantal dagen u moet uw experiment in werking stellen om uw gespecificeerd betrouwbaarheidsniveau, machtsniveau, en de score van Z te ontmoeten. Dit berekende aantal is onderworpen aan de zelfde kwesties zoals besproken in de Verwachte Bezoekers per het gebied van de Periode. In het geval van een website met veel bezoekers die terugkeren, is het veld Minimale tijd van het experiment (dagen) het verwachte aantal dagen dat nodig is om een aantal unieke bezoekers te zien dat gelijk is aan de waarde in het veld Minimale bezoekers Vereiste. |
| Bezoekers | Rubriek voor de bezoekerswaarden. |
| Testgroep | Aantal bezoekers nodig in de testgroep. |
| Controlegroep | Aantal bezoekers nodig in de controlegroep. |
| Totaal (gewoonlijk 100%) | Totaal aantal bezoekers nodig voor het experiment. Deze waarde moet aan of groter zijn dan de waarde op het MinimumVereiste gebied van Bezoekers (Test+Control Groepen). |
| Nauwkeurigheid van de testgroep (op het niveau van het vertrouwen van het Doel) | Het percentage erop wijst dat er een kans gelijk aan het gespecificeerde betrouwbaarheidsniveau is dat de gemeten waarde van metrisch berekend voor de testgroep binnen dit percentage van zijn ware waarde zal zijn. |
| Nauwkeurigheid van de controlegroep (op het niveau van het Vertrouwen van het Doel) | Het percentage erop wijst dat er een kans gelijk aan het gespecificeerde betrouwbaarheidsniveau is dat de gemeten waarde van metrisch die voor de controlegroep wordt berekend binnen dit percentage van zijn ware waarde zal zijn. |
| Z-score (bij doelnauwkeurigheid) | Aantal standaardafwijkingen een bepaalde waarde is van het testgemiddelde. |
| Werkelijk betrouwbaarheidsniveau (bij streefinterval) | Het voor het experiment bereikte betrouwbaarheidsniveau. Het betrouwbaarheidsniveau meet de waarschijnlijkheid dat de aangegeven verwachting waar is. |
| Werkelijk interval (op het niveau van het Doel Vertrouwen) | Het betrouwbaarheidsinterval dat is bereikt voor het experiment, dat een geschatte reeks waarden oplevert die waarschijnlijk een onbekende populatieparameter zal omvatten. Dit bereik wordt berekend aan de hand van een bepaalde reeks steekproefgegevens. |

U moet de waarde op het MinimumVereiste gebied van Bezoekers (Groepen Test+Control) bekijken. . .

![](assets/Experiment_Design_Min_Visitors.png)

en vergelijk het met de waarde in het Totale gebied in de [!DNL Visitors] kolom.

![](assets/Experiment_Design_Total_Visitors.png)

Om uw experiment statistisch geldig te zijn, moet de waarde in het Totale (gewoonlijk 100%) gebied aan of groter zijn dan de waarde op het MinimumVereiste gebied van Bezoekers (Test+Control Groepen).

Gezien de verstrekte input, wat het voorbeeldaantekenvel u toont is dat 10.475 bezoekers aan dit experiment moeten deelnemen om het ingegane 95% betrouwbaarheidspercentage (dat het minimum voorgestelde vertrouwen voor om het even welk gecontroleerd experiment is, hoewel u dit aantal kunt verhogen) te bereiken. Het experiment zoals dat momenteel is opgezet, omvat 30.000 bezoekers, wat ruim boven het vereiste minimumaantal bezoekers ligt.

Als u het aantal dagen gelijk houdt, kunt u het betrouwbaarheidsniveau verhogen zolang het totale aantal bezoekers blijft voldoen of het vereiste minimum overschrijdt.

1. Sparen het dossier voor uw verslagen en gebruik dan de informatie van het dossier om het experiment te vormen gebruikend de spreadsheet van de experimentele configuratie. Voor meer informatie over deze spreadsheet, zie het [Vormen van en het Opstellen van de Experiment](../../home/c-undst-ctrld-exp/t-crt-ctrld-exp/c-cnfg-dply-exp.md#concept-50f1de0242904698937bb72b3ea1b429).
