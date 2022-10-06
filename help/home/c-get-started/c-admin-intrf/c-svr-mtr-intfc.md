---
description: De interface van de Monitor van de Server is nuttig voor het oplossen van problemen of eenvoudig het volgen van de prestatiesparameters van de servercomputers van de Data Workbench en de computers van het Rapport die cliënten van de servercomputers van de Data Workbench zijn.
title: Servermonitorinterface
uuid: 609dd8ea-31a9-44c1-ab75-ca783ec85650
exl-id: fb8baae9-ac1e-4355-ba38-fef6621e22bb
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Servermonitorinterface{#server-monitor-interface}

{{eol}}

De interface van de Monitor van de Server is nuttig voor het oplossen van problemen of eenvoudig het volgen van de prestatiesparameters van de servercomputers van de Data Workbench en de computers van het Rapport die cliënten van de servercomputers van de Data Workbench zijn.

De interface van de Monitor van de Server toont of een groene punt of een rode punt bij zijn bovenkant, links van de computernaam. Een groene stip geeft aan dat de computer werkt zonder problemen. Een rode stip geeft aan dat een of meer fouten zijn opgetreden op de computer.

Het lagere gedeelte van de interface van de Monitor van de Server maakt een lijst van de verwerkingsstatus van elk van uw beschikbare profielen evenals prestatiesdetails over de computer.

Meer informatie over [!DNL Data Workbench servers], zie de *Handleiding voor installatie en beheer van serverproducten*. Meer informatie over [!DNL Report], zie de *Data Workbench Report Guide*.

**Om de interface van de Monitor van de Server te openen**

* Klik in Serverbeheer met de rechtermuisknop op het knooppunt van de Data Workbench-server of [!DNL Report] computer. t

Klikken **[!UICONTROL Server Monitor]** om details over één server te bekijken, of klik **[!UICONTROL Related Servers]** > **[!UICONTROL Server Monitor List]** om details over een cluster van verwante servers te bekijken.

![](assets/vis_ServerMonitor.png)

De [!DNL Server Monitor]interface werkt automatisch om de 10 seconden bij.

In de volgende tabel worden de taken weergegeven die u kunt voltooien met de opdracht [!DNL Server Monitor] interface.

<table id="table_A65426669ADE44B5A6BAD9D4E99A5CAC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Deze taak uitvoeren... </th> 
   <th colname="col2" class="entry"> Doe dit... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>De logverwerkingsstatus van een profiel controleren </p> </td> 
   <td colname="col2"> <p>Profiel weergeven <i>Profiel</i> Geef de vector een naam. In het bovenstaande voorbeeld zou u de Profile ExampleProfile-vector bekijken om te zien dat het ExampleProfile-profiel op één server wordt verwerkt en dat de logverwerking 100% is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om te bepalen hoe lang de computer duurt om op verzoeken te antwoorden </p> </td> 
   <td colname="col2"> <p>Geef het veld Opiniepeilingswachttijd weer. Als deze waarde groter is dan 1000ms, contacteer de Diensten van de Steun van de Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een schatting weergeven van hoe lang het kan duren voordat de transformatie is voltooid of de query is uitgevoerd </p> </td> 
   <td colname="col2"> <p>De sweep-tijd weergeven (uh:mm:ss). Dit veld is alleen aanwezig tijdens transformatie of query. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Het huidige aantal netwerkverbindingen met de computer bepalen </p> </td> 
   <td colname="col2"> <p>De laatste regel van de computer weergeven <span class="wintitle"> Servercontrole</span> informatie. In het bovenstaande voorbeeld ziet u dat momenteel twee netwerkverbindingen van één computer afkomstig zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>
