---
description: De open functionaliteit laat u toe om dergelijke punten zoals documenten of URIs in dergelijke externe toepassingen zoals een tekstredacteur of Webbrowser te openen.
solution: Analytics
title: Open functionaliteit configureren
topic: Data workbench
uuid: dfa79a2b-e9ff-4e62-b15b-ae7911adeafd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Open functionaliteit configureren{#configure-open-functionality}

De open functionaliteit laat u toe om dergelijke punten zoals documenten of URIs in dergelijke externe toepassingen zoals een tekstredacteur of Webbrowser te openen.

De open functionaliteit wordt momenteel gevormd slechts in de [!DNL Site] toepassing en slechts voor het openen URIs. Deze sectie verstrekt informatie over het vormen van de Open functionaliteit van URI voor [!DNL Site]. Voor informatie over het vormen van Open functionaliteit voor een andere toepassing of om andere punten te openen, contacteer de Raadplegende Diensten van Adobe.

In [!DNL Site], kunt u URI van een paginabekleding of een lijst met de rechtermuisknop aanklikken om URI in de toepassing te tonen waarvoor het werd geformatteerd. Bijvoorbeeld, van een de lijstvisualisatie van URI, kunt u URI klikken om een Web-pagina in Webbrowser te tonen.

Om URI van een visualisatie te openen, moet u eerst het [!DNL Open URI.cfg] dossier voor de dimensie van URI uitgeven om de plaats en noemende overeenkomsten te identificeren die de Werkbank van Gegevens gebruikt om URI te openen. Om URI in zijn inheems formaat (zoals HTML) te bekijken, moet de Werkbank van Gegevens toegang tot de referenced plaats en de toepassing hebben nodig om dat punt te openen. Bijvoorbeeld, om een Web-pagina te bekijken, zou de Werkbank van Gegevens toegang tot Internet nodig hebben evenals Webbrowser geïnstalleerd hebben.

**Open URI.vw bewerken**

1. Klik in het [!DNL Profile Manager], op **[!UICONTROL Context]** > **[!UICONTROL Dimension Element]** > **[!UICONTROL URI]**.
1. In de omslag van URI, klik het vinkje naast het [!DNL Open URI.vw]dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]** als het dossier een [!DNL .cfg] dossier of **[!UICONTROL Open]** > **[!UICONTROL in Notepad]** is als het een [!DNL .vw] dossier is.
1. Klik **[!UICONTROL Command]**, dan **[!UICONTROL Parameters]** om de inhoud van het dossier te bekijken.
1. Wijzig zonodig de [!DNL Site] parameter en de parameter van het Malplaatje:

<table id="table_CDB316DB271F476AB9F9B557B86AFD25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Verstrek deze informatie... </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Plaats </p> </td> 
   <td colname="col2"> <p>De plaats van URIs die u wilt openen. </p> <p>Voorbeeld: mysite.com </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sjabloon </p> </td> 
   <td colname="col2"> <p>De parameters die de Werkbank van Gegevens zou moeten gebruiken om van URIs de plaats te bepalen en te openen. </p> <p>Voorbeeld: <span class="filepath"> http://%Site%%URI%</span> </p> <p>Het standaardmalplaatje dat in het voorbeeld wordt getoond vertelt de Werkbank van Gegevens om Webbrowser te openen, zoek de plaats die in de parameter van de <span class="wintitle"> Plaats</span> wordt bepaald, dan bepaal de plaats van het de afmetingselement van URI u probeert te openen. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Sla het bestand op.
1. Om deze verandering beschikbaar te maken voor alle gebruikers van het het werk profiel, klik het vinkje voor het [!DNL .vw] dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Save to]** > **[!UICONTROL working profile name]**.

