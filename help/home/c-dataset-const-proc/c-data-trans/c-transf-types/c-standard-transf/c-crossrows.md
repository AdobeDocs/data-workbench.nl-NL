---
description: Als andere transformaties, wordt de transformatie CrossRows toegepast op de rijen van gegevens (logboekingangen) in uw logboekbronnen.
solution: Analytics
title: Kruisrijen
topic: Data workbench
uuid: 5910c150-6bec-4d98-b116-9b382fd54d3c
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Kruisrijen{#crossrows}

Als andere transformaties, wordt de transformatie CrossRows toegepast op de rijen van gegevens (logboekingangen) in uw logboekbronnen.

Voor elke rij van gegevens, neemt de transformatie de waarde van het gespecificeerde inputgebied, voert een reeks verwerkingsstappen uit, en registreert het resultaat op het outputgebied dat u specificeert. Nochtans, wanneer de [!DNL CrossRows] transformatie op één rij van gegevens werkt (deze rij wordt genoemd de outputrij), houdt het rekening met die rij plus één of meerdere andere rijen van gegevens (deze rijen worden genoemd inputrijen) die met zelfde volgende identiteitskaart worden geassocieerd. Daarom voor een bepaalde volgende identiteitskaart, is de waarde van het outputgebied voor elke outputrij gebaseerd op de waarden van het inputgebied voor één of meerdere inputrijen.

De transformatie verstrekt veelvoudige voorwaarden en beperkingen die u toelaten om de inputrijen voor de transformatie te beperken. U kunt deze grenzen in termen van de voorwaarden van de server van de gegevenswerkbank (zie [Voorwaarden](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md)), een waaier van inputrijen met betrekking tot de outputrij, of een waaier van tijden met betrekking tot de tijd van de outputrij uitdrukken. Voor die inputrijen die aan de voorwaarden en de beperkingen van de transformatie voldoen, kunt u een verrichting (zoals SUM) toepassen die de waarde van outputgebied bepaalt.

>[!NOTE]
>
>Om te werken, vereist de [!DNL CrossRows] transformatie dat het gegeven in tijd wordt bevolen en door volgende identiteitskaart in uw brongegevens gegroepeerd. Daarom werkt het [!DNL CrossRows] slechts wanneer bepaald in het [!DNL Transformation.cfg] dossier of in een [!DNL Transformation Dataset Include] dossier.

Aangezien u de beschrijvingen van de parameters in de volgende lijst herziet, herinner het volgende:

* De outputrij is de rij van gegevens waaraan de transformatie op een bepaald punt in tijd werkt.
* De rijen van de input zijn alle andere rijen van gegevens (vóór, na, of met inbegrip van de outputrij) de waarvan waarden van het inputgebied als input aan de transformatie dienen. De rijen van de input zijn onderworpen aan de Voorwaarde van de Input, de Sleutel, het Begin van de Rij, het Eind van de Rij, het Begin van de Tijd, en de parameters van het Eind van de Tijd.

<table id="table_152851484AFF4C50AF736DC62FAA43E3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> Beperkt de output van de transformatie tot bepaalde logboekingangen. Als de voorwaarde niet aan voor een bepaalde logboekingang wordt voldaan, wordt het gebied in de parameter van de Output verlaten onveranderd. De input kan nog worden gebruikt om andere logboekingangen te beïnvloeden. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> De naam van het gebied van de inputrij aan gebruik als input. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoerconditie </td> 
   <td colname="col2"> Accepteert input voor de transformatie van slechts bepaalde inputrijen. Als de Voorwaarde van de Input niet met voor een bepaalde inputrij wordt voldaan, wordt het inputgebied van die rij genegeerd en beïnvloedt andere outputrijen niet. Nochtans, wordt het outputgebied van die rij nog gewijzigd per de gespecificeerde Voorwaarde. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sleutel </td> 
   <td colname="col2"> <p>Optioneel. De naam van het gebied aan gebruik als sleutel. </p> <p> Als een sleutel wordt gespecificeerd, zijn de inputrijen voor een bepaalde outputrij beperkt tot het aangrenzende blok van rijen die de zelfde Belangrijkste waarde hebben zoals de outputrij. Deze beperking is naast alle andere beperkingen die op de inputrijen door andere parameters van de transformatie van <span class="wintitle"> Rijen</span> worden geplaatst. </p> <p> Bijvoorbeeld, als u met Webgegevens werkt en u de gebied x-zitting-sleutel (die een unieke waarde voor elke zitting heeft) de sleutel maakt, dan zijn de inputrijen voor de transformatie beperkt tot die rijen die de zelfde x-zitting-zeer belangrijke waarde hebben zoals de outputrij. Daarom overweegt u slechts die inputrijen die paginameningen vertegenwoordigen die tijdens de zelfde zitting voorkomen zoals de outputrij. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Exploitatie </td> 
   <td colname="col2"> <p>Een verrichting die, voor elke outputrij, wordt toegepast op alle inputrijen die aan alle voorwaarden voldoen die door de Voorwaarde van de Input, de Sleutel, het Begin van de Rij, het Eind van de Rij, het Begin van de Tijd, en de parameters van het Eind van de Tijd worden bepaald om een output te veroorzaken: 
     <ul id="ul_C01CCF73A9544BCFB7B1105042FEF2DD"> 
      <li id="li_2D1A192970904499AB9F4431D51106D7"> ALLEN neemt alle waarden van het inputgebied van de inputrijen en output hen als vector. </li> 
      <li id="li_B8863724AD924DE5BDBC987143548257"> SUM interpreteert de waarden van het inputgebied van de inputrijen als aantallen en vat hen samen. </li> 
      <li id="li_BF930069DCEA4E0B80893C3C06CAE100"> EERSTE ROW output de waarde van het inputgebied van de eerste inputrij. </li> 
      <li id="li_04B9E2D88C0847E28101FC830C18D8E2"> De LAATSTE output van de ROW de waarde van het inputgebied van de laatste inputrij. </li> 
     </ul> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het outputgebied. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin/einde rij </td> 
   <td colname="col2"> <p>Optioneel. Specificeert een waaier van inputrijen met betrekking tot de outputrij. Bijvoorbeeld, begint een Rij met waarde van "0"sluit alle rijen vóór de outputrij. Een rij begint waarde van "1"sluit eveneens de outputrij uit. De gemeenschappelijke waaiers omvatten: 
     <ul id="ul_B030F32A5146430BA50DD4FAB4A527B0"> 
      <li id="li_30DFB8C0265349C295943A1CB8077B86"> Begin 0: Deze rij en alle volgende. </li> 
      <li id="li_9090C2E94E394351867BC5B78F27B41C"> Begin 1: Alle volgende rijen. </li> 
      <li id="li_F870DC913E3F45BA94EE2EC04D344DE0"> Einde 0: Deze rij en alle vorige. </li> 
      <li id="li_B8A576E419744D84AB1298E5155B583E"> Einde -1: Alle vorige rijen. </li> 
      <li id="li_CD2307A262D34542A2860FF07005CAD7"> Begin -1, Eind -1: De vorige rij. </li> 
      <li id="li_6BF30B7BB7CC40A68B2332A3C11DD3B5"> Begin 1, Eind 1: De volgende rij. </li> 
     </ul> </p> </td> 
   <td colname="col3"> Alle rijen </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/tijdeinde </td> 
   <td colname="col2"> <p>Optioneel. Specificeert een waaier van tijden met betrekking tot de tijd van de outputrij. Bijvoorbeeld, omvat een Eind van de Tijd van 30 minuten alle rijen die binnen 30 minuten na de outputrij plaatsvinden. Een begin van de Tijd van -30 minuten omvat alle rijen die binnen 30 minuten vóór de outputrij plaatsvinden. </p> <p> De beschikbare tijdeenheden zijn dagen, weken, uren, notulen, ms (milliseconden), tikken (100 nanoseconden), en ns (nanoseconden). </p> </td> 
   <td colname="col3"> Alle keren </td> 
  </tr> 
 </tbody> 
</table>

De [!DNL CrossRows] transformatie in dit voorbeeld wordt toegepast op rijen van Webgegevens om voor elke paginamening de tijd van de volgende paginamening te vinden. Omdat wij weten dat slechts tijdens de transformatiefase van het proces van de datasetconstructie wordt toegepast, worden de rijen van gegevens bevolen door bezoeker (elke bezoeker heeft een unieke volgende identiteitskaart) en tijd. [!DNL CrossRows]

Het inputgebied, x-timestamp, wordt overwogen voor slechts die inputrijen waarin het x-is-pagina-mening gebied bevolkt is (erop wijzend de rij van gegevens vertegenwoordigt een paginamening). Het x-zitting-zeer belangrijke gebied (dat een unieke waarde voor elke zitting heeft) wordt gespecificeerd voor de Belangrijkste parameter. Daarom zijn de inputrijen (logboekingangen) voor de transformatie beperkt tot het aangrenzende blok van rijen die de zelfde waarde van x-zitting-sleutel hebben zoals de outputrij. Met andere woorden, om voor de transformatie te worden overwogen, moet een inputrij een paginamening vertegenwoordigen die tijdens de zelfde zitting voorkomt zoals de paginamening in de outputrij. De eerste rijverrichting neemt de waarde van het outputgebied van de eerste inputrij die aan de Voorwaarde voldoet en de zelfde x-zitting-zeer belangrijke waarde heeft zoals de outputrij. [!DNL Input]

![](assets/cfg_TransformationType_CrossRows.png)

[!DNL CrossRows] verricht in een hoeveelheid tijd die evenredig is aan de omvang van de inputs en de omvang van de outputs. Dit betekent dat voor verrichtingen SUM, EERSTE ROW, en LAATSTE ROW, het niet minder efficiënt is dan andere transformaties. Voor ALLE, is de situatie complexer omdat het mogelijk is om [!DNL CrossRows] aan output een hoeveelheid gegevens voor elke rij van gegevens (logboekingang) te vormen die aan het totale aantal rijen (logboekingangen) voor een bepaalde volgende identiteitskaart evenredig is.
