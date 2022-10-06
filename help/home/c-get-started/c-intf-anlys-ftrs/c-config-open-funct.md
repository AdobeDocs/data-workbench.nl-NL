---
description: Met de open functionaliteit kunt u items zoals documenten of URI's openen in externe toepassingen, zoals een teksteditor of een webbrowser.
title: Open functionaliteit configureren
uuid: dfa79a2b-e9ff-4e62-b15b-ae7911adeafd
exl-id: c807a284-b544-41cf-958b-27b47d2142ce
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# Open functionaliteit configureren{#configure-open-functionality}

{{eol}}

Met de open functionaliteit kunt u items zoals documenten of URI&#39;s openen in externe toepassingen, zoals een teksteditor of een webbrowser.

De open functionaliteit wordt momenteel gevormd slechts in [!DNL Site] en alleen voor het openen van URI&#39;s. Deze sectie bevat informatie over het configureren van de Open URI-functionaliteit voor [!DNL Site]. Voor informatie over het vormen van Open functionaliteit voor een andere toepassing of om andere punten te openen, contacteer de Raadgevende Diensten van de Adobe.

In [!DNL Site]kunt u met de rechtermuisknop op een URI van een paginabedekking of tabel klikken om de URI weer te geven in de toepassing waarvoor deze is opgemaakt. Vanuit een URI-tabelvisualisatie kunt u bijvoorbeeld op een URI klikken om een webpagina in een webbrowser weer te geven.

Als u een URI wilt openen vanuit een visualisatie, moet u eerst de [!DNL Open URI.cfg] bestand voor de URI-dimensie om de locatie en naamgevingsconventies te identificeren die Data Workbench gebruikt om de URI te openen. Om een URI in zijn inheemse formaat (zoals HTML) te bekijken, moet de Data Workbench toegang tot de referenced plaats en de toepassing hebben nodig om dat punt te openen. Als u bijvoorbeeld een webpagina wilt weergeven, heeft Data Workbench toegang tot internet nodig en is er een webbrowser geïnstalleerd.

**Open URI.vw bewerken**

1. In de [!DNL Profile Manager], klikt u op **[!UICONTROL Context]** > **[!UICONTROL Dimension Element]** > **[!UICONTROL URI]**.
1. Klik in de map URI met de rechtermuisknop op het vinkje naast de knop [!DNL Open URI.vw]bestand en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]** als het bestand een [!DNL .cfg] bestand of **[!UICONTROL Open]** > **[!UICONTROL in Notepad]** als het een [!DNL .vw] bestand.
1. Klikken **[!UICONTROL Command]** vervolgens **[!UICONTROL Parameters]** om de inhoud van het bestand weer te geven.
1. De [!DNL Site] parameter en de parameter van het Malplaatje zonodig:

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
   <td colname="col2"> <p>De parameters die Data Workbench zou moeten gebruiken om van URIs de plaats te bepalen en te openen. </p> <p>Voorbeeld: <span class="filepath"> https://%Site%%URI%</span> </p> <p>De standaardsjabloon die in het voorbeeld wordt weergegeven, vertelt de Data Workbench om een webbrowser te openen en zoekt naar de locatie die in het dialoogvenster <span class="wintitle"> Site</span> , zoekt u het element URI-dimensie dat u wilt openen. </p> </td>
  </tr>
 </tbody>
</table>

1. Sla het bestand op.
1. Als u deze wijziging beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor de optie [!DNL .vw] in het [!DNL User] kolom en klik op **[!UICONTROL Save to]** > **[!UICONTROL working profile name]**.
