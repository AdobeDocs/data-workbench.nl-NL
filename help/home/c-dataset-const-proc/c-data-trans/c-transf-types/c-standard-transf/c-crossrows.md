---
description: Net als andere transformaties wordt de CrossRows-transformatie toegepast op de gegevensrijen (logitems) in de logbronnen.
title: CrossRows
uuid: 5910c150-6bec-4d98-b116-9b382fd54d3c
exl-id: 321f986e-44a9-454c-9311-0ae37a11a088
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# CrossRows{#crossrows}

{{eol}}

Net als andere transformaties wordt de CrossRows-transformatie toegepast op de gegevensrijen (logitems) in de logbronnen.

Voor elke rij gegevens neemt de transformatie de waarde van het opgegeven invoerveld, voert een reeks verwerkingsstappen uit en registreert het resultaat in het uitvoerveld dat u opgeeft. Wanneer echter [!DNL CrossRows] de transformatie werkt op één rij van gegevens (deze rij wordt genoemd de outputrij), houdt het rekening dat de rij plus één of meerdere andere rijen van gegevens (deze rijen worden genoemd inputrijen) die met zelfde het volgen identiteitskaart worden geassocieerd. Voor een bepaalde id voor reeksspatiëring is de waarde van het uitvoerveld voor elke uitvoerrij daarom gebaseerd op de waarden van het invoerveld voor een of meer invoerrijen.

De transformatie biedt meerdere voorwaarden en beperkingen waarmee u de invoerrijen voor de transformatie kunt beperken. U kunt deze limieten uitgedrukt in termen van de voorwaarden van de gegevenswerkbankserver (zie [Voorwaarden](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md)), een bereik van invoerrijen ten opzichte van de uitvoerrij of een bereik van tijden ten opzichte van de tijd van de uitvoerrij. Voor die invoerrijen die aan de voorwaarden en beperkingen van de transformatie voldoen, kunt u een verrichting (zoals SUM) toepassen die de waarde van outputgebied bepaalt.

>[!NOTE]
>
>Om te werken, [!DNL CrossRows] voor transformatie moeten de gegevens in de tijd worden geordend en met de tracking-id in de brongegevens worden gegroepeerd. Daarom [!DNL CrossRows] werkt alleen wanneer deze zijn gedefinieerd in het dialoogvenster [!DNL Transformation.cfg] of in een [!DNL Transformation Dataset Include] bestand.

Let op het volgende terwijl u de beschrijvingen van de parameters in de volgende tabel bekijkt:

* De uitvoerrij is de gegevensrij waaraan de transformatie op een bepaald tijdpunt werkt.
* Invoerrijen zijn alle andere rijen met gegevens (voor, na of inclusief de uitvoerrij) waarvan de waarden van het invoerveld fungeren als invoer voor de transformatie. Invoerrijen zijn onderworpen aan de parameters Invoervoorwaarde, Toets, Begin rij, Einde rij, Begin tijd en Einde tijd.

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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> Hiermee wordt de uitvoer van de transformatie beperkt tot bepaalde logitems. Als voor een bepaald logbestandvermelding niet aan de voorwaarde wordt voldaan, blijft het veld in de parameter Uitvoer ongewijzigd. De invoer kan nog worden gebruikt om andere logboekingangen te beïnvloeden. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> De naam van het veld in de invoerrij dat als invoer moet worden gebruikt. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoervoorwaarde </td> 
   <td colname="col2"> Accepteert invoer voor de transformatie van alleen bepaalde invoerrijen. Als voor een bepaalde invoerrij niet aan de invoervoorwaarde wordt voldaan, wordt het invoerveld van die rij genegeerd en heeft dit geen invloed op andere uitvoerrijen. Het uitvoerveld van die rij wordt echter nog steeds gewijzigd volgens de opgegeven voorwaarde. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sleutel </td> 
   <td colname="col2"> <p>Optioneel. De naam van het veld dat als sleutel moet worden gebruikt. </p> <p> Als een sleutel wordt gespecificeerd, zijn de inputrijen voor een bepaalde outputrij beperkt tot het aangrenzende blok van rijen die de zelfde Zeer belangrijke waarde zoals de outputrij hebben. Deze beperking komt bovenop alle andere beperkingen die door andere parameters van de <span class="wintitle"> CrossRows</span> transformatie. </p> <p> Als u bijvoorbeeld met webgegevens werkt en het veld x-session-key (met een unieke waarde voor elke sessie) als sleutel gebruikt, zijn de invoerrijen voor de transformatie beperkt tot die rijen met dezelfde x-session-key als de uitvoerrij. Daarom houdt u alleen rekening met invoerrijen die paginaweergaven vertegenwoordigen die voorkomen tijdens dezelfde sessie als de uitvoerrij. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bewerking </td> 
   <td colname="col2"> <p>Een bewerking die voor elke uitvoerrij wordt toegepast op alle invoerrijen die voldoen aan alle voorwaarden die zijn gedefinieerd door de parameters Invoervoorwaarde, Toets, Begin rij, Einde rij, Begin tijd en Einde tijd om een uitvoer te produceren: 
     <ul id="ul_C01CCF73A9544BCFB7B1105042FEF2DD"> 
      <li id="li_2D1A192970904499AB9F4431D51106D7"> ALL neemt alle waarden van het inputgebied van de inputrijen en output hen als vector. </li> 
      <li id="li_B8863724AD924DE5BDBC987143548257"> SUM interpreteert de waarden van het inputgebied van de inputrijen als aantallen en sommen hen. </li> 
      <li id="li_BF930069DCEA4E0B80893C3C06CAE100"> EERSTE RIJ geeft als uitvoer de waarde van het invoerveld vanaf de eerste invoerrij. </li> 
      <li id="li_04B9E2D88C0847E28101FC830C18D8E2"> De LAATSTE RIJ geeft de waarde van het invoerveld uit de laatste invoerrij. </li> 
     </ul> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het uitvoerveld. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin/einde rij </td> 
   <td colname="col2"> <p>Optioneel. Hiermee geeft u een bereik van invoerrijen op ten opzichte van de uitvoerrij. Met de waarde bij Begin rij van 0 worden bijvoorbeeld alle rijen vóór de uitvoerrij uitgesloten. Een rij begint waarde "1" sluit ook de uitvoerrij uit. Veelvoorkomende bereiken zijn: 
     <ul id="ul_B030F32A5146430BA50DD4FAB4A527B0"> 
      <li id="li_30DFB8C0265349C295943A1CB8077B86"> Begin 0: Deze rij en alle volgende rijen. </li> 
      <li id="li_9090C2E94E394351867BC5B78F27B41C"> Begin 1: Alle volgende rijen. </li> 
      <li id="li_F870DC913E3F45BA94EE2EC04D344DE0"> Einde 0: Deze rij en alle vorige rijen. </li> 
      <li id="li_B8A576E419744D84AB1298E5155B583E"> Einde -1: Alle vorige rijen. </li> 
      <li id="li_CD2307A262D34542A2860FF07005CAD7"> Begin -1, eind -1: De vorige rij. </li> 
      <li id="li_6BF30B7BB7CC40A68B2332A3C11DD3B5"> Begin 1, Einde 1: De volgende rij. </li> 
     </ul> </p> </td> 
   <td colname="col3"> Alle rijen </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Einde tijd beginnen/tijd </td> 
   <td colname="col2"> <p>Optioneel. Hiermee geeft u een tijdsbereik op ten opzichte van de tijd van de uitvoerrij. Een time-einde van 30 minuten omvat bijvoorbeeld alle rijen die binnen 30 minuten na de uitvoerrij worden uitgevoerd. Een tijd begint van -30 minuten omvat alle rijen die binnen 30 minuten vóór de outputrij plaatsvinden. </p> <p> Beschikbare tijdeenheden zijn dagen, weken, uren, minuten, ms (milliseconden), tikken (100 nanoseconden) en ns (nanoseconden). </p> </td> 
   <td colname="col3"> Alle malen </td> 
  </tr> 
 </tbody> 
</table>

De [!DNL CrossRows] transformatie in dit voorbeeld wordt toegepast op rijen webgegevens om voor elke pagina de tijd van de volgende paginaweergave te zoeken. Omdat we weten dat [!DNL CrossRows] alleen wordt toegepast tijdens de transformatiefase van het constructieproces van de gegevensset, worden de rijen met gegevens geordend door de bezoeker (elke bezoeker heeft een unieke tracking-id) en de tijd.

Het invoerveld, x-timestamp, wordt alleen gebruikt voor invoerrijen waarin het veld voor de x-is-paginaweergave is ingevuld (de rij met gegevens wordt aangeduid als een paginaweergave). Het veld x-session-key (met een unieke waarde voor elke sessie) wordt opgegeven voor de parameter Key. Daarom zijn de inputrijen (logboekingangen) voor de transformatie beperkt tot het aangrenzende blok van rijen die de zelfde waarde van x-session-sleutel zoals de outputrij hebben. Met andere woorden, om voor de transformatie in aanmerking te komen, moet een inputrij een paginamening vertegenwoordigen die tijdens de zelfde zitting zoals de paginamening in de outputrij voorkomt. De eerste rijverrichting neemt de waarde van het outputgebied van de eerste inputrij die aan [!DNL Input] Voorwaarde en met dezelfde sleutelwaarde voor de x-sessie als de uitvoerrij.

![](assets/cfg_TransformationType_CrossRows.png)

[!DNL CrossRows] wordt uitgevoerd in een hoeveelheid tijd die evenredig is aan de grootte van de invoer plus de grootte van de uitvoer. Dit betekent dat voor bewerkingen SUM, EERSTE RIJ en LAATSTE RIJ, deze niet minder efficiënt is dan andere transformaties. Voor ALLES, is de situatie complexer omdat het mogelijk is te vormen [!DNL CrossRows] om een hoeveelheid gegevens voor elke rij gegevens (logboekingang) uit te voeren die aan het totale aantal rijen (logboekingangen) voor een bepaalde het volgen identiteitskaart evenredig is.
