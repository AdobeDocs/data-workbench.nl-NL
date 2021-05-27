---
description: Een eenvoudige dimensie heeft een één-aan-vele verhouding met zijn oudertelbare dimensie.
title: Eenvoudige Dimension
uuid: 3bca2354-02c4-4739-a7da-acccdb0efdfd
exl-id: 2acad750-7c48-40f1-8130-ab056ac8bf0d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# Eenvoudige Dimension{#simple-dimensions}

Een eenvoudige dimensie heeft een één-aan-vele verhouding met zijn oudertelbare dimensie.

Een eenvoudige dimensie is altijd een onderliggend element van een aftelbare dimensie. U kunt een eenvoudige dimensie zien als een representatie van een eigenschap van de elementen in de bovenliggende dimensie. Als u bijvoorbeeld met webgegevens werkt, kunt u de dimensie Verwijzer bezoeker definiëren. Dit is een eenvoudige dimensie met een bovenliggende dimensie van Bezoeker. Deze vertegenwoordigt de eerste HTTP-referentie voor elke bezoeker in de dimensie Visitor. Elke bezoeker in de dimensie Bezoeker heeft slechts één bezoekersreferentie, maar veel bezoekers kunnen dezelfde bezoekersreferentie hebben. Daarom heeft de dimensie Bezoekerreferentie een-op-een-relatie met de dimensie Bezoeker.

Eenvoudige afmetingen worden gedefinieerd door de volgende parameters:

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
   <td colname="col2"> Beschrijvende naam van de dimensie zoals deze wordt weergegeven in de werkbank voor gegevens. De naam van de dimensie mag geen afbreekstreepje (-) bevatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De voorwaarden waaronder de relatie tussen de bovenliggende waarde en de waarde van het invoerveld moet worden gemaakt. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Hiermee wordt bepaald of de dimensie wordt weergegeven in de interface van de gegevenswerkbank. Deze parameter is standaard ingesteld op false. Als de afmeting bijvoorbeeld alleen als basis van een metrische waarde moet worden gebruikt, kunt u deze parameter instellen op true om de afmeting te verbergen in de weergave op de werkbank. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> Het waardenveld dat gerelateerd is aan de bovenliggende dimensie (parent). </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand laden </td> 
   <td colname="col2"> <p>Optioneel. Een bestand met beschikbare waarden voor de relatie. U gebruikt een laadbestand wanneer een van de volgende twee van toepassing is: </p> <p> 
     <ul id="ul_056C4A8E46AA479397DC63173C035D5C"> 
      <li id="li_C26EB5A4AB3C4BEB8EB3A217A5A2377E"> De waarden hebben een specifieke sorteervolgorde die u wilt behouden in de weergave van de gegevenswerkbank. U kunt bijvoorbeeld een kwartdimensie maken waarvan de elementen (de kwartalen van het jaar) altijd in chronologische volgorde worden weergegeven. </li> 
      <li id="li_5D4DF56BC6124D038A7260131B1F3DB3"> U wilt plaatsaanduidingen maken voor waarden die mogelijk niet in de gegevens worden gevonden, maar wel in de weergave van de werkbank met gegevens moeten worden weergegeven. </li> 
     </ul> </p> <p> Als een waarde wordt aangetroffen die niet aanwezig is in het bestand, wordt deze toegevoegd aan het einde van de waarden bij weergave in de werkbank voor gegevens. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bewerking </td> 
   <td colname="col2"> <p>De beschikbare bewerkingen zijn als volgt: </p> <p> 
     <ul id="ul_88AE4279413C42609D8B53EC64B5E913"> 
      <li id="li_DD9623D006844BC28B2AAA8E12AA04E1"> EERSTE NONBLANK: De eerste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de eerste logboekingang komt. Als Invoer een vectorveld is, wordt de eerste rij in de vector voor het desbetreffende logbestandvermelding gebruikt. </li> 
      <li id="li_0FBE7F0B7B9744D994ECEDAA08F0045C"> EERSTE RIJ: De waarde voor de eerste logbestandvermelding die betrekking heeft op het bovenliggende dimensielement wordt gebruikt, zelfs als de invoer leeg is. Als Invoer een vectorveld is, wordt de eerste rij in de vector voor het desbetreffende logbestandvermelding gebruikt. Als deze waarde leeg is of geen getal, of als het relevante logbestandvermelding niet voldoet aan de voorwaarde van de dimensie, wordt geen waarde gebruikt. </li> 
      <li id="li_C17190BC699D4A099DC5326C07D1044D"> LAATSTE NONBLANK: De laatste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de laatste logboekingang komt. Als Invoer een vectorveld is, wordt de eerste rij in de vector voor het desbetreffende logbestandvermelding gebruikt. </li> 
      <li id="li_00BAE86F12004C098F6A455908DB7062"> LAATSTE RIJ: De waarde voor de laatste logbestandvermelding die betrekking heeft op het bovenliggende dimensielement wordt gebruikt, zelfs als de invoer leeg is. Als Invoer een vectorveld is, wordt de eerste rij in de vector voor het desbetreffende logbestandvermelding gebruikt. Als deze waarde leeg is of geen getal, of als het relevante logbestandvermelding niet voldoet aan de voorwaarde van de dimensie, wordt geen waarde gebruikt. </li> 
     </ul> </p> <p> <p>Opmerking:  Als de Verrichting geen waarde of een lege waarde voor een bepaalde logboekingang oplevert, zal het overeenkomstige element van de ouderafmeting op "niets"element van de eenvoudige afmeting betrekking hebben. </p> </p> <p> Geef een bewerking op om ervoor te zorgen dat de dimensie op de juiste manier wordt gedefinieerd. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bovenliggend </td> 
   <td colname="col2"> De naam van de bovenliggende dimensie. Elke aftelbare dimensie kan een bovenliggende dimensie zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Dit voorbeeld illustreert de definitie van een eenvoudige dimensie met behulp van gebeurtenisgegevens die zijn verzameld uit websiteverkeer en een laadbestand.

Bekijk het voorbeeld van een opiniepeiling van favoriete Girl Scout cookies van sitebezoekers. Een webpagina legt deze stem vast en retourneert deze naar de webserver in de naam-waardeparen-favoriet. Er wordt slechts één stem per bezoeker geteld, maar bezoekers kunnen hun mening wijzigen en desgewenst opnieuw stemmen. Dit is een één-op-veel relatie: een bezoeker kan veel stemmen hebben , maar elke stem heeft slechts betrekking op één bezoeker . Daarom is de ouder van de dimensie bezoekers (slechts één stem per bezoeker) en de operatie is LAST ROW (zodat zij hun mening kunnen veranderen en opnieuw kunnen stemmen).

Voor alle soorten cookies moeten plaatsaanduidingen aanwezig zijn, zodat de cookietypen die geen stemmen ontvangen, worden weergegeven in de weergave op de werkbank. Daarom is een laadbestand gedefinieerd dat de lijst bevat met cookietypen die kunnen worden geselecteerd. De inhoud van dit bestand, opgeslagen in een bestand met de naam [!DNL cookietypes.txt], ziet er ongeveer als volgt uit:

Dierlijke schatten

Caramel Delights

Lemon Pastry Creams

Peanut Butter Patches

Shortbreads

Dunne minuten

De uiteindelijke afmeting wordt hier weergegeven:

![](assets/cfg_Transformation_Dim_Simple.png)
