---
description: De interface van de Monitor van de Server is nuttig voor het oplossen van problemen of eenvoudig het volgen van de prestatiesparameters van de servercomputers van de Werkbank van Gegevens en de computers van het Rapport die cliënten van de servercomputers van de Werkbank van Gegevens zijn.
solution: Analytics
title: Servermonitorinterface
topic: Data workbench
uuid: 609dd8ea-31a9-44c1-ab75-ca783ec85650
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Servermonitorinterface{#server-monitor-interface}

De interface van de Monitor van de Server is nuttig voor het oplossen van problemen of eenvoudig het volgen van de prestatiesparameters van de servercomputers van de Werkbank van Gegevens en de computers van het Rapport die cliënten van de servercomputers van de Werkbank van Gegevens zijn.

De interface van de Monitor van de Server toont of een groene punt of een rode punt bij zijn bovenkant, links van de computernaam. Een groene punt wijst erop dat de computer zonder kwestie functioneert. Een rode punt wijst erop dat één of meerdere fouten op de computer zijn voorgekomen.

Het lagere gedeelte van de interface van de Monitor van de Server maakt een lijst van de verwerkingsstatus van elk van uw beschikbare profielen evenals prestatiesdetails over de computer.

Voor meer informatie over [!DNL Data Workbench servers], zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server van de Installatie en van het Beleid. Voor meer informatie over [!DNL Report], zie de Gids *van het Rapport van het Rapport van de* Werkbank van Gegevens.

**Om de interface van de Monitor van de Server te openen**

* In de Manager van Servers, klik de knoop van de server of de [!DNL Report] computer van de Werkbank van Gegevens met de rechtermuisknop aan. t

Klik **[!UICONTROL Server Monitor]** aan meningsdetails over één server, of klik **[!UICONTROL Related Servers]** > **[!UICONTROL Server Monitor List]** om details over een cluster van verwante servers te bekijken.

![](assets/vis_ServerMonitor.png)

De [!DNL Server Monitor]interface werkt automatisch om de 10 seconden bij.

De volgende lijst maakt een lijst van de taken die kunnen worden voltooid gebruikend de [!DNL Server Monitor] interface.

<table id="table_A65426669ADE44B5A6BAD9D4E99A5CAC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Om deze taak uit te voeren... </th> 
   <th colname="col2" class="entry"> Doe dit... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Om de status van de logboekverwerking van een profiel te controleren </p> </td> 
   <td colname="col2"> <p>Bekijk de vector van de Naam van het <i>Profiel</i> van het Profiel. In het voorbeeld hierboven, zou u de vector van ExampleProfile van het Profiel bekijken om te zien dat de het profielprocessen ExampleProfile op één server en zijn logboekverwerking 100% volledig zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om te bepalen hoe lang de computer duurt om op verzoeken te antwoorden </p> </td> 
   <td colname="col2"> <p>Bekijk het gebied van de opiniepeilingslatentie. Als deze waarde groter is dan 1000ms, contacteer de Diensten van de Steun van Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om een schatting te bekijken hoe lang het zou kunnen duren om transformatie te voltooien of het vragen </p> </td> 
   <td colname="col2"> <p>Bekijk het gebied van de sweep time (hh:mm:ss), dat slechts tijdens transformatie of het vragen aanwezig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om het huidige aantal netwerkverbindingen aan de computer te bepalen </p> </td> 
   <td colname="col2"> <p>Bekijk de laatste lijn van de informatie van de Monitor <span class="wintitle"> van de</span> Server van de computer. In het voorbeeld hierboven, ziet u dat 2 netwerkverbindingen momenteel van één computer komen. </p> </td> 
  </tr> 
 </tbody> 
</table>

