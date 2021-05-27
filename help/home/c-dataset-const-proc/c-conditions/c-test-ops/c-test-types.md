---
description: De vergelijkingsvoorwaarde en de voorwaarde van de Waaier vereisen dat u het type van vergelijking specificeert dat voor de voorwaarde moet worden gemaakt.
title: Testtypes voor testbewerkingen
uuid: dc0433dd-a35e-472e-8975-f58347512c11
exl-id: 8abed46e-e76d-47c0-bbe9-cf98cf2d61e8
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Testtypes voor de Verrichtingen van de Test{#test-types-for-test-operations}

De vergelijkingsvoorwaarde en de voorwaarde van de Waaier vereisen dat u het type van vergelijking specificeert dat voor de voorwaarde moet worden gemaakt.

In de volgende tabel worden de beschikbare typen beschreven ( [!DNL LEXICAL], [!DNL NUMERIC] en [!DNL DATETIME]).

<table id="table_1B3AD8BDF0414D0AB8EE0E6D1B53E2CE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Testtype </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Notities </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> INTEGER</span> </p> </td> 
   <td colname="col2"> <p>Zet eerst het invoerveld in een geheel getal. Als dit niet mogelijk is, wordt een waarde van nul gebruikt. De test retourneert alleen true als de resulterende waarde voor de invoer van gehele getallen groter dan of gelijk is aan de opgegeven minimumwaarde en kleiner dan of gelijk is aan de opgegeven maximumwaarde. </p> </td> 
   <td colname="col3"> <p>Als een van de velden min of max leeg blijft, gebruikt het systeem de juiste minimale of maximale waarde die beschikbaar is voor 64-bits gehele getallen met teken. </p> <p> Als de min- of maximumwaarde die in de voorwaarde is opgegeven, niet met succes wordt geparseerd naar een geheel-getalwaarde, vervangt het systeem nul en stopt het niet met het verwerken van de gegevensset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> DATETIME</span> </p> </td> 
   <td colname="col2"> <p>Zet eerst het invoerveld in een datum. Als het invoerveld niet in een geldige datum kan worden omgezet, retourneert de voorwaardetest false. Als het veld in een datum kan worden omgezet, retourneert de test alleen de waarde "true" als de invoerdatum op of na de opgegeven minimumdatum valt en op of voor de opgegeven maximumdatum. </p> </td> 
   <td colname="col3"> <p>Als de minimale en maximale datums niet geldig zijn, wordt de gegevensset niet samengesteld. </p> <p> Als de minimale of maximale data niet worden opgegeven, vervangt het systeem op de juiste wijze ofwel de minimale datum (1 januari 1600) ofwel de maximale datum (ergens in de 24e eeuw). </p> <p> Adobe raadt u aan een van de volgende indelingen te gebruiken voor <span class="wintitle"> DATETIME</span>: </p> 
    <ul id="ul_44F469CC5D974382AF70D7B1975CF077"> 
     <li id="li_DB5FD4AFD6B34436ACD7C13282F64956"> 1 januari 2013 HH:MM:SS EDT </li> 
     <li id="li_307580C3F97D495BB16F1212DB38CE37"> 1 januari 2013 UU:MM:SS GMT </li> 
    </ul> <p> De tijdzone wordt standaard ingesteld op GMT als dit niet is opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> LEXISCH</span> </p> </td> 
   <td colname="col2"> <p>Retourneert alleen true als het invoerveld lexicaal groter dan of gelijk is aan de tekenreeks die is opgegeven als het minimum en kleiner dan of gelijk aan de tekenreeks die is opgegeven in de maximumwaarde. </p> </td> 
   <td colname="col3"> <p>Bij Lexicale vergelijking wordt de ASCII-waarde gebruikt van tekens in de tekenreeksen die van links naar rechts worden verplaatst en waarbij de tekens worden vergeleken. Voor het eerste teken dat niet overeenkomt, wordt het teken met de grotere ASCII-waarde beschouwd als de grootste van de twee. Als de ene tekenreeks korter is dan de andere, maar tot dat punt alle tekens hetzelfde zijn geweest, wordt de langere tekenreeks beschouwd als de grootste van de twee. Als de tekenreeksen voor tekenequivalent en exact dezelfde lengte zijn, worden ze lexicaal gelijk geacht. </p> </td> 
  </tr> 
 </tbody> 
</table>
