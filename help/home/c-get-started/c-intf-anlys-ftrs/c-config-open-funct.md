---
description: Met de open functionaliteit kunt u items zoals documenten of URI's openen in externe toepassingen, zoals een teksteditor of een webbrowser.
title: Open functionaliteit configureren
uuid: dfa79a2b-e9ff-4e62-b15b-ae7911adeafd
exl-id: c807a284-b544-41cf-958b-27b47d2142ce
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# Open functionaliteit configureren{#configure-open-functionality}

Met de open functionaliteit kunt u items zoals documenten of URI&#39;s openen in externe toepassingen, zoals een teksteditor of een webbrowser.

De open functionaliteit wordt momenteel gevormd slechts in de [!DNL Site] toepassing en slechts voor het openen van URIs. Deze sectie bevat informatie over het configureren van de Open URI-functionaliteit voor [!DNL Site]. Voor informatie over het vormen van Open functionaliteit voor een andere toepassing of om andere punten te openen, contacteer de Raadgevende Diensten van de Adobe.

In [!DNL Site], kunt u URI van een paginabekleding of lijst met de rechtermuisknop aanklikken om URI in de toepassing te tonen waarvoor het werd geformatteerd. Vanuit een URI-tabelvisualisatie kunt u bijvoorbeeld op een URI klikken om een webpagina in een webbrowser weer te geven.

Als u een URI wilt openen vanuit een visualisatie, moet u eerst het [!DNL Open URI.cfg]-bestand voor de URI-dimensie bewerken om de locatie- en naamgevingsconventies te identificeren die de Data Workbench gebruikt om de URI te openen. Als u een URI in de eigen indeling (zoals HTML) wilt weergeven, moet de Data Workbench toegang hebben tot de locatie waarnaar wordt verwezen en de toepassing die nodig is om dat item te openen. Als u bijvoorbeeld een webpagina wilt weergeven, heeft Data Workbench toegang tot internet nodig en is er een webbrowser geïnstalleerd.

**Open URI.vw bewerken**

1. Klik in [!DNL Profile Manager] op **[!UICONTROL Context]** > **[!UICONTROL Dimension Element]** > **[!UICONTROL URI]**.
1. Klik in de map URI met de rechtermuisknop op het vinkje naast het [!DNL Open URI.vw]bestand en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]** als het bestand een [!DNL .cfg]-bestand is of **[!UICONTROL Open]** > **[!UICONTROL in Notepad]** als het een [!DNL .vw]-bestand is.
1. Klik **[!UICONTROL Command]**, dan **[!UICONTROL Parameters]** om de inhoud van het dossier te bekijken.
1. Pas de parameter [!DNL Site] en de parameter van het Malplaatje zonodig aan:

<table id="table_CDB316DB271F476AB9F9B557B86AFD25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Deze informatie opgeven... </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Site </p> </td> 
   <td colname="col2"> <p>De locatie van de URI's die u wilt openen. </p> <p>Voorbeeld: mijnsite.com </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sjabloon </p> </td> 
   <td colname="col2"> <p>De parameters die Data Workbench zou moeten gebruiken om van URIs de plaats te bepalen en te openen. </p> <p>Voorbeeld: <span class="filepath"> http://%Site%%URI%</span> </p> <p>Het standaardmalplaatje dat in het voorbeeld wordt getoond vertelt Data Workbench om Webbrowser te openen, zoekt de plaats die in <span class="wintitle"> wordt bepaald Plaats </span> parameter, dan bepaal de plaats van het de afmetingselement van URI u probeert te openen. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Sla het bestand op.
1. Als u deze wijziging beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor het bestand [!DNL .vw] in de kolom [!DNL User] en klikt u op **[!UICONTROL Save to]** > **[!UICONTROL working profile name]**.
