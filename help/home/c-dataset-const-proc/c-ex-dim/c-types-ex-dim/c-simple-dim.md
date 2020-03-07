---
description: Een eenvoudige dimensie heeft een één-aan-vele verhouding met zijn ouder telbare dimensie.
solution: Analytics
title: Eenvoudige afmetingen
topic: Data workbench
uuid: 3bca2354-02c4-4739-a7da-acccdb0efdfd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Eenvoudige afmetingen{#simple-dimensions}

Een eenvoudige dimensie heeft een één-aan-vele verhouding met zijn ouder telbare dimensie.

Een eenvoudige dimensie is altijd een kind van een telbare dimensie. U kunt aan een eenvoudige dimensie als vertegenwoordiging van een bezit van de elementen in zijn ouderafmeting denken. Bijvoorbeeld, als u met Webgegevens werkt, kon u de dimensie van de Verwijzing van de Bezoeker bepalen, die een eenvoudige afmeting met een ouderafmeting van Bezoeker is. Het vertegenwoordigt de eerste referentie van HTTP voor elke bezoeker in de dimensie van de Bezoeker. Elke bezoeker in de bezoekersdimensie heeft slechts één bezoeker, maar veel bezoekers kunnen de zelfde bezoeker hebben verwijzer. Daarom heeft de dimensie van de Verwijzing van de Bezoeker een één-aan-vele verhouding met de dimensie van de Bezoeker.

De eenvoudige afmetingen worden bepaald door de volgende parameters:

<table id="table_E6F729DFA226459DBFC1776CE8CB81F8"> 
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
   <td colname="col2"> Beschrijvende naam van de afmeting aangezien het in gegevenswerkbank verschijnt. De afmetingsnaam kan geen koppelteken (-) omvatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De voorwaarden waaronder de verhouding tussen de Ouder en de waarde van het inputgebied zou moeten worden gecreeerd. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Bepaalt of de afmeting in de interface van de gegevenswerkbank verschijnt. Door gebrek, wordt deze parameter geplaatst aan vals. Als, bijvoorbeeld, de afmeting slechts als basis van metrisch moet worden gebruikt, kunt u deze parameter aan waar plaatsen om de afmeting van de vertoning van de gegevenswerkbank te verbergen. </td> 
   <td colname="col3"> vals </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> Het gebied van waarden dat met de ouderdimensie (Ouder) verwant is. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand laden </td> 
   <td colname="col2"> <p>Optioneel. Een dossier van beschikbare waarden voor de verhouding. U gebruikt een ladingsdossier wanneer één van beiden van het volgende van toepassing is: </p> <p> 
     <ul id="ul_056C4A8E46AA479397DC63173C035D5C"> 
      <li id="li_C26EB5A4AB3C4BEB8EB3A217A5A2377E"> De waarden hebben een specifieke soortorde die u in de vertoning van de gegevenswerkbank wilt bewaren. Bijvoorbeeld, zou u een Kwartdimensie kunnen willen tot stand brengen de waarvan elementen (de kwartalen van het jaar) altijd in chronologische orde tonen. </li> 
      <li id="li_5D4DF56BC6124D038A7260131B1F3DB3"> U wilt plaatshouders voor waarden tot stand brengen die niet in de gegevens kunnen worden gevonden maar in de vertoning van de gegevenswerkbank moeten verschijnen. </li> 
     </ul> </p> <p> Als een waarde wordt ontmoet die niet aanwezig in het dossier is, wordt het toegevoegd aan het eind van de waarden wanneer bekeken in gegevenswerkbank. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Exploitatie </td> 
   <td colname="col2"> <p>De beschikbare verrichtingen zijn als volgt: </p> <p> 
     <ul id="ul_88AE4279413C42609D8B53EC64B5E913"> 
      <li id="li_DD9623D006844BC28B2AAA8E12AA04E1"> EERSTE NONBLANK: De eerste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de eerste logboekingang komt. Als de Input een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. </li> 
      <li id="li_0FBE7F0B7B9744D994ECEDAA08F0045C"> EERSTE RIJ: De waarde voor de eerste logboekingang met betrekking tot het element van de ouderafmeting wordt gebruikt, zelfs als de input leeg is. Als de Input een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen aantal, of als de relevante logboekingang niet aan de Voorwaarde van de afmeting voldoet, wordt geen waarde gebruikt. </li> 
      <li id="li_C17190BC699D4A099DC5326C07D1044D"> LAATSTE NONBLANK: De laatste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de laatste logboekingang komt. Als de Input een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. </li> 
      <li id="li_00BAE86F12004C098F6A455908DB7062"> LAATSTE RIJ: De waarde voor de laatste logboekingang met betrekking tot het element van de ouderafmeting wordt gebruikt, zelfs als de input leeg is. Als de Input een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen aantal, of als de relevante logboekingang niet aan de Voorwaarde van de afmeting voldoet, wordt geen waarde gebruikt. </li> 
     </ul> </p> <p> <p>Opmerking:  Als de Verrichting geen waarde of een lege waarde voor een bepaalde logboekingang oplevert, zal het overeenkomstige element van de ouderafmeting op "niets"element van de eenvoudige afmeting betrekking hebben. </p> </p> <p> U zou een verrichting moeten specificeren om ervoor te zorgen dat de afmeting zoals bedoeld wordt bepaald. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ouder </td> 
   <td colname="col2"> De naam van de ouderafmeting. Om het even welke telbare afmeting kan een ouderafmeting zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Dit voorbeeld illustreert de definitie van een eenvoudige afmeting gebruikend gebeurtenisgegevens die van websiteverkeer en een ladingsdossier worden verzameld.

Neem het voorbeeld van een opiniepeiling van de favoriete Girl Scout koekjes van bezoekers. Een Web-pagina vangt deze stem en keert het terug naar de Webserver in de naam-waarde paar voorkeur architectuur. Er wordt slechts één stem per bezoeker geteld, maar bezoekers kunnen hun mening veranderen en opnieuw stemmen indien gewenst. Dit is een relatie van één op vele: een bezoeker kan veel stemmen hebben , maar elke stem wordt geassocieerd met slechts één bezoeker . Daarom is de ouder van de dimensie bezoekers (slechts één stem per bezoeker) en de verrichting is LAATSTE ROW (zodat zij hun mening kunnen veranderen en opnieuw kunnen stemmen).

Placeholders moeten voor alle types van koekjes bestaan zodat de koekjestypes die geen stemmen ontvangen in de vertoning van de gegevenswerkbank verschijnen. Om deze redenen, is een ladingsdossier bepaald dat de lijst van koekjestypes bevat die kunnen worden geselecteerd. De inhoud van dit dossier, bewaard in een dossier genoemd [!DNL cookietypes.txt], kijkt iets als het volgende:

Dierlijke Treasurerings

Caramel Delights

Lemon Pastry Creams

Pandut Butter Patties

Kortere paden

Minimaal

De definitieve afmeting wordt bepaald zoals hieronder getoond:

![](assets/cfg_Transformation_Dim_Simple.png)

