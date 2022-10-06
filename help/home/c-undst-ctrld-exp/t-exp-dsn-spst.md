---
description: Dit bestand fungeert niet alleen als werkblad, maar ook als overzicht van uw beslissingen over het experiment.
solution: Analytics
title: Werkblad Experimenteel ontwerp
uuid: bcb11e39-9cbd-400c-af30-4b1c85e7f218
exl-id: 554790ab-1182-4481-87b0-e768ea769ddf
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 0%

---

# Werkblad Experimenteel ontwerp{#experiment-design-spreadsheet}

{{eol}}

Dit bestand fungeert niet alleen als werkblad, maar ook als overzicht van uw beslissingen over het experiment.

Als u hulp nodig hebt bij het ontwerpen van uw experiment, kunt u het spreadsheet van het proefontwerp (standaard VS Controlled Experiment Design.xls genoemd) van Adobe gebruiken.

Het spreadsheet van het proefontwerp kan alleen nuttige statistische conclusies opleveren wanneer de betrokken meting wordt gedefinieerd als een percentage bezoekers dat aan bepaalde criteria voldoet. Dat wil zeggen dat het alleen nuttig is wanneer een op bezoekers gebaseerde metrische hypothese wordt getest.

**Uw experiment ontwerpen met behulp van het ontwerpbestand van het experiment**

1. Als u beheerderstoegang hebt tot uw web- of toepassingsservers, navigeert u naar de [!DNL Sensor] installatiemap op elke [!DNL Sensor] in uw webcluster. Als u geen beheerdersrechten hebt, neemt u contact op met uw Adobe-accountmanager om het bestand aan te vragen.
1. Open het bestand Design.xls met VS-gecontroleerde experimenten. (U kunt de naam van dit bestand desgewenst wijzigen.)

   Het spreadsheet op de volgende pagina is een voorbeeld van hoe u het spreadsheet zou voltooien wanneer het voorbereiden om de voorbeeldhypothese te testen die door deze gids wordt gebruikt.

   ![](assets/experimentdesigntop.png)

   ![](assets/experimentdesignmiddle.png)

   ![](assets/experimentdesignbottom.png)

1. Voer tekst of waarden in voor alle velden in blauw in dit bestand, die in de volgende tabel worden beschreven. De berekende velden worden gedefinieerd in de tweede tabel.

<table id="table_C343F7A4BF3D4E0E9A5E9739EC7C2E10"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> In dit veld... </th> 
   <th colname="col2" class="entry"> Opgeven </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Titel van experiment </td> 
   <td colname="col2"> Een beschrijvende naam voor uw experiment. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beschrijving van experiment </td> 
   <td colname="col2"> Een tekstuele beschrijving van het experiment. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrisch onderzoek </td> 
   <td colname="col2"> <p>De naam van de metrische waarde waarop het experiment is gebaseerd. </p> <p>Voorbeeld: Bezoekerconversie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrische definitie </td> 
   <td colname="col2"> <p>De definitie van de metrische waarde waarop het experiment is gebaseerd. </p> <p>Indeling: Bezoekers[X]/Bezoekers </p> <p>Voorbeeld: <span class="filepath"> Bezoekers[URI='conversionpage.asp']/Bezoekers</span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beoogde begintijd </td> 
   <td colname="col2"> De datum en het tijdstip waarop het experiment moet beginnen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beoogde eindtijd </td> 
   <td colname="col2"> De datum en het tijdstip waarop het experiment moet worden beëindigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toepasselijke selecties </td> 
   <td colname="col2"> (Optioneel) De naam van de dimensie en de elementenset of het bereik waarmee u de gegevensset verder wilt segmenteren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Experimentele URI's </td> 
   <td colname="col2"> De URI's die bij uw hypothese horen. U bepaalt huidige URIs voor de controlegroep en afwisselende URIs die u voor de testgroep(en) hebt gecreeerd of zult creëren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metriek verwacht voor toepassingsselecties </td> 
   <td colname="col2"> Kop voor de metrische waarden die u voor uw website verwacht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gemiddelde aantal bezoekers per dag </td> 
   <td colname="col2"> Het gemiddelde aantal bezoekers van uw website per dag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekerconversie </td> 
   <td colname="col2"> De gemiddelde conversiesnelheid voor bezoekers van uw website. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Experimenteer bepaalt of de metrische naam voor de testgroepen ... </td> 
   <td colname="col2"> Kop voor hoe de metrische waarden moeten worden vergeleken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Groter dan de waarde voor de Controlegroep? </td> 
   <td colname="col2"> Stel dit veld in op True als u wilt dat u kunt concluderen dat de metrische waarde van de testgroep tijdens het experiment is toegenomen. Stel dit veld in op Onwaar om het aantal bezoekers te verminderen dat nodig is om conclusies te trekken. Adobe adviseert dat u het aan Waar plaatst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kleiner dan de waarde voor de controlegroep? </td> 
   <td colname="col2"> Stel dit veld in op True als u wilt dat u kunt concluderen dat de metrische waarde van de testgroep tijdens het experiment is afgenomen. Adobe adviseert dat u het aan Waar plaatst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Op ten minste (detectieniveau) </td> 
   <td colname="col2"> Het percentage waardoor u metrisch voor de testgroep hoger of lager wilt zijn dan dat voor de controlegroep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Met een betrouwbaarheidsniveau van ten minste </td> 
   <td colname="col2"> Het gewenste betrouwbaarheidsniveau voor de testgroepwaarden. Het betrouwbaarheidsniveau bepaalt het aantal valse positieven om de waarschijnlijkheid te meten dat de verklaarde verwachting waar is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> en een energieniveau van </td> 
   <td colname="col2"> Het gewenste vermogensniveau voor de waarden van de testgroep. Het machtsniveau bepaalt het aantal valse negatieven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> % Bezoekers </td> 
   <td colname="col2"> Kop voor het percentage bezoekers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Testgroep </td> 
   <td colname="col2"> Percentage bezoekers dat u in de testgroep wilt opnemen. U kunt met dit getal afspelen totdat de waarde in het veld Totaal (gewoonlijk 100%) in de sectie Bezoekers gelijk is aan of groter is dan de waarde in het veld Minimaal vereiste bezoekers (Groepen testen en besturen), die beide in de volgende tabel worden beschreven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Controlegroep </td> 
   <td colname="col2"> Percentage bezoekers dat u wilt opnemen in de controlegroep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Overige ontwerpnotities </td> 
   <td colname="col2"> Alle notities die u wilt opslaan voor toekomstig gebruik. </td> 
  </tr> 
 </tbody> 
</table>

De overige velden worden berekend op basis van de waarden die u hebt ingevoerd en worden in de volgende tabel beschreven.

| Veld | Beschrijving |
|---|---|
| Metriek verwacht voor toepassingsselecties | Kop voor de metrische waarden die u voor uw website verwacht. |
| Verwachte bezoekers per periode | Dit veld wordt normaal gesproken automatisch berekend door de spreadsheet. Het gaat ervan uit dat de website op de meeste dagen veel meer nieuwe bezoekers ontvangt dan bezoekers terugstuurt. Als dit niet het geval is, moet de berekening van deze cel worden overschreven met het werkelijke aantal bezoekers dat tijdens het experiment wordt verwacht. |
| Berekende Z-score voor Type I-fout | De Z-score voor een fout-positief resultaat. Dit is een tussentijdse statistische berekening. |
| Z-score wordt berekend voor Type II-fout | De Z-score voor een fout-negatief resultaat. Dit is een tussentijdse statistische berekening. |
| Minimale bezoekers vereist (test+controlegroepen) | Het minimum aantal bezoekers dat nodig is voor uw experiment om te voldoen aan het opgegeven betrouwbaarheidsniveau, het vermogensniveau en de Z-score, uitgedrukt als een percentage van de waarde in het veld Verwachte bezoekers per periode. |
| Minimale bezoekers vereist (test+controlegroepen) | Het minimale aantal bezoekers dat nodig is voor uw experiment om te voldoen aan het opgegeven vertrouwensniveau, het vermogensniveau en de Z-score. Deze waarde moet kleiner zijn dan of gelijk zijn aan de waarde in het veld Totaal (gewoonlijk 100%) in de sectie Bezoekers. |
| Minimale proeftijd (dagen) | Het minimum aantal dagen dat u nodig hebt om uw experiment uit te voeren om te voldoen aan uw opgegeven betrouwbaarheidsniveau, vermogensniveau en Z-score. Voor dit berekende aantal gelden dezelfde onderwerpen als die welke in het veld Verwachte bezoekers per periode worden besproken. In het geval van een website met veel terugkerende bezoekers is het veld Minimum Experiment Time (Dagen) het verwachte aantal dagen dat nodig is om een aantal unieke bezoekers te zien dat gelijk is aan de waarde in het veld Minimum aantal bezoekers vereist. |
| Bezoekers | Kop voor de waarden van bezoekers. |
| Testgroep | Aantal bezoekers in de testgroep. |
| Controlegroep | Aantal bezoekers nodig in de controlegroep. |
| Totaal (gewoonlijk 100%) | Het totale aantal bezoekers dat nodig is voor het experiment. Deze waarde moet gelijk zijn aan of groter zijn dan de waarde in het veld Minimum aantal vereiste bezoekers (groepen voor test en besturing). |
| Nauwkeurigheid testgroep (op het niveau van het Doelvertrouwen) | Percentage dat aangeeft dat er een kans is dat het opgegeven betrouwbaarheidsniveau gelijk is aan dat de gemeten waarde van de voor de testgroep berekende meetwaarde binnen dit percentage van de werkelijke waarde ligt. |
| De Nauwkeurigheid van de Groep van de controle (op het Niveau van het Vertrouwen van het Doel) | Het percentage erop wijst dat er een kans gelijk aan het gespecificeerde betrouwbaarheidsniveau is dat de gemeten waarde van metrisch die voor de controlegroep wordt berekend binnen dit percentage van zijn ware waarde zal zijn. |
| Z-score (bij doelnauwkeurigheid) | Het aantal standaardafwijkingen dat een bepaalde waarde oplevert, komt overeen met het testgemiddelde. |
| Werkelijk betrouwbaarheidsniveau (bij doelinterval) | Het betrouwbaarheidsniveau dat voor het experiment is bereikt. Het betrouwbaarheidsniveau meet de waarschijnlijkheid dat de vermelde verwachting waar is. |
| Werkelijk interval (op het niveau van het Vertrouwen van het Doel) | Het betrouwbaarheidsinterval dat is bereikt voor het experiment, dat een geschat bereik van waarden biedt dat waarschijnlijk een onbekende populatieparameter zal omvatten. Dit bereik wordt berekend op basis van een bepaalde set samplegegevens. |

U moet de waarde in het Minimale Vereiste Bezoekers (Test+Control Groepen) gebied bekijken. . .

![](assets/Experiment_Design_Min_Visitors.png)

en vergelijk het met de waarde in het veld Totaal van het dialoogvenster [!DNL Visitors] kolom.

![](assets/Experiment_Design_Total_Visitors.png)

Uw experiment is alleen statistisch geldig als de waarde in het veld Totaal (gewoonlijk 100%) gelijk is aan of groter is dan de waarde in het veld Minimaal vereiste bezoekers (Groepen testen en besturen).

Gezien de geleverde input, toont het voorbeeldaantekenvel u dat 10.475 bezoekers aan dit experiment moeten deelnemen om het ingegane 95% betrouwbaarheidspercentage te bereiken (dat is het minimum gesuggereerde vertrouwen voor om het even welk gecontroleerd experiment, hoewel u dit aantal kunt verhogen). Het experiment zoals dat momenteel is opgezet, omvat 30.000 bezoekers, wat ruim boven het vereiste minimumaantal bezoekers ligt.

Als u het aantal dagen gelijk houdt, kunt u het betrouwbaarheidsniveau verhogen zolang het totale aantal bezoekers blijft voldoen aan of het vereiste minimum overschrijden.

1. Sla het bestand op voor uw records en gebruik vervolgens de gegevens uit het bestand om het experiment te configureren met behulp van het werkblad met de testconfiguratie. Voor meer informatie over dit spreadsheet, zie [Het vormen en het Opstellen van de Experimenteer](../../home/c-undst-ctrld-exp/t-crt-ctrld-exp/c-cnfg-dply-exp.md#concept-50f1de0242904698937bb72b3ea1b429).
